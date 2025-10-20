.. _PhysiCell_java_SignalBehavior:

SignalBehavior
==============

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

Класс SignalBehavior используется для управления передачи сигналов и поведения клеток.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.SignalBehavior

Все члены класса SignalBehavior представлены ниже.

.. list-table:: Члены класса SignalBehavior
   :header-rows: 1

   * - Член класса
     - Описание

   * - double getSingleSignal(Cell cell, String signal)
     - | cell - клетка.
       | signal - название сигнала.
       |
       | Возвращает численное значение сигнала signal, описывающего тот или иной аспект жизни клетки cell.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_CargoCellRule_java>` использования.
   * - void setSingleBehavior(Cell cell, String signal, double value)
     - | cell - клетка.
       | signal - название сигнала.
       | value - значение.
       |
       | Устанавливает значение value сигналу signal, описывающему тот или иной аспект жизни клетки cell.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_CargoCellRule_java>` использования.