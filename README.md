# Домашнее задание к лекции «Модули»

## Задание webpackimport/export

Разделите всё приложение на модули:

Модуль Domain - где будет храниться логика предметной области (персонажи, атаки и т.д.)
Модуль Game - отвечающий за работу приложения (загрузку и сохранение)
Модуль App - отвечающий за запуск приложения
Заглушки для модулей:

файл domain.js:

`class Character {
}`

файл game.js

`class Game {
  start() {
    console.log('game started');
  }
}

class GameSavingData {
}

function readGameSaving() {
}

function writeGameSaving() {
}`

файл app.js

`const game = new Game();
game.start();`

## Организуйте:

Из модуля domain экспорт класса Character в качестве default'ного
В модуле game импорт класса Character
Экспорт из модуля game класса Game в качестве дефолтного, класса GameSavingData и функций readGameSaving и writeGameSaving
В модуле app.js одним импортом импортируйте Game, GameSavingData и функции readGameSaving, writeGameSaving (их при импорте переименуйте в loadGame и saveGame соответственно)
С самими функциями и классами ничего делать не нужно, нужно только правильно расставить инструкции import/export.

install server
`npm i -D http-server`