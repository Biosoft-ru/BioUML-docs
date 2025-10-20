.. _PhysiCell_java_Model:

Model
=====

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

Класс Model используется для работы с мультиклеточной моделью для численных расчетов.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.Model

Все члены класса Model представлены в ниже.

.. list-table:: Члены класса Model
   :header-rows: 1

   * - Член класса
     - Описание
     
   * - | SignalBehavior getSignals()
       |
       | или
       |
       | SignalBehavior signals
     - | Возвращает (содержит) объект, обрабатывающий прием сигналов от клеток и регулирующий поведение клеток.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_CargoCellRule_java>` использования.
   * - RandomGenerator getRNG()
     - | Возвращает генератор случайных чисел данной модели.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - CellDefinition getCellDefinition(String name)
     - | name - название типа клеток.
       |
       | Возвращает тип клеток с названием name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - Microenvironment getMicroenvironment()
     - | Возвращает среду модели.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - double getParameterDouble(String name)
     - | name - название параметра модели.
       |
       | Возвращает значение параметра name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - int getParameterInt(String name)
     - | name - название параметра модели.
       |
       | Возвращает целочисленное значение параметра name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - String getParameterString(String name)
     - | name - название параметра модели.
       |
       | Возвращает строковое значение параметра name.
       |
       | :ref:`Пример <PhysiCell_java_Biorobots_BiorobotsVisualizer_java>` использования.
   * - void setSaveFullInterval(double interval)
     - | interval - временной интервал.
       |
       | Устанавливает временной интервал interval для сохранения полных результатов расчета модели.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
