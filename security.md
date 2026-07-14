---
layout: page
title: OpenFlow Security
permalink: /security.html
---

## Сообщить об уязвимости

Отправьте приватное сообщение [Telegram @pnklrd](https://t.me/pnklrd) с пометкой
`OpenFlow security`. Не публикуйте working exploit, invite tokens, provider keys,
document contents или персональные данные в открытом issue.

Полезно указать:

- затронутую версию и компонент;
- безопасные шаги воспроизведения;
- ожидаемый и фактический результат;
- оценку возможного impact.

Мы постараемся подтвердить получение в течение трёх рабочих дней, провести первичную
оценку в течение 14 дней и сообщать о существенных изменениях статуса. Срок fix
зависит от severity и сложности. Public bug bounty сейчас отсутствует.

## Security model beta

- Figma network access ограничен одним HTTPS relay domain.
- Relay фиксирует upstream и model и не принимает client-supplied Authorization
  или upstream URL.
- Provider key хранится вне Figma как system credential.
- Invite tokens проверяются по SHA-256 hash и могут быть отозваны.
- Requests ограничены по размеру, частоте, concurrency и daily quota.
- Prompt и response bodies не сохраняются и не логируются relay.
- UI и main thread независимо проверяют semantic и geometry payload до document
  mutation; update выполняется через atomic group replacement.

OpenFlow beta не заявляет SOC 2, ISO 27001 или иную независимую сертификацию.
