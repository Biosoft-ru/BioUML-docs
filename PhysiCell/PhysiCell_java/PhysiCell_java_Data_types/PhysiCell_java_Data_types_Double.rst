.. _PhysiCell_java_Data_types_Double:

float, double
=============

.. role:: raw-html(raw)
   :format: html

.. raw:: html

    <style>
    table {
        border-collapse: collapse;
        width: 100%;
        background-color: white;
        table-layout: fixed;
    }
    th, td {
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
        word-wrap: break-word;
        overflow-wrap: break-word;
        hyphens: auto;
        -webkit-hyphens: auto;
        -moz-hyphens: auto;
        white-space: normal;
    }
    td p {
        word-wrap: break-word;
        overflow-wrap: break-word;
        word-break: break-all;
        hyphens: auto;
        -webkit-hyphens: auto;
        -moz-hyphens: auto;
        white-space: normal;
        margin: 0; /* убираем лишние отступы, если нужно */
    }
    /* ДОБАВЬТЕ ЭТИ СТИЛИ — КЛЮЧЕВОЕ ИЗМЕНЕНИЕ! */
    .line-block,
    .line-block .line {
        white-space: normal !important;
        word-wrap: break-word !important;
        overflow-wrap: break-word !important;
        hyphens: auto !important;
        -webkit-hyphens: auto !important;
        -moz-hyphens: auto !important;
    }
    tr:nth-child(even) {
        background-color: white;
    }
    th {
        background-color: #2980B9;
        color: white;
    }
    .table-bottom-margin {
        margin-top: 20px;
    }
    </style>

Оба этих типа данных являются примитивными и описывают числа с плавающей точкой с разной точностью. В таблице ниже приведено их сравнение.

.. list-table:: Сравнение типов данных float и double
   :header-rows: 1

   * - Тип данных
     - Точночть
     - Размер, байт
     - Пример

   * - float
     - Одинарная точность
     - 4
     - float f = 3.14f
   * - double
     - Двойная точность
     - 8
     - double d = 19.99

.. warning::
  При указании типа данных float в конце числа ставится знак "f" или "F".

Чаще всего для описания числа с плавающей точкой используется тип данных double.