# Task_1

## Задание
Реализовать программу на языке C\C++, которая должна включать
следующую последовательность действий:
1. Запрос какой-либо информации от пользователя (логин, номер
телефона, номер какого-либо документа, ключ любого вида и т.д.)
2. Произведение манипуляций по разработанному алгоритму с
введённой пользователем информацией для генерации ответа на
ключевой вопрос.
3. Запрос ключа от пользователя и сравнение его со сгенерированным
ключом на этапе 2.
4. Выдача результата по принципу: сгенерированный и алгоритмом и введённый пользователем
ключи совпадают – TRUE-> Поздравление или доступ к какой
либо информации; Не совпадают – ошибка.

При реализации программы должны быть соблюдены условия:
1. Внутри программы должен быть какой-либо алгоритм преобразования
данных для генерации ключевой информации. Например, сложение по
модулю кодов букв из таблицы ASCII, Подсчёт количества букв в
логине пользователя и умножение его на текущий год, запросы
системного времени или к каким-либо заранее определённым файлам.
2. Должны быть реализованы меры защиты от отладки: специальные
функции языка, искусственное усложнение кода, директивы
препроцессора, условия сборки компилятора, упаковщики и т. д.

Результатом выполнения задания должна быть разработанная программа в
виде исходных кодов, make/cmake файла сборки или инструкции по
сборке в случае применения дополнительных средств или специальных
скриптов. Документация к программе с описанием алгоритма работы,
описанием входных и выходных данных и применяемых в программе мер
защиты.

## Описание программы
На входе программа запрашивает логин (любая комбинация символов без пробелов). Затем логин преобразуется в ключ с помощью функции Transform.

Запрашивается пароль (комбинация символов без пробелов, которая использует заглавные и строчные буквы английского алфавита, цивры от 0 до 9, а также @ и .)
После этого происходит сравнения ключа с паролем.

На выходе программа выводит одну из двух строчек: "Access granted\n"или "Access denied\n".

>Все запрашиваемые данные обрезаются или дополняются символом "Q" до длины строки 32.

## Меры защиты
В качестве мер защиты были использованы: 
* маркосы C++ для выводимых строк;
* искуственное усложение кода: были добавлены "бессмысленные" операции с числами и строками, 
* при сборке файла были использованы флаги: -O3 (оптимизация и ухудшение читабельности)
* пост обработка бинарного файла с помощью функции strip
