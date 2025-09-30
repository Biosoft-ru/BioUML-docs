.. _PhysiCell_java_StandardModels:

StandardModels
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

Класс StandardModels используется для работы со стандартными моделями клеточного цикла и клеточной смерти.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.standard.StandardModels

Все члены класса StandardModels представлены ниже.

.. list-table:: Члены класса StandardModels
   :header-rows: 1

   * - Член класса
     - Описание

   * - static live
     - | Содержит жизненный цикл клетки "Live".
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - static int live.findPhaseIndex(int/String phase)
     - | phase - численный код или название одной из фаз жизненного цикла "Live".
       |
       | Возвращает индекс (номер) фазы жизненного цикла "Live" с кодом (названием) phase.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.