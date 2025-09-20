.. _PhysiCell_java_UpDownSignal:

UpDownSignal
============

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

Класс UpDownSignal используется для расчета эффекта выходного сигнала по :ref:`формуле Хилла <Physicell_java_hill_function>` на основе множественных входящих сигналов-эффектов.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.standard.UpDownSignal

Все члены класса UpDownSignal представлены ниже.

.. list-table:: Члены класса UpDownSignal
   :header-rows: 1

   * - Член класса
     - Описание

   * - UpDownSignal sig = new UpDownSignal(Model model)
     - | model - модель.
       |
       | Создает новый сигнал sig в модели model.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - double baseParameter
     - | Возвращает базовое значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - double maxParameter
     - | Возвращает максимальное значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - addEffect(double value, String direction)
     - | value - значение.
       | direction - направленность*.
       |
       | \*Возможные значения направленности:
       | 1) "n (N)" - нейтральный,
       | 2) "i (I)" - ингибитор,
       | 3) "p (P)" - промотор.
       |
       | Добавляет эффект со значением value и направленностью direction.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - computeEffect()
     - | Вычисляет значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - reset()
     - | Обнуляет все параметры сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.

.. _PhysiCell_java_hill_function:

Формула Хилла
~~~~~~~~~~~~~

Формула Хилла имеет следующий вид:

.. math::

   Y = \frac{L^h}{L_{0,5}^h + L^h},

где:

- Y - значение выходящего сигнала,
- L - значение входящего сигнала,
- :math:`L_{0,5}` - значение входящего сигнала, при котором значение выходящего сигнала равно половине от максимального возможного,
- h - коэффициент Хилла.

График данной функции имеет S-образную форму.

.. figure:: /images/Physicell/Physicell_java_code/Hill_function.png
   :width: 100%
   :alt: Hill_function
   :align: center

:raw-html:`<br>`