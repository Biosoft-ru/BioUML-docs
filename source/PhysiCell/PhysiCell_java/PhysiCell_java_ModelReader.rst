.. _PhysiCell_java_ModelReader:

ModelReader
===========

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

Класс ModelReader используется для чтения модели из текстового файла.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.xml.ModelReader

Все члены класса ModelReader представлены в ниже.

.. list-table:: Члены класса ModelReader
   :header-rows: 1

   * - Член класса
     - Описание

   * - static readColor(String color)
     - | color - цвет, например "green", "red" или "rgb(100,100,255)".
       |
       | Возвращает цвет, описываемый строкой color.
       |
       | :ref:`Пример <PhysiCell_java_Biorobots_BiorobotsVisualizer_java>` использования.