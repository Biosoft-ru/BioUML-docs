
.. _PhysiCell_simulation_Engine_Save_report:

Сохранение таблиц (Save report)
===============================

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

.. |icon_option| image:: /images/icons/option.png

Если опция |icon_option| **Save report** включена, то после завершения симуляции в директории с результатами у вас будет находиться папка с названием **Reports**.

В этой папке находятся таблицы с названием **Report_[модельное время]**. Значение модельного времени, указанное в названии, говорит о том, через сколько временных единиц после начала симуляции была сгенерирована данная таблица.

Количество таблиц будет зависеть от значений параметров **Max Time** и **Report interval** (см. пример ниже).

.. code-block:: text
   :caption: Пример

   Report interval = 10 (таблицы сохраняются через каждые 10 модельных временных единиц).
   Max Time = 100 (симуляция длится 100 модельных временных единиц).

   Таблицы в папке Reports:
   - Report_0000,
   - Report_0010,
   - Report_0020,
   - Report_0030,
   - Report_0040,
   - Report_0050,
   - Report_0060,
   - Report_0070,
   - Report_0080,
   - Report_0090,
   - Report_0100.

В этих таблицах для каждой клетки в модели представлены следующие данные:

- **ID**: уникальный идентификатор каждой клетки.
- **X**: координата клетки по оси X.
- **Y**: координата клетки по оси Y.
- **Z**: координата клетки по оси Z.
- **Cycle**: тип жизненного цикла клетки.
- **Elapsed**: время, проведенное клеткой в текущей фазе жизненного цикла.

Пример такой таблицы представлен ниже:

.. list-table:: 
   :header-rows: 1
   
   * - ID
     - X
     - Y
     - Z
     - Cycle
     - Elapsed
   * - 0
     - 12.096
     - 54.536
     - 0.000
     - Live
     - 0.0
   * - 1
     - -16.753
     - 487.781
     - 0.000
     - Live
     - 0.0
   * - 2
     - 434.889
     - -235.863
     - 0.000
     - Live
     - 0.0
   * - 3
     - -317.709
     - 70.606
     - 0.000
     - Live
     - 0.0
   * - 4
     - 297.120
     - -104.069
     - 0.000
     - Live
     - 0.0
   * - 5
     - 498.915
     - -157.909
     - 0.000
     - Live
     - 0.0
   * - 6
     - -82.918
     - 92.278
     - 0.000
     - Live
     - 0.0
   * - 7
     - 398.698
     - -41.584
     - 0.000
     - Live
     - 0.0
   * - 8
     - 164.770
     - 318.611
     - 0.000
     - Live
     - 0.0
   * - 9
     - 986.695
     - 292.718
     - 0.000
     - Live
     - 0.0

.. important::
   Выводимые данные можно поменять, указав пользовательский java-код в поле **report** в подвкладке **Model report** вкладки **Microenvironment**, предварительно отметив ☑ напротив **Custom report**.
