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
       }
       th, td {
           border: 1px solid #dddddd;
           text-align: center;
           padding: 8px;
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
.. |icon_blue_circle| image:: /images/icons/Physicell/blue_circle.png
.. |icon_red_circle| image:: /images/icons/Physicell/red_circle.png
.. |icon_blue_red_gradient_circle| image:: /images/icons/Physicell/blue_red_gradient_circle.png

Для редактирования общих свойств всей модели используется вкладка **Microenvironment** :ref:`(Рисунок 1) <Physicell_microenvironment_Pic.1>`.

.. _Physicell_microenvironment_Pic.1:

.. figure:: images/Physicell/Physicell_microenvironment/microenvironment_tab.png
   :width: 100%
   :alt: microenvironment_tab
   :align: center

   Рисунок 1. Вкладка Microenvironment для редактирования свойств всей модели.

Чтобы ее открыть, нужно нажать на нее ЛКМ.

Данная вкладка содержит в себе набор вложенных вкладок, каждая из которых описывает различные аспекты модели :ref:`(Рисунок 2) <Physicell_microenvironment_Pic.2>`:

- **Domain**: свойства сетки,
- **Substrates**: вещества,
- **Cell types**: типы клеток,
- **Events**: события,
- **User Parameters**: пользовательские параметры модели,
- **Initial Condition**: начальное расположение клеток,
- **Model Report**: отчет по модели,
- **Visualizer**: визуализация клеток,
- **Color schemes**: цветовые схемы,
- **Model Options**: другие параметры модели.

.. _Physicell_microenvironment_Pic.2:

.. figure:: images/Physicell/Physicell_microenvironment/microenvironment_inner_tabs.png
   :width: 100%
   :alt: microenvironment_inner_tabs
   :align: center

   Рисунок 2. Вложенные вкладки в Microenvironment.

Чтобы открыть любую вкладку, нужно нажать на нее ЛКМ.

Далее отдельно разберем работу с каждой из вкладок.

.. _Physicell_microenvironment_Domain:

Свойства сетки (Domain)
-----------------------

Во вкладке **Domain** описывается пространство внешней среды, которое задается прямоугольной сеткой.

В этой вкладке можно редактировать следующие параметры :ref:`(Рисунок 3) <Physicell_microenvironment_Pic.3>`:

- **Xmin**: минимальное значение координаты по оси X,
- **Ymin**: минимальное значение координаты по оси Y,
- **Zmin**: минимальное значение координаты по оси Z,
- **Xmax**: максимальное значение координаты по оси X,
- **Ymax**: максимальное значение координаты по оси Y,
- **Zmax**: максимальное значение координаты по оси Z,
- **dx**: шаг сетки по оси X,
- **dy**: шаг сетки по оси Y,
- **dz**: шаг сетки по оси Z,
- **Use 2D**: отметьте ☑, если хотите, чтобы пространство внешней среды ограничивалось двумя измерениями (оси X и Y).

.. note::
   Параметры Zmin, Zmax и dz доступны для редактирования, только если не выбрано Use 2D.

.. _Physicell_microenvironment_Pic.3:

.. figure:: images/Physicell/Physicell_microenvironment/Domain_menu.png
   :width: 100%
   :alt: Domain_menu
   :align: center

   Рисунок 3. Меню редактирования пространства внешней среды модели.

Чтобы задать значение любого параметра, нужно нажать ЛКМ справа от соответствующей иконки и вписать собственное значение.

Пример 2D-сетки с параметрами Xmin = -500, Xmax = 500, dx = 100, Ymin = -500, Ymax = 500, dy = 100 представлен :ref:`на рисунке 4 <Physicell_microenvironment_Pic.4>`.

.. _Physicell_microenvironment_Pic.4:

.. figure:: images/Physicell/Physicell_microenvironment/microenvironment_domain.png
   :width: 100%
   :alt: microenvironment_domain
   :align: center

   Рисунок 4. Пример 2D-сетки внешней среды.

.. _Physicell_microenvironment_Substrates:

Вещества (Substrates)
---------------------

Во вкладке **Substrates** в табличной форме приведен список всех веществ в модели вместе с их свойствами :ref:`(Рисунок 5) <Physicell_microenvironment_Pic.5>`. 

.. _Physicell_microenvironment_Pic.5:

.. figure:: images/Physicell/Physicell_microenvironment/Substrates_menu.png
   :width: 100%
   :alt: Substrates_menu
   :align: center

   Рисунок 5. Список всех веществ в модели с их свойствами.

На данной вкладке можно редактировать все свойства веществ:

- **Name**: название субстрата,
- **Initial condition**: исходное количество вещества в каждой :ref:`ячейке среды <Physicell_microenvironment_Domain>`,
- **Decay rate**: скорость разложения вещества в среде,
- **Diffusion coefficient**: скорость диффузии вещества в среде,
- **X min**: :raw-html:`граничное условие для концентрации вещества на границе среды X = X<sub>min</sub>`,
- **X max**: :raw-html:`граничное условие для концентрации вещества на границе среды X = X<sub>max</sub>`,
- **Y min**: :raw-html:`граничное условие для концентрации вещества на границе среды Y = Y<sub>min</sub>`,
- **Y max**: :raw-html:`граничное условие для концентрации вещества на границе среды Y = Y<sub>max</sub>`,
- **Z min**: :raw-html:`граничное условие для концентрации вещества на границе среды Z = Z<sub>min</sub>`,
- **Z max**: :raw-html:`граничное условие для концентрации вещества на границе среды Z = Z<sub>max</sub>`.

Чтобы задать значение любого параметра, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение.

Также свойства веществ можно настраивать напрямую на диаграмме: либо при их :ref:`создании <Physicell_model_development_Substrate_creation>`, либо :ref:`редактируя <Physicell_model_development_Additional_properties>` уже созданные.

.. note::
   Удалять и добавлять новые вещества на данной вкладке нельзя.

На данной вкладке можно сортировать вещества по значениям любой из их характеристик. Для этого нужно нажать ЛКМ на название того стобца, по значениям которого вы хотите их отсортировать :ref:`(Рисунок 6) <Physicell_microenvironment_Pic.6>`.

.. _Physicell_microenvironment_Pic.6:

.. figure:: images/Physicell/Physicell_microenvironment/Substrates_sorting.png
   :width: 100%
   :alt: Substrates_sorting
   :align: center

   Рисунок 6. Сортировка веществ по значениям одной из их характеристик (показано на примере Decay rate).

После этого рядом с названием выбранной характеристики появится значок |icon_increase_sorting|, обозначающий сортировку от наименьшего к наибольшему. Чтобы отсортировать от наибольшего к наименьшему, нужно нажать ЛКМ на название этой же характеристики еще раз, после чего рядом с ней появится значок |icon_decrease_sorting|.

Также можно настраивать размер каждой колонки. Для этого нужно:

- навести курсор на границу любых двух столбцов,
- зажать ЛКМ,
- передвинуть курсор в новое место таблицы,
- отпустить ЛКМ :ref:`(Рисунок 7) <Physicell_microenvironment_Pic.7>`.

.. _Physicell_microenvironment_Pic.7:

.. figure:: images/Physicell/Physicell_microenvironment/Column_edit.png
   :width: 100%
   :alt: Column_edit
   :align: center

   Рисунок 7. Изменение ширины столбцов.

Типы клеток (Cell types)
------------------------

Во вкладке **Cell types** в табличной форме приведен список всех типов клеток в модели вместе с их свойствами :ref:`(Рисунок 8) <Physicell_microenvironment_Pic.8>`.

.. _Physicell_microenvironment_Pic.8:

.. figure:: images/Physicell/Physicell_microenvironment/Cell_types_menu.png
   :width: 100%
   :alt: Cell_types_menu
   :align: center

   Рисунок 8. Список всех типов клеток в модели с их свойствами.

На данной вкладке можно редактировать все свойства клеток:

- **Name**: название типа клеток,
- **Initial number**: исходное количество клеток данного типа,
- **Color**: цвет, с помощью которого клетки данного типа будут отображаться при симуляции модели,
- **Comment**: можете оставить любые комментарии для клеток данного типа.

Чтобы задать значение любого параметра, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение.

Чтобы выбрать значение параметра **Color**, нужно нажать ЛКМ в ячейку строки под этим заголовком и из раскрывающегося списка выбрать нужный цвет :ref:`(Рисунок 9) <Physicell_microenvironment_Pic.9>`.

.. _Physicell_microenvironment_Pic.9:

.. figure:: images/Physicell/Physicell_microenvironment/Cell_types_color.png
   :width: 100%
   :alt: Cell_types_color
   :align: center

   Рисунок 9. Изменение значения параметра Color.

Чтобы более детально настроить цвет клеток, нужно в конце раскрывающегося списка под полем **Color** выбрать **more colors...** :ref:`(Рисунок 10A) <Physicell_microenvironment_Pic.10>` и в появившемся окне задать нужный цвет :ref:`(Рисунок 10Б) <Physicell_microenvironment_Pic.10>`.

.. _Physicell_microenvironment_Pic.10:

.. figure:: images/Physicell/Physicell_microenvironment/Cell_types_more_colors.png
   :width: 100%
   :alt: Cell_types_more_colors
   :align: center

   Рисунок 10. Выберите more colors (А) для более детальной настройки цвета клеток (Б).

Также свойства клеток можно настраивать напрямую на диаграмме: либо при их :ref:`создании <Physicell_model_development_Cell_creation>`, либо :ref:`редактируя <Physicell_model_development_Additional_properties>` уже созданные.

.. note::
   Удалять и добавлять новые типы клеток на данной вкладке нельзя.

Сортировка типов клеток по значениям какого-либо из их признаков, а также изменение размеров любой колонки таблицы со всеми клетками выполняется также, как и с :ref:`веществами <Physicell_microenvironment_Substrates>`.

События (Events)
----------------

Во вкладке **Events** в табличной форме приведен список всех событий модели вместе с их настройками :ref:`(Рисунок 11) <Physicell_microenvironment_Pic.11>`.

.. _Physicell_microenvironment_Pic.11:

.. figure:: images/Physicell/Physicell_microenvironment/Events_menu.png
   :width: 100%
   :alt: Events_menu
   :align: center

   Рисунок 11. Список всех событий модели с их настройками.

На данной вкладке можно редактировать все настройки событий:

- **Name**: название события,
- **Execution time**: модельное время, при достижении которого срабатывает событие,
- **Custom Execution code**: выберите ☑, чтобы задать путь до Java-кода, который выполнится при срабатывании события,
- **Execution code**: путь до Java-кода, который выполняется при срабатывании события,
- **Comment**: комментарий,
- **Show code**: выберите ☑, если хотите полностью показывать код на диаграмме модели,
- **Format code**: выберите ☑, если хотите форматировать показываемый на диаграмме модели код.

Чтобы задать значение любого параметра, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение, указать путь до нужного файла или отметить ☑.

Также настройки событий можно редактировать напрямую на диаграмме: либо при их :ref:`создании <Physicell_model_development_Event_creation>`, либо :ref:`редактируя <Physicell_model_development_Additional_properties>` уже созданные.

.. note::
   Удалять и добавлять новые события на данной вкладке нельзя.

Сортировка событий по значениям какой-либо из их настроек, а также изменение размеров любой колонки таблицы со всеми событиями выполняется также, как и с :ref:`веществами <Physicell_microenvironment_Substrates>`.

Пользовательские параметры модели (User Parameters)
---------------------------------------------------

Пользовательские параметры модели могут быть добавлены для использования в пользовательском Java-коде, например, при генерации начального расположения клеток, срабатывания событий или в коде, описывающем поведение отдельных клеток.

Начальное расположение клеток (Initial Condition)
-------------------------------------------------

После нажатия на вкладку **Initial Condition** на панели свойств справа у вас появится меню, в котором нужно поставить ☑ напротив |icon_option| **Custom condition**, если вы хотите задать определенное начальное расположение клеток :ref:`(Рисунок 12) <Physicell_microenvironment_Pic.12>`.

.. _Physicell_microenvironment_Pic.12:

.. figure:: images/Physicell/Physicell_microenvironment/Initial_condition_menu.png
   :width: 100%
   :alt: Initial_condition_menu
   :align: center

   Рисунок 12. Настройка для указания начального расположения клеток.

Если вы не хотите настраивать определенное начальное расположение клеток (хотите оставить случайное расположение), то оставьте вкладку **Initial Condition** без изменений.

При выборе ☑ напротив |icon_option| **Custom condition** у вас появится меню, в котором можно настроить 2 параметра :ref:`(Рисунок 13) <Physicell_microenvironment_Pic.13>`:

- |icon_option| **Custom Java code**: путь до Java-кода в репозитории, описывающего начальное расположение клеток в модели,
- |icon_option| **Custom table**: путь до таблицы в репозитории, описывающей начальное расположение клеток в модели.

.. _Physicell_microenvironment_Pic.13:

.. figure:: images/Physicell/Physicell_microenvironment/Initial_condition_parameters.png
   :width: 100%
   :alt: Initial_condition_parameters
   :align: center

   Рисунок 13. Параметры Custom Java code и Custom table для указания определенного начального расположения клеток.

Чтобы указать путь до Java-кода или таблицы, нужно нажать ЛКМ на |icon_Java_code| **(select element)** или |icon_table| **(select element)**, соответственно, и в появившемся окне выбрать нужный файл в репозитории.

.. warning::
   Нельзя одновременно указать и Java-код и таблицу, нужно указать только что-то одно.

.. _Physicell_microenvironment_Model_Report:

Отчет по модели (Model Report)
------------------------------

После нажатия на вкладку **Model Report** на панели свойств справа у вас появится меню, в котором можно редактировать следующие параметры :ref:`(Рисунок 14) <Physicell_microenvironment_Pic.14>`:

- |icon_option| **Custom report**: поставьте ☑, если хотите задать Java-код, по которому будет создаваться отчет по модели в табличной форме,
- |icon_option| **Custom global report**: поставьте ☑, если хотите задать Java-код, который будет определять :ref:`вывод логов в консль во время симуляции модели <Physicell_simulation_Log_Model_report>`,
- |icon_option| **Custom visualizer**: поставьте ☑, если хотите задать Java-код, по которому будет изменяться расцветка клеток при симуляции модели.

.. - |icon_option| **Cell Type Properties**: настройка расцветки клеток в зависимости от различных сигналов (рассмотрено далее).
.. _Physicell_microenvironment_Pic.14:

.. figure:: images/Physicell/Physicell_microenvironment/Model_report_menu.png
   :width: 100%
   :alt: Model_report_menu
   :align: center

   Рисунок 14. Меню вкладки Model Report.

При указании ☑ напротив |icon_option| **Custom report**, |icon_option| **Custom global report** или |icon_option| **Custom visualizer** ниже выбранного поля появится новое поле |icon_option| **Report**, |icon_option| **Global report** или |icon_option| **Visualizer**, соответственно. Напротив этих полей можно нажать ЛКМ на |icon_Java_code| **(select element)**, а затем в появившемся окне указать путь до нужного Java-кода в репозитории :ref:`(Рисунок 15) <Physicell_microenvironment_Pic.15>`.

.. _Physicell_microenvironment_Pic.15:

.. figure:: images/Physicell/Physicell_microenvironment/Choose_appropriate_Java_code.png
   :width: 100%
   :alt: Choose_appropriate_Java_code
   :align: center

   Рисунок 15. Выбор нужного Java-кода (показано на примере Custom report).

.. Илья Николаевич сказал, что это он уберет, т.к. это дублирует содержимое вложенной вкладки Visualizer во вкладке microenvironment  
   Чтобы добавить настройку расцветки одного типа клеток, нужно:

   - нажать ЛКМ на строку с |icon_option| **Cell Type Properties**,
   - нажать ЛКМ на иконку |icon_add_new| :ref:`(Рисунок 19) <Physicell_microenvironment_Pic.19>`.

   .. _Physicell_microenvironment_Pic.19:

   .. figure:: images/Physicell/Physicell_microenvironment/Add_cell_type_property.png
      :width: 100%
      :alt: Add_cell_type_property
      :align: center

      Рисунок 19. Добавление настройки расцветки клеток.

   После добавления настройки расцветки у вас появится вкладка с ее порядковым номером (начиная с [0]). Таким же образом можно добавить сколько угодно настроек расцветки. 

   Раскрыв эту вкладку, можно увидеть доступные для редактирования параметры :ref:`(Рисунок 20) <Physicell_microenvironment_Pic.20>`:

   - **Cell Type**: тип клеток,
   - **Priority**: приоритет,
   - **Color type**: тип цвета,
   - **Signal**: сиганл,
   - **Color 1**: цвет 1,
   - **Color 2**: цвет 2,
   - **Min value**: минимальное значение,
   - **Max value**: максимальное значение.

   .. _Physicell_microenvironment_Pic.20:

   .. figure:: images/Physicell/Physicell_microenvironment/Cell_type_properties_parameters.png
      :width: 100%
      :alt: Cell_type_properties_parameters
      :align: center

      Рисунок 20. Параметры настройки расцветки, доступные для редактирования.

   В поле справа от |icon_option| **Cell Type** из расурывающегося списка нужно выбрать тип клеток, расцветку которой мы хотим настроить.

.. _Physicell_microenvironment_Visualizer:

Визуализация клеток (Visualizer)
--------------------------------

.. warning::
   Перед редактированием этой вкладки сначала необходимо настроить вкладку :ref:`Color schemes <Physicell_microenvironment_Color_schemes>`.

В этом разделе задаются условия, по которым к клетке применяются те или иные цветовые схемы, заданные во вкладке :ref:`Color schemes <Physicell_microenvironment_Color_schemes>`.

.. note::
   Также эти условия можно задавать через Java-код во вкладке :ref:`Model Report <Physicell_microenvironment_Model_Report>`, выбрав опцию **Custom visualizer** и указав путь в репозитории до нужного файла.

Для добавления и удаления условий применения цветовых схем используются кнопки |icon_plus| и |icon_minus|, соответственно (также как и в случае с самими :ref:`цветовыми схемами <Physicell_microenvironment_Color_schemes>`).

Для каждого условия можно настроить следующие параметры :ref:`(Рисунок 16) <Physicell_microenvironment_Pic.16>`:

- **Cell Type**: тип клеток, к которому будет применяться условие,
- **Priority**: приотритет применения данного условия,
- **Color type**: правило применения цветовой схемы,
- **Signal**: свойство клетки, значения которого применяются в условии,
- **Color 1**: 1-ая цветовая схема,
- **Color 2**: 2-ая цветовая схема,
- **Min value**: минимальное значение выбранного свойства клетки (Signal),
- **Max value**: максимальное значение выбранного свойства клетки (Signal).

.. _Physicell_microenvironment_Pic.16:

.. figure:: images/Physicell/Physicell_microenvironment/Add_new_color_scheme_condition.png
   :width: 100%
   :alt: Add_new_color_scheme_condition
   :align: center

   Рисунок 16. Настройка условия применения цветовых схем.

Значения полей **Cell Type**, **Color type**, **Signal**, **Color 1** и **Color 2** выбираются из раскрывающихся списков.

Чтобы задать значений полей **Priority**, **Min value** и **Max value**, нужно нажать ЛКМ под соответствующим заголовком и вписать собственное значение.

Особое внимание следует уделить правилам применения цветовых схем (**Color type**). Всего существует 4 таких правила:

- **Fixed color**: всегда применяется только одна цветовая схема, заданная в поле Color 1 (:raw-html:`<span style="color: red;">поле Color 2 при выборе такого правила становится неактивным</span>`),
- **Gradient**: цвет клетки изменяется по градиенту от 1-ой цветовой схемы (Color 1) ко 2-ой (Color 2) в зависимости от значения выбранного свойства клетки (Signal) относительно минимума (Min value) и максимума (Max value),
- **Larger than max**: если значение свойства клетки (Siganl) больше, чем максимум (Max value), то к клетке применяется 1-ая цветовая схема (Color 1); во всех остальных случаях применяется 2-ая цветовая схема (Color 2),
- **Smaller than min**: если значение свойства клетки (Siganl) меньше, чем минимум (Min value), то к клетке применяется 1-ая цветовая схема (Color 1); во всех остальных случаях применяется 2-ая цветовая схема (Color 2).

.. note::
   Поле **Priority** используется только для правил *Larger than max* и *Smaller than min*.
   
   Если в какой-то момент времени к одному и тому же типу клеток применяется одновременно несколько условий с такими типами правил, то будет выполняться то из них, которое имеет наименьшее значение в поле Priority.

В :ref:`таблице 1 <Physicell_microenvironment_Tbl.1>` показано, как работают разные правила применения цветовых схем на примере со следующими настройками:

- **Color 1**: |icon_blue_circle|,
- **Color 2**: |icon_red_circle|,
- **Min value**: 10,
- **Max value**: 100.

.. _Physicell_microenvironment_Tbl.1:

.. list-table:: Таблица 1. Пример работы различных правил применения цветовых схем
   :header-rows: 1

   * - Правило
     - Signal = 0
     - Signal = 50
     - Signal = 200

   * - Fixed color
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
   * - Gradient
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
     - .. image:: images/icons/Physicell/blue_red_gradient_circle.png
          :alt: сине-красный градиентный круг
     - .. image:: images/icons/Physicell/red_circle.png
          :alt: красный круг
   * - Larger than max
     - .. image:: images/icons/Physicell/red_circle.png
          :alt: красный круг
     - .. image:: images/icons/Physicell/red_circle.png
          :alt: красный круг
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
   * - Smaller than min
     - .. image:: images/icons/Physicell/blue_circle.png
          :alt: синий круг
     - .. image:: images/icons/Physicell/red_circle.png
          :alt: красный круг
     - .. image:: images/icons/Physicell/red_circle.png
          :alt: красный круг

.. _Physicell_microenvironment_Color_schemes:

Цветовые схемы (Color schemes)
------------------------------

.. warning::
   Пока мы пропустим вкладки **Model Report** и **Visualizer**, потому что перед их редактированием необходимо настроить параметры вкладки **Color schemes**.

Что такое цветовые схемы?
~~~~~~~~~~~~~~~~~~~~~~~~~

Цветовые схемы позволяют настраивать отрисовку клеток одного и того же типа в различных условиях.

Для понимания, в каких случаях может потребоваться использование цветовых схем, приведем пример.

.. code-block:: text
   :caption: Пример использования цветовых схем

   Предположим, вы моделируете заражение клеток вирусом.

   Клетки могут быть как здоровыми (не содержат внутри себя вирус), так и больными
   (содержат внутри себя вирус).

   В то же время больные клетки могут содержать различное количество вирусных частиц
   (10, 100, 1000 и т.д.).

   В таком случае, для визуализации результатов симуляции удобно использовать несколько цветовых схем,
   чтобы сразу было понятно, какие клетки здоровые, а какие больные и насколько.

   Например, здоровые клетки (0 вирусных частиц) можно отображать синим цветом, а больные
   (> 0 вирусных частиц) - желтым.
   Также в зависимости от количества вирусных частиц внутри клетки можно отрисовывать их с помощью
   различных оттенков желтого:

   - от 1 до 10 - светло-желтый,
   - от 10 до 100 - желтый,
   - от 100 до 1000 - ярко желтый,
   - > 1000 - темно-желтый.

   С использованием таких цветовых схем при просмотре результатов симуляции модели можно
   будет сразу визуально оценить интенсивность распространения вируса в клетках.

Настройка цветовых схем в модели
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

После нажатия на вкладку **Color schemes** на панели свойств справа у вас появится меню, в котором, нажав ЛКМ на иконку |icon_plus|, можно добавить новую цветовую схему :ref:`(Рисунок 17) <Physicell_microenvironment_Pic.17>`.

.. _Physicell_microenvironment_Pic.17:

.. figure:: images/Physicell/Physicell_microenvironment/Add_new_color_scheme.png
   :width: 100%
   :alt: Add_new_color_scheme
   :align: center

   Рисунок 17. Добавление новой цветовой схемы.

После этого у вас появится строка, соответствующая одной цветовой схеме :ref:`(Рисунок 18) <Physicell_microenvironment_Pic.18>`.

.. _Physicell_microenvironment_Pic.18:

.. figure:: images/Physicell/Physicell_microenvironment/Color_scheme_string.png
   :width: 100%
   :alt: Color_scheme_string
   :align: center

   Рисунок 18. Одной цветовой схеме соответствует одна строка.

Таким образом можно добавить сколько угодно цветовых схем.

В каждой цветовой схеме можно настраивать следующие параметры:

- **Name**: название цветовой схемы,
- **Inner Color**: цвет, с помощью которого отрисовывается внутреннее содержимое клетки,
- **Has border**: отметьте ☑, если хотите отрисовывать контур клетки,
- **Border color**: цвет, с помощью которого отрисовывается контур клетки (:raw-html:`<span style="color: red;">не редактируется, если не выбрано свойство Has border</span>`),
- **Has core**: отметьте ☑, если хотите отрисовывать ядро в клетке,
- **Core color**: цвет, с помощью которого отрисовывается внутреннее содержимое ядра клетки (:raw-html:`<span style="color: red;">не редактируется, если не выбрано свойство Has core</span>`),
- **Core border Color**: цвет, с помощью которого отрисовывается контур ядра клетки (:raw-html:`<span style="color: red;">не редактируется, если не выбрано свойство Has core</span>`).

Чтобы задать значение любого параметра, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение, отметить ☑ или выбрать нужный цвет из раскрывающегося списка.

Для удаления цветовой схемы нужно:

- нажать ЛКМ на строку, соответствующую определенной цветовой схеме,
- нажать ЛКМ на значок |icon_minus| :ref:`(Рисунок 19) <Physicell_microenvironment_Pic.19>`.

.. _Physicell_microenvironment_Pic.19:

.. figure:: images/Physicell/Physicell_microenvironment/Delete_color_scheme.png
   :width: 100%
   :alt: Delete_color_scheme
   :align: center

   Рисунок 19. Удаление цветовой схемы.

Другие параметры модели (Model Options)
---------------------------------------

Вкладка **Model Options** содержит все оставшиеся параметры модели, которые нельзя отнести ни к одной из рассмотренных выше вкладок.

После нажатия на эту вкладку на панели свойств справа у вас появится меню, в котором можно редактировать следующие параметры модели :ref:`(Рисунок 20) <Physicell_microenvironment_Pic.20>`:

- **Disable automated spring adhesion**: поставьте ☑, если хотите включить автоматическую адгезию клеток.

.. _Physicell_microenvironment_Pic.20:

.. figure:: images/Physicell/Physicell_microenvironment/Model_options_menu.png
   :width: 100%
   :alt: Model_options_menu
   :align: center

   Рисунок 20. Меню редактирования оставшихся параметров модели.