.. _PhysiCell_cell_properties_Cycle:

Жизненный цикл (Cycle)
======================

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
.. |icon_clue| image:: /images/icons/Physicell/clue.png
.. |icon_opened_clue| image:: /images/icons/Physicell/opened_clue.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png

После нажатия на вкладку **Cycle** на панели свойств справа у вас появится меню, в котором можно изменять параметры жизненного цикла клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Cycle_menu.png
   :width: 100%
   :alt: Cycle_menu
   :align: center

:raw-html:`<br>`

Название жизненного цикла клетки (Name)
---------------------------------------

При нажатии слева от кнопки |icon_option| **Name** раскрывается список, в котором можно выбрать тип жизненного цикла клетки:

.. figure:: /images/Physicell/Physicell_cell_properties/Cycle_name.png
   :width: 100%
   :alt: Cycle_name
   :align: center

:raw-html:`<br>`

- **Ki67 (basic)**: жизненный цикл, состоящий из двух фаз - :raw-html:`«<u>Ki67-</u>» и «<u>Ki67+</u>»`,
- **Ki67 (advanced**: жизненный цикл, состоящий из трех фаз - :raw-html:`«<u>Ki67-</u>», «<u>Ki67+ (premitotic)</u>» и «<u>Ki67+ (postmitotic)</u>»`,
- **Live**: простейший жизненный цикл, состоящий всего из одной фазы с условным названием :raw-html:`«<u>Live</u>»`,
- **Flow cytometry model (basic)**: жизненный цикл, состоящий из трех фаз - :raw-html:`«<u>G0/G1</u>», «<u>S</u>» и «<u>G2/M</u>»`,
- **Flow cytometry model (separated)**: жизненный цикл, состоящий из четырех фаз - :raw-html:`«<u>G0/G1</u>», «<u>S</u>», «<u>G2</u>» и «<u>M</u>»`,
- **Custom**: пользовательский жизненный цикл.

При выборе **Custom...** справа от поля |icon_option| **Custom cycle** нужно будет указать путь к модели, описывающий жизненный цикл клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Custom_cycle.png
   :width: 100%
   :alt: Custom_cycle
   :align: center

:raw-html:`<br>`

Фазы цикла (Phases) и переходы между ними (Transitions)
-------------------------------------------------------

При выборе определенного цикла автоматически изменяются вкладки поля **Phases** (фазы цикла) и **Transitions** (переходы между фазами цикла).

.. figure:: /images/Physicell/Physicell_cell_properties/Cycle_phases_transitions.png
   :width: 100%
   :alt: Cycle_phases_transitions
   :align: center

:raw-html:`<br>`
Чтобы открыть любую вкладку полей **Phases** или **Transitions**, нужно нажать ЛКМ на значок |icon_clue| слева от вкладки. Чтобы закрыть вкладку, нужно нажать ЛКМ на значок |icon_opened_clue| слева от вкладки.

.. figure:: /images/Physicell/Physicell_cell_properties/Open_and_close_tab.png
   :width: 100%
   :alt: Open_and_close_tab
   :align: center

:raw-html:`<br>`
При открытии любой из вкладок поля **Phases** появляется значок |icon_option| **Division on exit**. Отметьте ☑, если хотите, чтобы клетка делилась по окончании выбранной фазы жизненного цикла.

.. figure:: /images/Physicell/Physicell_cell_properties/Division_on_exit.png
   :width: 100%
   :alt: Division_on_exit
   :align: center

:raw-html:`<br>`
При открытии любой из вкладок поля **Transitions** появятся два значка:

.. figure:: /images/Physicell/Physicell_cell_properties/Transitions_rate_fixed.png
   :width: 100%
   :alt: Transitions_rate_fixed
   :align: center

:raw-html:`<br>`

- |icon_option| **Rate**: скорость перехода между соответствующими фазами жизненного цикла клетки (можно изменять, нажав ЛКМ на число слева и вписав собственное значение),
- |icon_option| **Fixed**: отметьте ☑, если хотите, чтобы время перехода между соответствующими фазами жизненного цикла клетки было зафиксировано.

.. note::
   При указании свойства Fixed переход между фазами жизненного цикла клетки происходит **ровно** через :math:`1/Rate` единиц времени поcле начала фазы.

   Если Fixed не указано, то переход происходит **в среднем** через :math:`1/Rate` единиц времени почле начала фазы. Моделируется это следующим образом:
   во время каждого шага агента (клетки) переход может произойти с вероятностью :math:`Rate*Phenotype \, dt`, где Phenotype dt- шаг модельного времени, с которым происходит обновление внутреннего состояния клеток (задается при настройках :ref:`симуляции модели <PhysiCell_simulation_Engine>`).

Редактирование фаз и переходов между ними
-----------------------------------------

Чтобы добавить новую фазу или переход в жизненный цикл клетки, нужно:

1. Нажать ЛКМ на вкладку |icon_option| **Phases** или |icon_option| **Transitions**.
2. Нажать ЛКМ на иконку |icon_add_new|.

.. figure:: /images/Physicell/Physicell_cell_properties/New_phase_or_transition.png
   :width: 100%
   :alt: New_phase_or_transition
   :align: center

:raw-html:`<br>`
После этого в соответствующем разделе у вас появится новая фаза или переход.

.. figure:: /images/Physicell/Physicell_cell_properties/New_phase.png
   :width: 100%
   :alt: New_phase
   :align: center

:raw-html:`<br>`
Кроме того, возможны и другие действия с фазами и переходами. Чтобы их отобразить, нужно нажать ЛКМ на любую фазу или переход, после чего сверху появится панель с возможными действиями.

.. figure:: /images/Physicell/Physicell_cell_properties/Actions_with_phases_or_transitions.png
   :width: 100%
   :alt: Actions_with_phases_or_transitions
   :align: center

:raw-html:`<br>`
Описание каждого из этих действий приведено ниже.

.. _PhysiCell_cell_properties_Actions:

.. list-table:: Элементы панели инструментов, используемой при работе с фазами и переходами жизненного цикла клетки
   :header-rows: 1
   :widths: 30 70

   * - Обозначние
     - Описание

   * - .. image:: /images/icons/Physicell/delete_phase_or_transition.png
     - Удаление выбранной фазы или перехода
   * - .. image:: /images/icons/Physicell/insert_before_phase_or_transition.png
     - Вставить новую фазу или переход перед выбранной
   * - .. image:: /images/icons/Physicell/insert_after_phase_or_transition.png
     - Вставить новую фазу или переход после выбранной
   * - .. image:: /images/icons/Physicell/move_up_phase_or_transition.png
     - Переместить выбранную фазу или переход выше
   * - .. image:: /images/icons/Physicell/move_down_phase_or_transition.png
     - Переместить выбранную фазу или переход ниже
