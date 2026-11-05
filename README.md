# Интерактивный пульт VINTEO

[**Открыть интерактивное демо**](https://youtimelex.github.io/vinteo-remote-control/) — пульт и демонстрация отклика терминала в браузере.

## Скачать

- [Только пульт — HTML](https://github.com/youtimelex/vinteo-remote-control/releases/latest/download/remote.html) — интерактивный пульт на чёрном фоне.
- [Пульт с демонстрацией — HTML](https://github.com/youtimelex/vinteo-remote-control/releases/latest/download/index.html) — пульт и демонстрационный интерфейс терминала.
- [Все файлы проекта — ZIP](https://github.com/youtimelex/vinteo-remote-control/releases/latest/download/vinteo-remote-control.zip).

HTML-файлы можно открыть в современном браузере без установки и подключения к интернету. Пульт реагирует на нажатия; в отдельном файле стрелки перемещают фокус, Enter нажимает выбранную кнопку, Escape и Backspace отправляют команды возврата.

**Это прототип:** отклик терминала в демо условный, соединения с устройством нет. Для управления реальным терминалом потребуется отдельная интеграция.

## Интеграция

В `remote.html` элемент `#remote-study` генерирует событие `remote-command`. В `event.detail.command` находится название нажатой кнопки, а `event.detail.source` содержит `remote`. Приложение может подписаться на событие и сопоставить команды со своим API. Протокол и подключение терминала в проект не входят.

В полной демонстрации `index.html` также генерируется событие `remote-command` с источником `demo` и демонстрационным состоянием. Иконки Lucide встроены в HTML; условия использования приведены в `LICENSE-lucide.txt`.
