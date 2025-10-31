Свойства всей модели
====================

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

.. |icon_increase_sorting| image:: /images/icons/Physicell/increase_sorting.png
.. |icon_decrease_sorting| image:: /images/icons/Physicell/decrease_sorting.png
.. |icon_option| image:: /images/icons/option.png
.. |icon_Java_code| image:: /images/icons/Physicell/Java_code.png
.. |icon_table| image:: /images/icons/Physicell/table.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png
.. |icon_plus| image:: /images/icons/Physicell/plus.png
.. |icon_minus| image:: /images/icons/Physicell/minus.png


Для редактирования общих свойств всей модели используется вкладка **Microenvironment**.

.. figure:: /images/Physicell/Physicell_microenvironment/microenvironment_tab.png
   :width: 100%
   :alt: microenvironment_tab
   :align: center
  
:raw-html:`<br>`
Чтобы ее открыть, нужно нажать на нее ЛКМ.

Данная вкладка содержит в себе набор вложенных вкладок, каждая из которых описывает различные аспекты модели:

.. figure:: /images/Physicell/Physicell_microenvironment/microenvironment_inner_tabs.png
   :width: 100%
   :alt: microenvironment_inner_tabs
   :align: center

:raw-html:`<br>`

- **Domain**: свойства сетки.
- **Substrates**: вещества.
- **Cell types**: типы клеток.
- **Events**: события.
- **User Parameters**: пользовательские параметры модели.
- **Initial Condition**: начальное расположение клеток.
- **Model Report**: отчет по модели.
- **Visualizer**: визуализация клеток.
- **Color schemes**: цветовые схемы.
- **Model Options**: другие параметры модели.

Чтобы открыть любую вкладку, нужно нажать на нее ЛКМ.

Далее подробно разберем работу с каждой из вкладок.

.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_microenvironment_Domain
   PhysiCell_microenvironment_Substrates
   PhysiCell_microenvironment_Cell_types
   PhysiCell_microenvironment_Events
   PhysiCell_microenvironment_User_parameters
   PhysiCell_microenvironment_Initial_condition
   PhysiCell_microenvironment_Model_report
   PhysiCell_microenvironment_Visualizer
   PhysiCell_microenvironment_Color_schemes
   PhysiCell_microenvironment_Model_options
