.. _PhysiCell_java_PhysiCellConstants:

PhysiCellConstants
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

Класс PhysiCellConstants используется для работы с константными численными значениями модели.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.PhysiCellConstants

Все члены класса PhysiCellConstants представлены ниже.

.. list-table:: Члены класса PhysiCellConstants
   :header-rows: 1

   * - Член класса
     - Описание

   * - static int apoptotic
     - | Возвращает численный код фазы "Apoptotic" цикла клеточной смерти "Apoptosis".
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - static int necrotic_swelling
     - | Возвращает численный код фазы "Necrotic (swelling)" цикла клеточной смерти "Necrosis".
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - static int necrotic_lysed
     - | Возвращает численный код фазы "Necrotic (lysed)" цикла клеточной смерти "Necrosis".
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - static int live
     - | Возвращает численный код фазы "Live" жизненного цикла "Live".
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - static int apoptosis_death_model
     - | Возвращает индекс типа клеточной смерти "Apoptosis".
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - static int necrosis_death_model
     - | Возвращает индекс типа клеточной смерти "Necrosis".
       |
       | :ref:`Пример <PhysiCell_java_Interactions_DifferentiatedPhenotype_java>` использования.