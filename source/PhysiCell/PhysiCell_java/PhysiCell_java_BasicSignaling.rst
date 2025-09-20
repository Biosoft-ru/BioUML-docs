.. _PhysiCell_java_BasicSignaling:

BasicSignaling
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

Класс BasicSignaling используется для работы с методами, которые рассчитывают значение выходного сигнала на основе одного входящего сигнала.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.BasicSignaling

Все члены класса BasicSignaling представлены ниже.

.. list-table:: Члены класса BasicSignaling
   :header-rows: 1

   * - Член класса
     - Описание

   * - static double linear_response_function(double signal, double min, double max)
     - | signal - значение входящего сигнала.
       | min - минимальное значение.
       | max - максимальное значение.
       |
       | возвращает ответ на сигнал signal по следующей формуле:
       | :math:`\frac{signal-min}{max-min}`,
       | отображающей значение сигнала signal с отрезка [min, max] на отрезок [0, 1].
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - static double decreasing_linear_response_function(double signal, double min, double max)
     - | signal - значение входящего сигнала.
       | min - минимальное значение.
       | max - максимальное значение.
       |
       | Возвращает ответ на сигнал signal по следующей формуле:
       | :math:`(signal-max)*(max-min)`,
       | отображающей значение сигнала signal с отрезка [min, max] на отрезок [-1, 0].
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - static double Hill_response_function(double signal, double half_max, double hill_power)
     - | signal - значение входящего сигнала.
       | half_max - значение сигнала, при котором ответ достигает половины от своей максимально возможной величины.
       | hill_power - коэффициент Хилла.
       |
       | Возвращает ответ на сигнал signal по :ref:`формуле Хилла <PhysiCell_java_hill_function>`.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.