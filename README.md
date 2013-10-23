Конкурс красоты кода
====================

Компания XIAG проводит первый конкурс красоты кода.

[![Scrutinizer Quality Score](https://scrutinizer-ci.com/g/Magomogo/code-competition/badges/quality-score.png?s=425109351a8488b0b72903e0132a4cd07fb39c5f)](https://scrutinizer-ci.com/g/Magomogo/code-competition/)

[![Code Coverage](https://scrutinizer-ci.com/g/Magomogo/code-competition/badges/coverage.png?s=2202d932963da16b3956425579078cc8356e148d)](https://scrutinizer-ci.com/g/Magomogo/code-competition/)

Правила
=======

- Участник должен иметь github - аккаунт
- Форкнув этот репозиторий разработчик объявляет о своем участии в конкурсе
- Разработанный код должен пройти ./acceptance_test.php, необходимо изменить функцию doTest для вызова своей реализации
  задания
- Покрытие кода тестами рассчитывает phpunut, тесты должны быть расположены в директории ./test
- Оценка красоты кода проводится голосованием с использованием формальных метрик, которые рассчитавает Scrutinizer:
  https://scrutinizer-ci.com/g/Magomogo/code-competition/ к голосованию допускаются любые пользователи, голос отдаётся
  звездочкой, поставленной репозиторию участника.

Установка
=========

    composer install --dev
    ./acceptance_test.php
    ./phpunit

Задание
=======

Необходимо написать разбиватель списка на страницы. Входные параметры:

- $offset, номер первой показываемой записи
- $total, общее количество записей
- $rowsPerPage, количество записей на страницу
- $pagesCount, количество номеров страниц, которые нужно показать

Результатом должна быть текстовая строка с номерами страниц, и выделенной текущей страницей:

    3 4 [5] 6 7
