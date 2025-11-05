.. _PhysiCell_java_Microenvironment:

Microenvironment
================

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

Класс Microenvironment используется для работы со средой модели, в которой находятся клетки и вещества.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.biofvm.Microenvironment

Все члены класса Microenvironment представлены ниже.

.. list-table:: Члены класса Microenvironment
   :header-rows: 1

   * - Член класса
     - Описание

   * - mesh
     - | Содержит :ref:`решетку <Physicell_microenvironment_Domain>` внешней среды.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - double[] mesh.boundingBox
     - | Содержит массив из 6 значений - :ref:`границы <Physicell_microenvironment_Domain>` внешней среды [Xmin, Xmax, Ymin, Ymax, Zmin, Zmax].
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - options
     - | Содержит настройки внешней среды модели.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_Initial_java>` использования.
   * - boolean options.simulate2D
     - | Содержит true, если модель двумерная.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_Initial_java>` использования.
   * - double[] options.X_range
     - | Содержит массив [Xmin, Xmax], в котором первый элемент - минимальное значение координаты x внешней среды, а второй - максимальное.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_TherapyEvent_java>` использования.
   * - double[] options.Y_range
     - | Содержит массив [Ymin, Ymax], в котором первый элемент - минимальное значение координаты y внешней среды, а второй - максимальное.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_TherapyEvent_java>` использования.
   * - RandomGenerator getRNG()
     - | Возвращает генератор случайных чисел данной среды.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_Initial_java>` использования.
   * - int findDensityIndex(String substrate)
     - | substrate - название субстрата.
       |
       | Вовзращает индекс (номер) плотности субстрата substrate.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - List<Cell> getAgents([metadata].class)
     - | metadata - метаданные о другом классе (практически всегда используется класс :ref:`Cell <Physicell_java_Cell>`).
       |
       | Возвращает список всех агентов (клеток) выбранного класса.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.