# Описание проекта
Этот проект реализует конвейер данных с использованием Apache Airflow для подсчета общего количества символа 'a' в 100 случайно сгенерированных текстовых файлах.

## Этапы работы конвейера:
1)Генерация файлов: Создаются 100 текстовых файлов, каждый из которых содержит 1000 случайных символов латинского алфавита.

2)Параллельный подсчёт: Для каждого файла запускается поток, который подсчитывает количество символов 'a' в этом файле и сохраняет результат в файл с расширением .res.

3)Суммирование результатов: После завершения всех потоков запускается задача, которая суммирует значения из всех файлов .res и выводит общее количество символов 'a'.
##
Поскольку Airflow не поддерживается на Windows напрямую, используется Docker для развёртывания среды Airflow.
