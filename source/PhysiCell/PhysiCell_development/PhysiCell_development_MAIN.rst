Начало работы с PhysiCell моделью
=================================

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

.. |icon_Type_Diagram| image:: /images/icons/Type-Diagram-icon.png
.. |icon_opened_folder| image:: /images/icons/Physicell/opened_folder.png
.. |icon_cell_definition| image:: /images/icons/Physicell/cell_definition.png
.. |icon_substrate| image:: /images/icons/Physicell/substrate.png
.. |icon_secretion| image:: /images/icons/Physicell/secretion_corrected.png
.. |icon_chemotaxis| image:: /images/icons/Physicell/chemotaxis_corrected.png
.. |icon_interaction| image:: /images/icons/Physicell/interaction_corrected.png
.. |icon_transformation| image:: /images/icons/Physicell/transformation_corrected.png
.. |icon_event| image:: /images/icons/Physicell/event.png

Чтобы начать работать с моделью, сначала нужно ее открыть. Для этого два раза ЛКМ нажмите на |icon_Type_Diagram| или нажмите ПКМ на |icon_Type_Diagram| и в выпадающем списке нажмите ЛКМ на |icon_opened_folder| **Open**.

.. figure:: /images/Physicell/Physicell_model_development/Open_the_diagram.png
   :width: 50%
   :alt: Open_the_diagram
   :align: center

:raw-html:`<br>`
После этого в левой верхней части экрана появится окно, в котором можно создавать модель.

.. figure:: /images/Physicell/Physicell_model_development/Diagram_window.png
   :width: 100%
   :alt: Diagram_window
   :align: center

:raw-html:`<br>`
В верхней части этого окна можно видеть панель инструментов, которые используются для построения PhysiCell модели.

.. figure:: /images/Physicell/Physicell_model_development/Diagram_instruments.png
   :width: 50%
   :alt: Diagram_instruments
   :align: center

:raw-html:`<br>`
Выбрать тот или иной инструмент можно нажатием на соответствующую иконку ЛКМ. Описание каждого инструмента представлено ниже.

.. list-table:: Элементы панели инструментов, используемой при работе с PhysiCell моделями
   :header-rows: 1

   * - Обозначение
     - Описание

   * - .. image:: /images/icons/Physicell/cursor.png
          :alt: курсор
     - Выбор элемента на диаграмме
   * - .. image:: /images/icons/Physicell/cell_definition.png
          :alt: тип клеток
     - Тип клеток
   * - .. image:: /images/icons/Physicell/substrate.png
          :alt: субстрат
     - Субстрат
   * - .. image:: /images/icons/Physicell/event.png
          :alt: событие
     - Событие
   * - .. image:: /images/icons/Physicell/note.png
          :alt: примечание
     - Примечание
   * - .. image:: /images/icons/Physicell/secretion_corrected.png
          :alt: секреция
     - Секреция/Потребление
   * - .. image:: /images/icons/Physicell/chemotaxis_corrected.png
          :alt: хемотаксис
     - Хемотаксис
   * - .. image:: /images/icons/Physicell/interaction_corrected.png
          :alt: взаимодействие
     - Взаимодействие
   * - .. image:: /images/icons/Physicell/transformation_corrected.png
          :alt: трансформация
     - Трансформация

Основными участниками PhysiCell модели являются клетки различных типов (|icon_cell_definition|) и субстраты (|icon_substrate|).

Между ними возможно 4 типа взаимодействий:

- **Секреция/Потребление** (|icon_secretion|): выделение/поглощение клеткой того или иного субстрата.
- **Хемотаксис** (|icon_chemotaxis|): движение клетки к или от определенного субстрата.
- **Взаимодействие** (|icon_interaction|): воздействие клеток одного типа на клетки другого типа,
- **Трансформация** (|icon_transformation|): превращение клеток одного типа в клетки другого типа.

.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_development_Cells
   PhysiCell_development_Substrate
   PhysiCell_development_Secretion
   PhysiCell_development_Chemotaxis
   PhysiCell_development_Interaction
   PhysiCell_development_Transformation
   PhysiCell_development_Event
   PhysiCell_development_Change_color