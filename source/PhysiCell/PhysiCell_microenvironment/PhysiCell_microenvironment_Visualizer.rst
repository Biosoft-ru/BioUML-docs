.. _PhysiCell_microenvironment_Visualizer:

Визуализация клеток (Visualizer)
================================

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

.. |icon_plus| image:: /images/icons/Physicell/plus.png
.. |icon_minus| image:: /images/icons/Physicell/minus.png
.. |icon_blue_circle| image:: /images/icons/Physicell/blue_circle.png
.. |icon_red_circle| image:: /images/icons/Physicell/red_circle.png
.. |icon_purple_circle| image:: /images/icons/Physicell/purple_circle.png

.. warning::
   Перед редактированием этой вкладки сначала необходимо настроить вкладку :ref:`Color schemes <PhysiCell_microenvironment_Color_schemes>`.

В этом разделе задаются условия, по которым к клетке применяются те или иные цветовые схемы, заданные во вкладке :ref:`Color schemes <PhysiCell_microenvironment_Color_schemes>`.

.. note::
   Также эти условия можно задавать через Java-код во вкладке :ref:`Model Report <PhysiCell_microenvironment_Model_Report>`, выбрав опцию **Custom visualizer** и указав путь в репозитории до нужного файла.

Для добавления и удаления условий применения цветовых схем используются кнопки |icon_plus| и |icon_minus|, соответственно.

Для каждого условия можно настроить следующие параметры:

.. figure:: /images/Physicell/Physicell_microenvironment/Add_new_color_scheme_condition.png
   :width: 100%
   :alt: Add_new_color_scheme_condition
   :align: center

:raw-html:`<br>`

- **Cell Type**: тип клеток, к которому будет применяться условие.
- **Priority**: приотритет применения данного условия.
- **Color type**: правило применения цветовой схемы.
- **Signal**: свойство клетки, значения которого применяются в условии.
- **Color 1**: 1-ая цветовая схема.
- **Color 2**: 2-ая цветовая схема.
- **Min value**: минимальное значение выбранного свойства клетки (Signal).
- **Max value**: максимальное значение выбранного свойства клетки (Signal).

Значения полей **Cell Type**, **Color type**, **Signal**, **Color 1** и **Color 2** выбираются из раскрывающихся списков.

Чтобы задать значения полей **Priority**, **Min value** и **Max value**, нужно нажать ЛКМ под соответствующим заголовком и вписать собственное значение.

Особое внимание следует уделить правилам применения цветовых схем (**Color type**). Всего существует 4 таких правила:

- **Fixed color**: всегда применяется только одна цветовая схема, заданная в поле Color 1 (:raw-html:`<span style="color: red;">поле Color 2 при выборе такого правила становится неактивным</span>`).
- **Gradient**: цвет клетки изменяется по градиенту от 1-ой цветовой схемы (Color 1) ко 2-ой (Color 2) в зависимости от значения выбранного свойства клетки (Signal) относительно минимума (Min value) и максимума (Max value).
- **Larger than max**: если значение свойства клетки (Siganl) больше, чем максимум (Max value), то к клетке применяется 1-ая цветовая схема (Color 1); во всех остальных случаях применяется 2-ая цветовая схема (Color 2).
- **Smaller than min**: если значение свойства клетки (Siganl) меньше, чем минимум (Min value), то к клетке применяется 1-ая цветовая схема (Color 1); во всех остальных случаях применяется 2-ая цветовая схема (Color 2).

.. note::
   Поле **Priority** используется только для правил *Larger than max* и *Smaller than min*.
   
   Если в какой-то момент времени к одному и тому же типу клеток применяется одновременно несколько условий с такими типами правил, то будет выполняться то из них, которое имеет наименьшее значение в поле Priority.

Ниже показано, как работают разные правила применения цветовых схем на примере со следующими настройками:

- **Color 1**: |icon_blue_circle|.
- **Color 2**: |icon_red_circle|.
- **Min value**: 10.
- **Max value**: 100.

.. list-table:: Пример работы различных правил применения цветовых схем
   :header-rows: 1

   * - Правило
     - Signal = 0
     - Signal = 50
     - Signal = 200

   * - Fixed color
     - |icon_blue_circle|
     - |icon_blue_circle|
     - |icon_blue_circle|
   * - Gradient
     - |icon_blue_circle|
     - |icon_purple_circle|
     - |icon_red_circle|
   * - Larger than max
     - |icon_red_circle|
     - |icon_red_circle|
     - |icon_blue_circle|
   * - Smaller than min
     - |icon_blue_circle|
     - |icon_red_circle|
     - |icon_red_circle|
