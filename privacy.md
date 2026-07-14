---
layout: page
title: OpenFlow Privacy Policy
permalink: /privacy.html
---

Дата вступления в силу: 14 июля 2026 года.

## Кратко

OpenFlow обрабатывает только данные, необходимые для построения user flow.
Plugin не использует accounts, analytics или advertising trackers. Не вводите в
prompt персональные, платёжные, медицинские, конфиденциальные или иные чувствительные
данные.

## Какие данные обрабатываются

При generation OpenFlow передаёт через `https://openflow.baboonshop.ru`:

- введённый пользователем prompt;
- ограниченную историю текущего OpenFlow-чата;
- текущий `FlowSpec` выбранной managed OpenFlow group, если пользователь редактирует
  уже применённую схему;
- revocable invite token, необходимый для доступа к beta relay.

OpenFlow не читает и не отправляет произвольное содержимое Figma canvas или
selection. Модель получает только текст пользователя и явно выбранный managed flow.

## Где хранятся данные

- Invite token хранится только в Figma `clientStorage` на стороне пользователя.
- После явного Apply ограниченная история чата, применённый `FlowSpec` и техническая
  metadata без secrets сохраняются в private plugin data созданной OpenFlow group.
- Неприменённый draft существует только в памяти plugin и не восстанавливается
  после закрытия.
- Relay хранит только SHA-256 hashes invite tokens, сведения об их статусе и
  дневные агрегаты использования за последние 30 дней.
- Relay не сохраняет prompts, chat, request/response bodies, provider responses,
  Authorization headers, upstream credentials или IP-адреса пользователей.

## Внешняя обработка

Запросы передаются по HTTPS через OpenFlow relay в OpenCode Go с фиксированной
моделью `deepseek-v4-flash`. OpenCode обрабатывает input и output для выполнения
generation. Условия обработки OpenCode опубликованы в его
[Privacy Policy](https://opencode.ai/legal/privacy-policy) и
[Terms of Service](https://opencode.ai/legal/terms-of-service).

Provider API key хранится только на сервере как system credential и никогда не
передаётся в Figma. OpenFlow не использует provider output для собственной
аналитики или обучения моделей.

## Удаление и управление

Пользователь может удалить token в Settings, удалить OpenFlow group из документа
или очистить её данные средствами Figma. Автор beta может отозвать invite token;
после revoke он перестаёт давать доступ к relay. Дневные агрегаты автоматически
удаляются по окончании 30-дневного retention period.

## Изменения и контакт

Существенные изменения этой политики будут опубликованы на этой странице до или
одновременно с обновлением plugin. Вопросы о privacy: [Telegram @pnklrd](https://t.me/pnklrd).
