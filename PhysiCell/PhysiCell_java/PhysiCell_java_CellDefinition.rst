.. _PhysiCell_java_CellDefinition:

CellDefinition
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

Класс CellDefinition используется для работы с типами клеток.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.CellDefinition

Все члены класса CellDefinition представлены ниже.

.. list-table:: Члены класса CellDefinition
   :header-rows: 1

   * - Член класса
     - Описание

   * - int type
     - | Содержит численный код (номер) данного типа клеток.
       |
       | :ref:`Пример <PhysiCell_java_Biorobots_BiorobotsVisualizer_java>` использования.
   * - CustomCellData custom_data
     - | Содержит объект, содержщий пользовательскую информацию о клетках данного типа.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - double custom_data.get(String name)
     - | name - название переменной данного типа клеток.
       |
       | Возвращает значение по умолчанию (стартовое) переменной name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.
   * - CellParameters parameters
     - | Содержит объект, содержащий информацию о дополнительных встроенных параметрах данного типа клеток.
       |
       | :ref:`Пример <PhysiCell_java_Heterogeneity_Initial_java>` использования.
   * - double parameters.o2_proliferation_saturation
     - | Содержит количество кислорода, при котором он перестает усиливать пролиферацию клеток данного типа.
       |
       | Используется для типа клеток с :ref:`фенотипом <Physicell_cell_properties_Functions>` «Default O2-based phenotype».
       |
       | :ref:`Пример <PhysiCell_java_Heterogeneity_Initial_java>` использования.
   * - double parameters.o2_reference
     - | Содержит референсное значение кислорода.
       |
       | :ref:`Пример <PhysiCell_java_Heterogeneity_Initial_java>` использования.