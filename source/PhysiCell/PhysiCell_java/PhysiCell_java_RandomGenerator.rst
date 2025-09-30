.. _PhysiCell_java_RandomGenerator:

RandomGenerator
===============

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

Класс RandomGenerator используется для генерации случайных величин в модели.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.RandomGenerator

Все члены класса RandomGenerator представлены ниже.

.. list-table:: Члены класса RandomGenerator
   :header-rows: 1

   * - Член класса
     - Описание

   * - boolean checkRandom(double probability)
     - | probability - вероятность (диапазон [0, 1]).
       |
       | Возвращает true, если probability > случайно сгенерированного числа из диапазона [0, 1].
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double UniformRandom()
     - | Возвращает случайное число с равномерным распределением от 0 до 1.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - double UniformRandom(double value1, double value2)
     - | value1 - число.
       | value2 - число.
       |
       | Возвращает случайное число с равномерным распределением от value1 до value2.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_TherapyEvent_java>` использования.
   * - double NormalRandom(double mean, double SD)
     - | mean - среднее значение.
       | SD - стандартное отклонение.
       |
       | Возвращает случайное число с нормальным распределением со средним значением mean и стандартным отклонением SD.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - double NormalRestricted(double mean, double SD, double min, double max)
     - | mean - среднее значение.
       | SD - стандартное отклонение.
       | min - минимальное значение.
       | max - максимальное значение.
       |
       | Возвращает случайное число с нормальным распределением со средним mean, стандартным отклонением SD, с минимальным значеним min и максимальным значением max.
       | Если значение этого числа выходит за заданные рамки, то возвращается ближайшее допустимое число.
       |
       | :ref:`Пример <PhysiCell_java_Heterogeneity_Initial_java>` использования.