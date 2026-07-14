---
layout: page
title: Как пользоваться OpenFlow
permalink: /guide.html
---

# Как пользоваться OpenFlow

OpenFlow — бесплатная русскоязычная Community beta для Figma Design. Из-за
ограниченной серверной квоты AI generation доступна по персональному revocable
invite token. Запросить token может любой пользователь Community через
[Telegram @pnklrd](https://t.me/pnklrd).

## Первый запуск

1. Установите OpenFlow из Figma Community и откройте его в Figma Design.
2. На вкладке **Настройки** вставьте invite token и нажмите
   **Проверить подключение**.
3. Перейдите в **Чат**, опишите happy path и две-три короткие развилки или
   воспользуйтесь кнопкой **Вставить пример**.
4. Нажмите **Создать preview** и проверьте узлы, переходы и предупреждения.
5. Нажмите **Добавить в Figma**. До этого шага canvas не изменяется.

## Изменение flow

Выделите созданную OpenFlow group и снова откройте plugin. Напишите follow-up,
создайте новый preview и примените его. OpenFlow старается сохранить stable nodes,
их ручные позиции и стили. Кнопка reset positions полностью перестраивает схему
без ручных привязок после явного подтверждения.

Вкладка **Mermaid** поддерживает ограниченный import/export. Chat рассчитан на
flows до 15 nodes и 30 transitions; Source и сохранённый документ — до 80/160.
Большой процесс лучше разделить на несколько схем.

## Данные и ограничения

OpenFlow отправляет только введённый prompt, ограниченную историю OpenFlow chat и
FlowSpec явно выбранной managed group. Не отправляйте secrets и чувствительные
персональные данные. Подробности: [Privacy Policy](privacy.html) и
[Beta Terms](terms.html).

Если connection test или generation не работает, пришлите безопасный текст ошибки
в [Telegram @pnklrd](https://t.me/pnklrd). Не присылайте invite token.
