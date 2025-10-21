.. _PhysiCell_java_PhysiCellUtilities:

PhysiCellUtilities
==================

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

Класс PhysiCellUtilities включает дополнительные методы работы с моделью.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.PhysiCellUtilities

Все члены класса PhysiCellUtilities представлены ниже.

.. list-table:: Члены класса PhysiCellUtilities
   :header-rows: 1

   * - Член класса
     - Описание

   * - static void place(Model model, String type, int number)
     - | model - модель.
       | type - название типа клеток.
       | number - целое положительное число.
       |
       | Добавляет в модель model клетки типа type, случайно распределенные по всей среде, в количестве number.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_Initial_java>` использования.
   * - static void place2D(Model model, String type, int number)
     - | model - модель.
       | type - название типа клеток.
       | number - целое положительное число.
       |
       | Добавляет в модель model клетки типа type, случайно распределенные по всей среде в плоскости z = 0, в количестве number.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Initial_java>` использования.
   * - static List<Cell> getNeighbors(Cell cell)
     - | cell - клетка.
       |
       | Возвращает массив, состоящий из соседей данной клетки - клеток в той же ячейке решетки и соседних ячейках.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PredatorPhenotype_java>` использования.