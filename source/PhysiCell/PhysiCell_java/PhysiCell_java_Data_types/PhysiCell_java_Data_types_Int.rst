.. _PhysiCell_java_Data_types_Int:

byte, short, int, long
======================

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

Все эти типы данных являются примитивными и описывают целые числа в разных диапазонах. В таблице ниже приведено сравнение этих типов данных.

.. list-table:: Сравнение типов данных byte, short, int и long
   :header-rows: 1

   * - Тип данных
     - Диапазон
     - Размер, байт
     - Пример

   * - byte
     - [-128; 127]
     - 1
     - byte b = 100
   * - short
     - [-32 768; 32 767]
     - 2
     - short s = 1000
   * - int
     - [-2³¹; 2³¹ – 1]
     - 4
     - int i = 25
   * - long
     - [-2⁶³; 2⁶³ – 1]
     - 8
     - long l = 1000L

.. warning::
  При указании типа данных long в конце числа ставится знак "L".

Чаще всего для описания целого числа используется тип данных int.