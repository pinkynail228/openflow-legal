---
layout: page
title: Как пользоваться OpenFlow
permalink: /guide.html
---

[English guide](guide-en.html)

# Как пользоваться OpenFlow

OpenFlow — бесплатная Mermaid-first Community beta для Figma Design. Основной
сценарий работает локально без регистрации, invite key и сетевых запросов.

## Mermaid: основной сценарий

1. Откройте OpenFlow: вкладка **Mermaid** выбрана по умолчанию.
2. Вставьте поддерживаемый Mermaid source или нажмите **Вставить пример**.
3. Нажмите **Предпросмотр** и проверьте узлы, переходы и предупреждения.
4. Нажмите **Добавить в Figma**. До этого canvas не изменяется.
5. Для обновления выделите созданную OpenFlow group, снова откройте plugin,
   измените Mermaid и примените изменения.

Изменённый source нужно снова проверить. Пока он dirty, применение и AI-запрос
заблокированы, чтобы не использовать устаревший FlowSpec.

## API: дополнительная AI beta

Откройте **API**, вставьте revocable OpenFlow invite key и нажмите **Проверить
ключ**. Это не личный provider key: OpenCode credential остаётся только на relay.
Принятый key хранится только в Figma `clientStorage` на этом устройстве.

После generation OpenFlow автоматически вернёт вас в Mermaid. Проверьте source и
предпросмотр, затем явно примените схему. API рассчитан на flow до 15 nodes и 30
transitions; Mermaid/document — до 80/160. Запросить бесплатный персональный key
может любой пользователь Community через [Telegram @pnklrd](https://t.me/pnklrd).

## Блоки, ветвления и ошибки

Встроенная кнопка `?` объясняет все восемь kinds и stable IDs. Только `decision`
и `decisionUser` могут иметь 2–3 подписанных исхода. `end` и `error` терминальны.
Исправимая ошибка — `card`/`subtle`, а последующий пользовательский выбор —
отдельный `decisionUser`. Кнопка **Вставить легенду в Figma** создаёт обычную
редактируемую group без managed-flow markers.

В меню выбранной схемы находятся **Сбросить ручные позиции** и **Очистить историю
API**. Интерфейс и новая AI generation поддерживают RU/EN; переключение языка не
переводит существующие diagram labels или chat.

Не отправляйте secrets или чувствительные персональные данные. Подробнее:
[Privacy Policy](privacy.html) и [Beta Terms](terms.html). Ошибки присылайте без
invite key в [Telegram @pnklrd](https://t.me/pnklrd).
