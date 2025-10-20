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

Класс UpDownSignal используется для расчета эффекта выходного сигнала согласно многомерному закону Хилла на основе множественных входящих сигналов-эффектов. Методы этого класса используются для вычисления влияния :ref:`правил <PhysiCell_cell_properties_Rules>`.


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
     - | Содержит базовое значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - double maxParameter
     - | Содержит максимальное значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - void addEffect(double value, String direction)
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
   * - void computeEffect()
     - | Вычисляет значение сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - void reset()
     - | Обнуляет все параметры сигнала.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.