.. _PhysiCell_simulation_Engine_Save_density:

Сохранение данных о веществах (Save density)
============================================

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

Если опция |icon_option| **Save density** включена, то после завершения симуляции в директории с результатами у вас будет находиться папка с названием **Density**.

В этой папке находятся таблицы с названием **Density_[модельное время]**. Значение модельного времени, указанное в названии, говорит о том, через сколько временных единиц после начала симуляции была сгенерирована данная таблица.

Количество таблиц будет зависеть от значений параметров **Max Time** и **Report interval** (см. пример ниже).

.. code-block:: text
   :caption: Пример

   Report interval = 10 (таблицы сохраняются через каждые 10 модельных временных единиц).
   Max Time = 50 (симуляция длится 50 модельных временных единиц).

   Таблицы в папке Density:
   - Density_0000,
   - Density_0010,
   - Density_0020,
   - Density_0030,
   - Density_0040,
   - Density_0050.

В этих таблицах для каждой ячейки внешней среды представлены следующие данные:

- **ID**: уникальный идентификатор каждой ячейки.
- **X**: координата ячейки по оси X.
- **Y**: координата ячейки по оси Y.
- **Z**: координата ячейки по оси Z.
- **[Субстрат 1]**: количество субстрата 1 в данной ячейке.
- **[Субстрат 2]**: количество субстрата 2 в данной ячейке.
- ...
- ...
- ...
- **[Субстрат n]**: количество субстрата n в данной ячейке.

.. note::
   В таблице для каждого субстрата модели будет своя колонка, где будет указано количество именно этого субстрата в данной ячейке.

Пример такой таблицы представлен ниже:

.. list-table:: 
   :header-rows: 1
   
   * - ID
     - X
     - Y
     - Z
     - Substrate
     - Substrate_1
   * - 1
     - -490,0
     - -490,0
     - 0,0
     - 0,005
     - 100,0
   * - 2
     - -470,0
     - -490,0
     - 0,0
     - 0,005
     - 100,0
   * - 3
     - -450,0
     - -490,0
     - 0,0
     - 0,005
     - 100,0
   * - 4
     - -430,0
     - -490,0
     - 0,0
     - 0,005
     - 100,0
   * - 5
     - -410,0
     - -490,0
     - 0,0
     - 0,005
     - 100,0
   * - ...
     - ...
     - ...
     - ...
     - ...
     - ...

▼ таблица продолжается ▼