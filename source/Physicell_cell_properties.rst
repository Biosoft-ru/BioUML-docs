Свойства клеток
===============

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
           text-align: left;
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

.. |icon_clue| image:: /images/icons/Physicell/clue.png
.. |icon_opened_clue| image:: /images/icons/Physicell/opened_clue.png
.. |icon_option| image:: /images/icons/option.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png
.. |icon_chemotaxis| image:: /images/icons/Physicell/chemotaxis.png
.. |icon_secretion| image:: /images/icons/Physicell/secretion.png
.. |icon_interaction| image:: /images/icons/Physicell/interaction.png
.. |icon_transformation| image:: /images/icons/Physicell/transformation.png
.. |icon_plus| image:: /images/icons/Physicell/plus.png
.. |icon_minus| image:: /images/icons/Physicell/minus.png

У каждого типа клеток в модели есть определенный набор свойств. Чтобы настроить эти свойства, нужно:

1. выбрать на диаграмме клетки, совйства которых вы хотите изменить,
2. в правом нижнем окошке нажать ЛКМ на вкладку **Cell Types** :ref:`(Рисунок 1) <Physicell_cell_properties_Pic.1>`.

.. _Physicell_cell_properties_Pic.1:

.. figure:: images/Physicell/Physicell_cell_properties/Cell_Types_button.png
   :width: 100%
   :alt: Cell_Types_buttton
   :align: center

   Рисунок 1. Открытие вкладки редактирования свойств клетки.

После этого в правом нижнем окошке у вас появится перечень свойств клетки :ref:`(Рисунок 2) <Physicell_cell_properties_Pic.2>`:

- **Cycle**: жизненный цикл клетки,
- **Division**: тип деления клетки,
- **Death**: тип смерти клетки,
- **Volume**: объем клетки и ее компартментов,
- **Mechanics**: механические свойства клетки,
- **Integrity**: целостность и повреждения клетки,
- **Motility**: подвижность клетки,
- **Secretion**: секреция/потребление клеткой,
- **Interactions**: межклеточные взаимодействия,
- **Transformations**: трансформация клетки,
- **Custom data**: пользовательские данные клетки,
- **Functions**: функции, описывающие поведение клетки,
- **Intracellular**: внутриклеточная модель клетки,
- **Rules**: правила, описывающие поведение клетки,
- **Initial distribution**: начальное распределение характеристик клетки.

.. _Physicell_cell_properties_Pic.2:

.. figure:: images/Physicell/Physicell_cell_properties/Cell_properties_panel.png
   :width: 100%
   :alt: Cell_properties_panel
   :align: center

   Рисунок 2. Панель свойств клеток.

Чтобы перейти к редактированию того или иного свойства клетки, необходимо нажать ЛКМ на соответствующую вкладку в панели свойств.

Далее мы рассмотрим каждое из свойст подробно.

.. _Physicell_cell_properties_Live_cycle:

Жизненный цикл клетки (Cycle)
-----------------------------

После нажатия на вкладку **Cycle** на панели свойств справа у вас появится меню, в котором можно изменять параметры жизненного цикла клетки :ref:`(Рисунок 3) <Physicell_cell_properties_Pic.3>`.

.. _Physicell_cell_properties_Pic.3:

.. figure:: images/Physicell/Physicell_cell_properties/Cycle_menu.png
   :width: 100%
   :alt: Cycle_menu
   :align: center

   Рисунок 3. Меню редактирования параметров жизненного цикла клетки.

В этом меню можно редактировать следующие параметры жизненного цикла клетки:

Название жизненного цикла клетки (Name)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

При нажатии слева от кнопки |icon_option| **Name** раскрывается список, в котором можно выбрать тип жизненного цикла клетки :ref:`(Рисунок 4) <Physicell_cell_properties_Pic.4>`:

- **Ki67 (basic)**: жизненный цикл, состоящий из двух фаз - :raw-html:`«<u>Ki67-</u>» и «<u>Ki67+</u>»`,
- **Ki67 (advanced**: жизненный цикл, состоящий из трех фаз - :raw-html:`«<u>Ki67-</u>», «<u>Ki67+ (premitotic)</u>» и «<u>Ki67+ (postmitotic)</u>»`,
- **Live**: простейший жизненный цикл, состоящий всего из одной фазы с условным названием :raw-html:`«<u>Live</u>»`,
- **Flow cytometry model (basic)**: жизненный цикл, состоящий из трех фаз - :raw-html:`«<u>G0/G1</u>», «<u>S</u>» и «<u>G2/M</u>»`,
- **Flow cytometry model (separated)**: жизненный цикл, состоящий из четырех фаз - :raw-html:`«<u>G0/G1</u>», «<u>S</u>», «<u>G2</u>» и «<u>M</u>»`,
- **Custom**: пользовательский жизненный цикл.

.. _Physicell_cell_properties_Pic.4:

.. figure:: images/Physicell/Physicell_cell_properties/Cycle_name.png
   :width: 100%
   :alt: Cycle_name
   :align: center

   Рисунок 4. Жизненные циклы клетки.

При выборе **Custom...** справа от поля |icon_option| **Custom cycle** нужно будет указать путь к модели, описывающий жизненный цикл клетки :ref:`(Рисунок 5) <Physicell_cell_properties_Pic.5>`.

.. _Physicell_cell_properties_Pic.5:

.. figure:: images/Physicell/Physicell_cell_properties/Custom_cycle.png
   :width: 100%
   :alt: Custom_cycle
   :align: center

   Рисунок 5. Указание пользовательского жизненного цикла клетки.

.. _Phases_and_transitions:

Фазы цикла (Phases) и переходы между ними (Transitions)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

При выборе определенного цикла автоматически изменяются вкладки поля **Phases** (фазы цикла) и **Transitions** (переходы между фазами цикла) :ref:`(Рисунок 6) <Physicell_cell_properties_Pic.6>`.

.. _Physicell_cell_properties_Pic.6:

.. figure:: images/Physicell/Physicell_cell_properties/Cycle_phases_transitions.png
   :width: 100%
   :alt: Cycle_phases_transitions
   :align: center

   Рисунок 6. Автоматическое изменение вкладок полей Phases и Transitions при выборе определенного цикла в поле Name.

Чтобы открыть любую вкладку полей **Phases** или **Transitions**, нужно нажать ЛКМ на значок |icon_clue| слева от вкладки :ref:`(Рисунок 7А) <Physicell_cell_properties_Pic.7>`. Чтобы закрыть вкладку, нужно нажать ЛКМ на значок |icon_opened_clue| слева от вкладки :ref:`(Рисунок 7Б) <Physicell_cell_properties_Pic.7>`.

.. _Physicell_cell_properties_Pic.7:

.. figure:: images/Physicell/Physicell_cell_properties/Open_and_close_tab.png
   :width: 100%
   :alt: Open_and_close_tab
   :align: center

   Рисунок 7. Открытие (А) и закрытие (Б) вкладок ЛКМ.

При открытии любой из вкладок поля **Phases** появляется значок |icon_option| **Division on exit**. Отметьте ☑, если хотите, чтобы клетка делилась по окончании выбранной фазы жизненного цикла :ref:`(Рисунок 8) <Physicell_cell_properties_Pic.8>`.

.. _Physicell_cell_properties_Pic.8:

.. figure:: images/Physicell/Physicell_cell_properties/Division_on_exit.png
   :width: 100%
   :alt: Division_on_exit
   :align: center

   Рисунок 8. Выбор фазы жизненного цикла клетки, по окончании которого будет происходить клеточное деление.

При открытии любой из вкладок поля Transitions появится два значка:

- |icon_option| **Rate**: скорость перехода между соответствующими фазами жизненного цикла клетки (можно изменять, нажав ЛКМ на число и вписав собственное значение),
- |icon_option| **Fixed**: отметьте ☑, если хотите, чтобы время перехода между соответствующими фазами жизненного цикла клетки было зафиксировано :ref:`(Рисунок 9) <Physicell_cell_properties_Pic.9>`.

.. note::
   При указании свойства Fixed переход между фазами жизненного цикла клетки происходит **ровно** через :math:`1/Rate` единиц времени поcле начала фазы.

   Если Fixed не указано, то переход происходит **в среднем** через :math:`1/Rate` единиц времени почле начала фазы. Моделируется это следующим образом:
   во время каждого шага агента (клетки) переход может произойти с вероятностью :math:`Rate*Phenotype \, dt`, где Phenotype dt- шаг модельного времени, с которым происходит обновление внутреннего состояния клеток (задается при настройках :ref:`симуляции модели <Physicell_simulation>`).

.. _Physicell_cell_properties_Pic.9:

.. figure:: images/Physicell/Physicell_cell_properties/Transitions_rate_fixed.png
   :width: 100%
   :alt: Transitions_rate_fixed
   :align: center

   Рисунок 9. Настройка переходов между всеми фазами жизненного цикла клетки.

Редактирование фаз и переходов между ними
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Чтобы добавить новую фазу или переход в жизненный цикл клетки нужно:

- нажать ЛКМ на вкладку |icon_option| **Phases** или |icon_option| **Transitions**,
- нажать ЛКМ на иконку |icon_add_new| :ref:`(Рисунок 10) <Physicell_cell_properties_Pic.10>`.

.. _Physicell_cell_properties_Pic.10:

.. figure:: images/Physicell/Physicell_cell_properties/New_phase_or_transition.png
   :width: 100%
   :alt: New_phase_or_transition
   :align: center

   Рисунок 10. Добавление новой фазы или перехода в жизненный цикл клетки (показано на примере фазы).

После этого в соответствующем разделе у вас появится новая фаза или переход :ref:`(Рисунок 11) <Physicell_cell_properties_Pic.11>`.

.. _Physicell_cell_properties_Pic.11:

.. figure:: images/Physicell/Physicell_cell_properties/New_phase.png
   :width: 100%
   :alt: New_phase
   :align: center

   Рисунок 11. Новая фаза жизненного цикла клетки.

Кроме этого возможны и другие действия с фазами и переходами. Для их отображения нужно нажать ЛКМ на любую фазу или переход, и после этого сверху появится панель с возможными действиями :ref:`(Рисунок 12) <Physicell_cell_properties_Pic.12>`.

.. _Physicell_cell_properties_Pic.12:

.. figure:: images/Physicell/Physicell_cell_properties/Actions_with_phases_or_transitions.png
   :width: 100%
   :alt: Actions_with_phases_or_transitions
   :align: center

   Рисунок 12. Панель возможных действий с фазами или переходами.

Описание каждого из этих действий приведено в :ref:`таблице 1 <Physicell_cell_properties_Tbl.1>`.

.. _Physicell_cell_properties_Tbl.1:

.. list-table:: Таблица 1. Элементы панели управления, используемой при работе с фазами и переходами жизненного цикла клетки
   :header-rows: 1

   * - Обозначние
     - Описание

   * - .. image:: images/icons/Physicell/delete_phase_or_transition.png
          :alt: удаление фазы или перехода
     - Удаление выбранной фазы или перехода
   * - .. image:: images/icons/Physicell/insert_before_phase_or_transition.png
          :alt: вставить перед фазой или переходом
     - Вставить новую фазу или переход перед выбранной
   * - .. image:: images/icons/Physicell/insert_after_phase_or_transition.png
          :alt: вставить после фазы или перехода
     - Вставить новую фазу или переход после выбранной
   * - .. image:: images/icons/Physicell/move_up_phase_or_transition.png
          :alt: переместить фазу или переход вверх
     - Переместить выбранную фазу или переход выше
   * - .. image:: images/icons/Physicell/move_down_phase_or_transition.png
          :alt: переместить фазу или переход вниз
     - Переместить выбранную фазу или переход ниже

Тип деления клетки (Division)
-----------------------------

После нажатия на вкладку **Division** на панели свойств справа у вас появится меню, в котором можно изменять параметры деления клетки :ref:`(Рисунок 13) <Physicell_cell_properties_Pic.13>`.

.. _Physicell_cell_properties_Pic.13:

.. figure:: images/Physicell/Physicell_cell_properties/Division_menu.png
   :width: 100%
   :alt: Division_menu
   :align: center

   Рисунок 13. Меню редактирования параметров деления клетки.

Если деление выбранного вами типа клеток должно происходить асимметрично, то отметьте ☑ справа от поля |icon_option| **Asymmetric division**.

.. note::
   Асимметричное деление - деление, при котором из клетки одного типа могут образоваться клетки другого типа.

При выборе этого пункта ниже у вас появится поле **Probabilities** (вероятности появления клеток другого типа) :ref:`(Рисунок 14) <Physicell_cell_properties_Pic.14>`.

.. _Physicell_cell_properties_Pic.14:

.. figure:: images/Physicell/Physicell_cell_properties/Probabilities.png
   :width: 100%
   :alt: Probabilities
   :align: center

   Рисунок 14. Поле Probabilities (вероятности) при асимметричном делении клеток.

Чтобы добавить вероятность появления клетки другого типа при делении, нужно:

- нажать ЛКМ на строку с полем **Probabilities**,
- нажать ЛКМ на значок |icon_add_new| :ref:`(Рисунок 15) <Physicell_cell_properties_Pic.15>`.

.. _Physicell_cell_properties_Pic.15:

.. figure:: images/Physicell/Physicell_cell_properties/Add_new_probability.png
   :width: 100%
   :alt: Add_new_probability
   :align: center

   Рисунок 15. Добавление вероятности появления другого типа клеток при делении родительской клетки.

Таким образом можно добавить сколько угодно вероятностей для выбранного типа клеток (при открытии вкладки **Probabilities** каждая вероятность будет иметь свой порядковый номер, начиная с [0]).

Для работы с уже существующими вероятностями используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Для каждой вероятности можно настраивать 2 параметра :ref:`(Рисунок 16) <Physicell_cell_properties_Pic.16>`:

- **Cell type**: тип клеток, который может получиться при делении родительской клетки,
- **Probability**: вероятность появления клетки другого типа (выбранного в Cell type) при делении родительской клетки.

.. _Physicell_cell_properties_Pic.16:

.. figure:: images/Physicell/Physicell_cell_properties/Probability_for_cell_type.png
   :width: 100%
   :alt: Probability_for_cell_type
   :align: center

   Рисунок 16. Настройка параметров Cell type и Probability.

Чтобы изменить значение каждого из этих параметров, нужно нажать ЛКМ слева от соответствующего параметра и вписать свое значение.

.. warning::
   При асимметричном делении сумма всех Probability должна равняться 1.

Ниже еще раз объясним, как работает асимметричное деление, на примере.

.. code-block:: text
   :caption: Пример настройки асимметричного деления клетки

   Probabilities
   ├── [0]
   │   ├── Cell type: Нейрон
   │   └── Probability: 0.3
   ├── [1]
   │   ├── Cell type: Эритроцит
   │   └── Probability: 0.5
   └── [2]
       ├── Cell type: Фибробласт
       └── Probability: 0.2

   Такая настройка означает, что при делении клетки выбранного нами типа может образоваться
   либо нейрон (с вероятностью 30%), либо эритроцит (с вероятностью 50%), либо фибробласт
   (с вероятностью 20%).

   Сумма всех вероятностей равна 1 (0.3 + 0.5 + 0.2)

.. _Physicell_cell_properties_Death_type:

Тип смерти клетки (Death)
-------------------------

После нажатия на вкладку **Death** на панели свойств справа у вас появится меню, в котором можно изменять параметры смерти клетки :ref:`(Рисунок 17) <Physicell_cell_properties_Pic.17>`.

.. _Physicell_cell_properties_Pic.17:

.. figure:: images/Physicell/Physicell_cell_properties/Death_menu.png
   :width: 100%
   :alt: Death_menu
   :align: center

   Рисунок 17. Меню редактирования параметров смерти клетки.

По умолчанию у клетки есть два вида смерти: **apoptosis** (апоптоз) и **necrosis** (некроз). При нажатии ЛКМ на панель **Death models** сверху появится иконка |icon_add_new|, нажав на которую можно будет добавить еще один возможный тип смерти клетки :ref:`(Рисунок 18) <Physicell_cell_properties_Pic.18>`.

.. _Physicell_cell_properties_Pic.18:

.. figure:: images/Physicell/Physicell_cell_properties/New_death.png
   :width: 100%
   :alt: New_death
   :align: center

   Рисунок 18. Добавление нового типа смерти клетки.

Выбрав конкретный тип смерти клетки можно использовать тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Раскрыв панель определенного типа клеточной смерти можно детально настроить его параметры :ref:`(Рисунок 19) <Physicell_cell_properties_Pic.19>`:

- **Rate**: начальная вероятность наступления клеточной смерти,
- **Cycle**: цикл клеточной смерти (подробно рассмотрен далее),
- **Unlysed fluid change rate**: скорость изменения объема жидкости клетки во время апоптоза или некроза,
- **Lysed fluid change rate**: скорость изменения объема жидкости клетки во время некроза (:raw-html:`<span style="color: red;">при апоптозе этот параметр равен 0</span>`),
- **Cytoplasmic biomass change rate**: скорость изменения объема цитоплазмы,
- **Nuclear biomass change rate**: скорость изменения объема ядра,
- **Calcification rate**: скорость кальцификации,
- **Relative rupture volume**: относительный объем клетки, при котором происходит разрыв мембраны,
- **Time Units**: единицы измерения времени.

.. _Physicell_cell_properties_Pic.19:

.. figure:: images/Physicell/Physicell_cell_properties/Death_parameters.png
   :width: 100%
   :alt: Death_parameters
   :align: center

   Рисунок 19. Параметры смерти клетки.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Далее разберем как настроить цикл клеточной смерти.

.. _Physicell_cell_properties_Death_cycle:

Цикл клеточной смерти (Cycle)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Чтобы настроить цикл клеточной смерти, нужно раскрыть вкладку **Cycle** определенного типа клеточной смерти :ref:`(Рисунок 20) <Physicell_cell_properties_Pic.20>`.

.. _Physicell_cell_properties_Pic.20:

.. figure:: images/Physicell/Physicell_cell_properties/Death_cycle.png
   :width: 100%
   :alt: Death_cycle
   :align: center

   Рисунок 20. Редактирование параметров цикла клеточной смерти.

После этого у вас появятся новые поля, которые можно редактировать :ref:`(Рисунок 21) <Physicell_cell_properties_Pic.21>`:

- **Name**: название цикла клеточной смерти,
- **Custom cycle**: путь к модели, описывающей пользовательский цикл клеточной смерти (необходимо указать, если в предыдущем пункте выбрано :raw-html:`«<u>Custom...</u>»`),
- **Phases**: фазы цикла клеточной смерти,
- **Transitions**: переходы между фазами цикла клеточной смерти.

.. _Physicell_cell_properties_Pic.21:

.. figure:: images/Physicell/Physicell_cell_properties/Death_cycle_parameters.png
   :width: 100%
   :alt: Death_cycle_parameters
   :align: center

   Рисунок 21. Параметры цикла клеточной смерти.

Настройка фаз и переходов происходит по тому же принципу, что и в случае :ref:`жизненного цикла клетки <Phases_and_transitions>`.

.. _Physicell_cell_properties_Volume:

Объем клетки и ее компартментов (Volume)
----------------------------------------

После нажатия на вкладку **Volume** на панели свойств справа у вас появится меню, в котором отображаются параметры объема клетки :ref:`(Рисунок 22) <Physicell_cell_properties_Pic.22>`:

- **Total volume**: общий объем клетки,
- **Fluid fraction**: доля жидкости в объеме клетки,
- **Nuclear**: объем клеточного ядра,
- **Fluid change rate**: скорость изменения количества жидкости в клетке,
- **Cytoplasmic biomass change rate**: скорость изменения объема цитоплазмы клетки,
- **Nuclear biomass change rate**: скорость изменения объема ядра клетки,
- **Calcified fraction**: кальцифицированная доля клетки,
- **Calcification rate**: скорость кальцификации клетки,
- **Relative rapture volume**: относительное значение объема клетки, при котором происходит разрыв мембраны.

.. _Physicell_cell_properties_Pic.22:

.. figure:: images/Physicell/Physicell_cell_properties/Volume_menu.png
   :width: 100%
   :alt: Volume_menu
   :align: center

   Рисунок 22. Меню редактирования параметров объема клетки.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Механические свойства клетки (Mechanics)
----------------------------------------

После нажатия на вкладку **Mechanics** на панели свойств справа у вас появится меню, в котором отображаются параметры механических свойств клетки :ref:`(Рисунок 23) <Physicell_cell_properties_Pic.23>`:

- **Cell adhesion strength**: сила межклеточной адгезии,
- **Cell repulsion strength**: сила межклеточного отталкивания,
- **Membrane adhesion strength**: сила адгезии к мембране,
- **Membrane repulsion strength**: сила отталкивания от мембраны,
- **Relative max adhesion distance**: относительно максимальная дистанция адгезии,
- **Max attachments**: максимальное количество клеток, с которыми клетка выбранного типа может иметь контакт одновременно,
- **Attachment elasticity**: коэффициент эластичности прикрепления клетки,
- **Attachment rate**: скорость прикрепления клеток,
- **Detachment rate**: скорость открепления клеток.

.. _Physicell_cell_properties_Pic.23:

.. figure:: images/Physicell/Physicell_cell_properties/Mechanics_menu.png
   :width: 100%
   :alt: Mechanics_menu
   :align: center

   Рисунок 23. Меню редактирования параметров механических свойств клетки.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Целостность и повреждения клетки (Integrity)
--------------------------------------------

После нажатия на вкладку **Integrity** на панели свойств справа у вас появится меню, в котором отображаются параметры целостности и повреждений клетки :ref:`(Рисунок 24) <Physicell_cell_properties_Pic.24>`:

- **Damage rate**: скорость повреждения клеток данного типа за 1 шаг обновления внутреннего состояния клеток (Phenotype dt; устанавливается при настройке :ref:`симуляции модели <Physicell_simulation>`),
- **Damage repair rate**: скорость "выздоровления" клетки от нанесенных повреждения.

.. note::
   Damage rate не зависит от клеток других типов, просто клетка с течением времени сама по себе повреждается.

.. _Physicell_cell_properties_Pic.24:

.. figure:: images/Physicell/Physicell_cell_properties/Integrity_menu.png
   :width: 100%
   :alt: Integrity_menu
   :align: center

   Рисунок 24. Меню редактирования параметров целостности и повреждений клетки.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Подвижность клетки (Motility)
-----------------------------

После нажатия на вкладку **Motility** на панели свойств справа у вас появится меню, в котором нужно поставить ☑ напротив |icon_option| **Is Motile**, если выбранный тип клеток должен быть подвижен :ref:`(Рисунок 25) <Physicell_cell_properties_Pic.25>`.

.. _Physicell_cell_properties_Pic.25:

.. figure:: images/Physicell/Physicell_cell_properties/Is_motile.png
   :width: 100%
   :alt: Is_motile
   :align: center

   Рисунок 25. Настройка того, будут ли клетки подвижны или нет.

Если выбранный тип клеток должен быть неподвижен, то оставьте вкладку **Motility** без изменений.

При отметке того, что клетки должны быть подвижны, у вас появится меню, в котором можно настроить параметры подвижности :ref:`(Рисунок 26) <Physicell_cell_properties_Pic.26>`.

.. _Physicell_cell_properties_Pic.26:

.. figure:: images/Physicell/Physicell_cell_properties/Motility_menu.png
   :width: 100%
   :alt: Motility_menu
   :align: center

   Рисунок 26. Меню редактирования параметров подвижности клетки.

В появившемся меню можно настроить следующие параметры:

- **Migration speed**: скорость передвижения клетки,
- **Persistence time**: время в течение которого клетка не меняет направление движения,
- **Migration bias**: определяет процент времени, в течение которого клетка движется случайно,
- **Restricted to 2D**: отметьте ☑, если клетки должны двигаться только в двух измерениях,
- **Chemotaxis**: настройка параметров хемотаксиса (рассмотрено ниже).

В примере на :ref:`рисунке 26 <Physicell_cell_properties_Pic.26>` выбранный тип клеток на диаграмме уже имеет реакцию хемотаксиса (|icon_chemotaxis|), поэтому под полем **Chemotaxis** уже располагается поле с названием субстрата (в данном случае, **Substrate**), к или от которого движется клетка. Если бы клетки на диаграмме имели несколько реакций хемотаксиса, то таких полей было бы несколько (отдельное поле для каждой реакции хемотаксиса на диаграмме).

Раскрыв вкладку с названием субстрата можно настроить чувствительность к этому субстрату :ref:`(Рисунок 27) <Physicell_cell_properties_Pic.27>`.

.. _Physicell_cell_properties_Pic.27:

.. figure:: images/Physicell/Physicell_cell_properties/Sensitivity_setting.png
   :width: 100%
   :alt: Sensitivity_setting
   :align: center

   Рисунок 27. Настройка чувствительности клетки к субстрату.

Также чувствительность клетки к субстрату можно настроить при создании или редактировании самой реакции :ref:`хемотаксиса <Physicell_model_development_Chemotaxis>` на диаграмме модели.

Для работы с уже существующими реакциями хемотаксиса клетки используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Секреция/потребление клеткой (Secretion)
----------------------------------------

После нажатия на вкладку **Secretion** на панели свойств справа у вас появится меню, в котором отображаются параметры реакций секреции и потребления клетки :ref:`(Рисунок 28) <Physicell_cell_properties_Pic.28>`.

.. _Physicell_cell_properties_Pic.28:

.. figure:: images/Physicell/Physicell_cell_properties/Secretion_menu.png
   :width: 100%
   :alt: Secretion_menu
   :align: center

   Рисунок 28. Меню редактирования параметров реакций секреции и потребления клетки.

Если выбранный тип клеток на диаграмме не имеет реакций секреции, то на вкладке **Secretion** не будет доступных для редактирования параметров.

В примере на :ref:`рисунке 28 <Physicell_cell_properties_Pic.28>` выбранный тип клеток на диаграмме уже имеет реакцию секреции (|icon_secretion|), поэтому под полем **Substrates** уже располагается поле с названием субстрата (в данном случае, **Substrate**), который клетка секретирует или потребляет. Если бы клетки на диаграмме имели несколько реакций секреции, то таких полей было бы несколько (отдельное поле для каждой реакции секреции на диаграмме).

Для каждого субстрата, который клетка секретирует или потребляет, можно настроить следующие параметры :ref:`(Рисунок 29) <Physicell_cell_properties_Pic.29>`:

- **Secretion Rate**: скорость секреции вещества,
- **Secretion Target**: значение «насыщения» при котором прекращается секреция,
- **Uptake Rate**: скорость потребления вещества,
- **Net export rate**: постоянный уровень секреции/потребления субстрата, не зависящий от объема клетки.

.. _Physicell_cell_properties_Pic.29:

.. figure:: images/Physicell/Physicell_cell_properties/Secretion_settings.png
   :width: 100%
   :alt: Secretion_settings
   :align: center

   Рисунок 29. Настройка параметров реакций секреции и потреления клетки.

Также эти параметры можно настроить при создании или редактировании самой реакции :ref:`секреции <Physicell_model_development_Secretion>` на диаграмме модели.

Для работы с уже существующими реакциями секреции клетки используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Межклеточные взаимодействия (Interactions)
------------------------------------------

После нажатия на вкладку **Interactions** на панели свойств справа у вас появится меню, в котором отображаются параметры межклеточных взаимодействий клетки :ref:`(Рисунок 30) <Physicell_cell_properties_Pic.30>`:

- **Damage rate**: интенсивность, с которой клетка атакует другие клетки при взаимодействии,
- **Damage phagocytosis rate**: интенсивность с которой клетка осуществляет фагоцитоз мертвых клеток любого типа,
- **Cell types**: типы клеток, с которыми взаимодействуют выбранные клетки (рассмотрено ниже).


.. warning::
   Не путать **Damage rate** во вкладке Interactions и **Damage rate** во вкладке Integrity.

   **Damage rate** (Interactions) - интенсивность, с которой клетка атакует ДРУГИЕ клетки при взаимодействии.

   **Damage rate** (Integrity) - интенсивность, с которой клетка САМА по себе получает повреждения (не зависит от других клеток, просто клетка как бы "изнашивается").

.. _Physicell_cell_properties_Pic.30:

.. figure:: images/Physicell/Physicell_cell_properties/Interactions_menu.png
   :width: 100%
   :alt: Interactions_menu
   :align: center

   Рисунок 30. Меню редактирования параметров межклеточных взаимодействий клетки.

В примере на :ref:`рисунке 28 <Physicell_cell_properties_Pic.28>` выбранный тип клеток на диаграмме уже имеет реакцию взаимодействия (|icon_interaction|), поэтому под полем **Cell types** уже располагается поле с названием типа клеток (в данном случае, **CellDefinition_1**), с которым клетки выранного типа взаимодействуют. Если бы таких типов клеток было несколько, то для каждого из них было бы соответствующее поле.

Для каждого типа клеток, с которым клетки выранного типа взаимодействуют, можно настроить следующие параметры :ref:`(Рисунок 31) <Physicell_cell_properties_Pic.31>`:

- **Attack rate**: интенсивность атаки,
- **Fuse rate**: интенсивность слияния двух клеток,
- **Phagocytosis rate**: интенсивность фагоцитоза.

.. _Physicell_cell_properties_Pic.31:

.. figure:: images/Physicell/Physicell_cell_properties/Interaction_settings.png
   :width: 100%
   :alt: Interaction_settings
   :align: center

   Рисунок 31. Настройка параметров межклеточных взаимодействий клетки.

Также эти параметры можно настроить при создании или редактировании самой реакции :ref:`взаимодействия <Physicell_model_development_Interaction>` на диаграмме модели.

Для работы с уже существующими реакциями межклеточных взаимодействий клетки используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Трансформация клетки (Transformations)
--------------------------------------

После нажатия на вкладку **Transformations** на панели свойств справа у вас появится меню, в котором отображаются параметры реакций трансформации клетки :ref:`(Рисунок 32) <Physicell_cell_properties_Pic.32>`.

.. _Physicell_cell_properties_Pic.32:

.. figure:: images/Physicell/Physicell_cell_properties/Transformations_menu.png
   :width: 100%
   :alt: Transformations_menu
   :align: center

   Рисунок 32. Меню редактирования параметров реакций трансформации клетки.

Если выбранный тип клеток на диаграмме не имеет реакций трансформации, то на вкладке **Transformations** не будет доступных для редактирования параметров.

В примере на :ref:`рисунке 32 <Physicell_cell_properties_Pic.32>` выбранный тип клеток на диаграмме уже имеет реакцию трансформации (|icon_transformation|), поэтому под полем **Cell types** уже располагается поле с названием типа клеток (в данном случае, **CellDefinition**), в который выбранные клетки трансформируются. Если бы клетки на диаграмме имели несколько реакций трансформации, то таких полей было бы несколько (отдельное поле для каждой реакции трансформации на диаграмме).

Для каждого типа клеток, в который выбранные клетки трансформируются, можно настроить параметр **Transformation rate**, характеризующий скорость трансформации :ref:`(Рисунок 33) <Physicell_cell_properties_Pic.33>`.

.. _Physicell_cell_properties_Pic.33:

.. figure:: images/Physicell/Physicell_cell_properties/Transformation_rate_setting.png
   :width: 100%
   :alt: Transformation_rate_setting
   :align: center

   Рисунок 33. Настройка параметра Transformation rate для каждой реакции трансформации клетки.

Также этот параметр можно настроить при создании или редактировании самой реакции :ref:`трансформации <Physicell_model_development_Transformation>` на диаграмме модели.

Для работы с уже существующими реакциями трансформации клетки используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Пользовательские данные клетки (Custom data)
--------------------------------------------

Пользовательские данные применяются для расширения списка параметров клеток и могут использоваться в Java-коде, внутриклеточной ОДУ-модели или правилах, описывающих поведение модели.

После нажатия на вкладку **Custom data** на панели свойств справа у вас появится меню, в котором можно редактировать пользовательские данные клетки :ref:`(Рисунок 34) <Physicell_cell_properties_Pic.34>`.

.. _Physicell_cell_properties_Pic.34:

.. figure:: images/Physicell/Physicell_cell_properties/Custom_data_menu.png
   :width: 100%
   :alt: Custom_data_menu
   :align: center

   Рисунок 34. Меню редактирования пользовательских данных клетки.

Чтобы добавить новые данные, нужно:

- нажать ЛКМ на вкладку |icon_option| **Variables**,
- нажать ЛКМ на иконку |icon_add_new| :ref:`(Рисунок 35) <Physicell_cell_properties_Pic.35>`.

.. _Physicell_cell_properties_Pic.35:

.. figure:: images/Physicell/Physicell_cell_properties/Add_new_custom_data.png
   :width: 100%
   :alt: Add_new_custom_data
   :align: center

   Рисунок 35. Добавление новых пользовательских данных клетки.

Таким образом можно добавить сколько угодно пользовательских данных для выбранного типа клеток.

После этого появится новая вкладка, в которой можно редактировтаь следующие параметры :ref:`(Рисунок 36) <Physicell_cell_properties_Pic.36>`:

- **Name**: название параметра,
- **Value**: начальное значение параметра,
- **Units**: единицы измерения параметра (необязательно),
- **Conserved**: отметьте ☑, если хотите, чтобы данный параметр подчинялся закону сохранения масс при делении клеток.

.. _Physicell_cell_properties_Pic.36:

.. figure:: images/Physicell/Physicell_cell_properties/Edit_custom_data.png
   :width: 100%
   :alt: Edit_custom_data
   :align: center

   Рисунок 36. Редактирование пользовательских данных клетки.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Для работы с уже существующими пользовательскими данными клетки используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

.. _Physicell_cell_properties_Functions:

Функции, описывающие поведение клетки (Functions)
-------------------------------------------------

После нажатия на вкладку **Functions** на панели свойств справа у вас появится меню, в котором можно редактировать функции, описывающие поведение клетки :ref:`(Рисунок 37) <Physicell_cell_properties_Pic.37>`.

.. _Physicell_cell_properties_Pic.37:

.. figure:: images/Physicell/Physicell_cell_properties/Functions_menu.png
   :width: 100%
   :alt: Functions_menu
   :align: center

   Рисунок 37. Меню редактирования функций, описывающих поведение клетки.

Всего можно редактировать 11 функций, каждая из которых описывает отдельный аспект жизни клетки :ref:`(Рисунок 38) <Physicell_cell_properties_Pic.38>`.

.. _Physicell_cell_properties_Pic.38:

.. figure:: images/Physicell/Physicell_cell_properties/Functions_all.png
   :width: 100%
   :alt: Functions_all
   :align: center

   Рисунок 38. Функции, описывающие отдельные аспекты жизни клетки.

Для каждой из этих функций доступно на выбор несколько сценариев поведения. Выбрать тот или иной сценарий можно, нажав ЛКМ справа от соответствующей функции и выбрав в раскрывающемся списке нужный сценарий :ref:`(Рисунок 39) <Physicell_cell_properties_Pic.39>`.

.. _Physicell_cell_properties_Pic.39:

.. figure:: images/Physicell/Physicell_cell_properties/Many_scenario.png
   :width: 100%
   :alt: Many_scenario
   :align: center

   Рисунок 39. Для каждой функции доступно несколько сценариев поведения клетки.

Ниже представлен список всех функций и доступных сценариев для каждой из них:

.. raw:: html

   <ul>
      <li><b>Phenotype update</b>: общее описание поведения клетки, изменение ее поведения в зависимости от внешних и внутренних сигналов.
      <ul>
         <li><u>Default O2-based phenotype</u> - описывает жизнедеятельность клетки в зависимости от кислорода.</li>
      </ul>
      </li>
      <li><b>Volume update</b>: описывает изменения объемных свойства клетки (количество жидкости, объем ядра и т.д.) в зависимости от объема.
      <ul>
         <li><u>Standard volume update</u> - задает зависимость свойств от объема по умолчанию.</li>
      </ul>
      </li>
      <li><b>Custom rule</b>: дополнительная функция поведения клетки.
      <ul>
         <li><u>Avoid microenvironment boundaries</u> - клетка избегает границ внешней среды,</li>
         <li><u>Wrap microenvironment boundaries</u> - клетка проходит сквозь границу на другой край внешней среды.</li>
      </ul>
      </li>
      <li><b>Velocity update</b>: описывает изменение скорости передвижения клетки.
      <ul>
         <li><u>Standard Velocity</u> - скорость меняется по правилам по умолчанию в зависимости от заданных степеней адгезии и отклонения и присутствия других клеток вокруг.</li>
      </ul>
      </li>
      <li><b>Migration update</b>: описывает передвижения клетки.
      <ul>
         <li><u>Chemotaxis</u> - хемотаксис по градиенту одного вещества,</li>
         <li><u>Advanced chemotaxis (weighted combination of gradients)</u> - хемотаксис по градиентам нескольких веществ с соответствующими чувствительностями,</li>
         <li><u>Advanced normalize chemotaxis (weighted combination of normalized gradients)</u> - хемотаксис по нормализованным градиентам нескольких веществ с соответствующими чувствительностями.</li>
      </ul>
      </li>
      <li><b>Membrane interaction</b>: описывает взаимодействие клетки с базальной мембраной (<span style="color: red;">сама базальная мембрана не моделируется, предполагается, что вся система расположена на ней</span>).
      <ul>
         <li><u>Avoid domain edge</u> - клетка избегает границы мембраны.</li>
      </ul>
      </li>
      <li><b>Membrane distance calculator</b>: описывает расчет клеткой расстояния до базальной мембраны.
      <ul>
         <li><u>Domain edge distance</u> - рассчитывает расстояние до края мембраны.</li>
      </ul>
      </li>
      <li><b>Orientation</b>: описывает изменение ориентации клетки в пространстве.
      <ul>
         <li><u>Up orientation</u> - ориентация параллельно оси Z.</li>
      </ul>
      </li>
      <li><b>Contact</b>: описывает контакт клетки с другими клетками.
      <ul>
         <li><u>Standard Elastic Contact</u> - эластичная адгезия/отталкивание от других типов клеток.</li>
      </ul>
      </li>
      <li><b>Cell creation</b>: описывает процесс создания новой клетки во время деления или при начальной инициализации.</li>
      <li><b>Cell division</b>: описывает процесс деления клетки.
      <ul>
         <li><u>Standard asymmetric division</u> - клетка делится асимметрично.</li>
      </ul>
      </li>
   </ul>

Также для каждой функции можно выбрать сценарий «**Custom...**». При таком выборе ниже функции, для которой был выбран данный сценарий, появится дополнительная вкладка |icon_option| «**Custom [название функции]**», в которой нужно указать путь до Java-кода, который будет описывать поведение клетки в рамках соответствующей функции :ref:`(Рисунок 40) <Physicell_cell_properties_Pic.40>`.

.. _Physicell_cell_properties_Pic.40:

.. figure:: images/Physicell/Physicell_cell_properties/Custom_scenario.png
   :width: 100%
   :alt: Custom_scenario
   :align: center

   Рисунок 40. Для каждой функции можно выбрать пользовательский Java-код, который будет описывать поведение клетки в рамках соответствующей функции (показано на примере функции «Phenotype update»).

Внутриклеточная модель клетки (Intracellular)
---------------------------------------------

Для задания внутриклеточных механизмов для выбранного типа клеток может применяться SBML-модель, использующая обыкновенные дифференциальные уравнения, алгебраические уравнения и дискретные события. Данная модель может использовать в качестве параметров свойства клетки, количество потребленных и выделенных веществ, а также может менять значения свойств клетки.

После нажатия на вкладку **Intracellular** на панели свойств справа у вас появится меню, в котором напротив поля |icon_option| **Diagram** можно указать путь до SBML-модели, которая будет описывать поведение внутри клеток выбранного типа :ref:`(Рисунок 41) <Physicell_cell_properties_Pic.41>`.

.. _Physicell_cell_properties_Pic.41:

.. figure:: images/Physicell/Physicell_cell_properties/Intracellular_menu.png
   :width: 100%
   :alt: Intracellular_menu
   :align: center

   Рисунок 41. Меню, в котором нужно указать путь до SBML-модели, описывающей реакции внутри клетки.

Чтобы указать путь до SBML-модели, нужно нажать ЛКМ на |icon_option| **(select element)** и в появившемся меню указать, где в вашем репозитории находится SBML-модель :ref:`(Рисунок 42) <Physicell_cell_properties_Pic.42>`.

.. _Physicell_cell_properties_Pic.42:

.. figure:: images/Physicell/Physicell_cell_properties/SBML_model_path.png
   :width: 100%
   :alt: SBML_model_path
   :align: center

   Рисунок 42. Указание пути до SBML-модели.

После указания пути до SBML-модели, у вас появятся два новых поля :ref:`(Рисунок 43) <Physicell_cell_properties_Pic.43>`:

- **Variables**: список соответствий между переменными SBML-модели и свойствами клетки,
- **engine**: движок, используемый для симуляции SBML-модели.

.. _Physicell_cell_properties_Pic.43:

.. figure:: images/Physicell/Physicell_cell_properties/New_fields_intracellular.png
   :width: 100%
   :alt: New_fields_intracellular
   :align: center

   Рисунок 43. После указания SBML-модели возникают поля Variables и engine.

Ниже разберем как редактировать каждое из этих полей.

Список соответствий между переменными SBML-модели и свойствами клетки (Variables)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Чтобы добавить соответствие между одной переменной SBML-модели и одним свойством клетки нужно:

- нажать ЛКМ на |icon_option| **Variables**,
- нажать ЛКМ на иконку |icon_add_new| :ref:`(Рисунок 44) <Physicell_cell_properties_Pic.44>`.

.. _Physicell_cell_properties_Pic.44:

.. figure:: images/Physicell/Physicell_cell_properties/New_correspondance.png
   :width: 100%
   :alt: New_correspondance
   :align: center

   Рисунок 44. Добавление соответствия между одной переменной SBML-модели и одним свойством клетки.

Таким образом можно добавить сколько угодно соответствий.

После этого под |icon_option| **Variables** появится новая вкладка, в которой можно редактировать три параметра :ref:`(Рисунок 45) <Physicell_cell_properties_Pic.45>`:

- **Variable**: название переменной SBML-модели, в соответствие которой мы хотим задать то или иное свойство клетки,
- **Phenotype property**: название свойства клетки, соответствующего выбранной переменной,
- **Type**: тип соответствия.

.. _Physicell_cell_properties_Pic.45:

.. figure:: images/Physicell/Physicell_cell_properties/Variable_phenotype_property_type.png
   :width: 100%
   :alt: Variable_phenotype_property_type
   :align: center

   Рисунок 45. Для каждого соответствия можно редактировать параметры Variable, Phenotype property и Type.

Чтобы указать значение каждого из этих трех параметров, нужно нажать ЛКМ справа от соответствующего поля (**Variable**, **Phenotype property** или **Type**) и из раскрывающегося списка выбрать нужное значение :ref:`(Рисунок 46) <Physicell_cell_properties_Pic.46>`.

.. _Physicell_cell_properties_Pic.46:

.. figure:: images/Physicell/Physicell_cell_properties/Variable_selection.png
   :width: 100%
   :alt: Variable_selection
   :align: center

   Рисунок 46. Выбор значений параметров Variable, Phenotype property и Type из раскрывающегося списка.

В раскрывающихся списках напротив полей |icon_option| **Variable** и |icon_option| **Phenotype property** можно найти любой параметр выбранной SBML-модели и любое свойство выбранного типа клеток, соответственно.

В раскрывающемся списке напротив |icon_option| **Type** всегда можно выбрать один из 3-ех типов соответствия:

- **Input**: переменная SBML-модели является параметром Physicell модели. Численное значение проставляется в SBML-модель из выбранного свойства клетки (значение определяется Physicell моделью и SBML-модель никак на него не влияет; она только использует его в качестве значения одного из своих параметров),
- **Output**: переменная SBML-модели рассчитывается в этой же модели и полученное численное значение проставляется в Physicell модель как значение соответствующего свойства клетки (значение определяется SBML-моделью и Physicell модель никак на него не влияет; она только использует его в качестве значения одного из свойств клетки),
- **Contact**: переменная SBML-модели проставляется в эту же модель из свойств клетки, но меняется в результате решения системы ОДУ внутри SBML-модели, и измененное численное значение проставляется обратно в свойства клетки в Physicell модель и т.д. (значение определяется в обеих моделях: SBML и Physicell).

Для работы с уже существующими соответствиями используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.

Движок, используемый для симуляции SBML-модели (engine)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Внутри вкладки **engine** можно редактировать значения следующих параметров :ref:`(Рисунок 47) <Physicell_cell_properties_Pic.47>`:

- **Selected engine**: движок, используемый для симуляции SBML-модели,
- **Time increment**: размер шага симуляции SBML-модели,
- **Simulator**: численный решатель систем обыкновенных дифференциальных уравнений, используемый при симуляции SBML-модели,
- **Simulator options**: параметры решателя.

.. _Physicell_cell_properties_Pic.47:

.. figure:: images/Physicell/Physicell_cell_properties/Engine_parameters.png
   :width: 100%
   :alt: Engine_parameters
   :align: center

   Рисунок 47. Внутри вкладки engine можно редактировать значения полей Selected engine, Time increment, Simulator и Simulator options.

Чтобы выбрать движок для симуляции SBML-модели, нужно нажать ЛКМ справа от иконки |icon_option| **Selected engine** и из раскрывающегося списка выбрать один из доступных вариантов :ref:`(Рисунок 48) <Physicell_cell_properties_Pic.48>`.

.. _Physicell_cell_properties_Pic.48:

.. figure:: images/Physicell/Physicell_cell_properties/Engine_selection.png
   :width: 100%
   :alt: Engine_selection
   :align: center

   Рисунок 48. Выбор движка для симуляции SBML-модели.

Ниже представлены доступные варианты движков:

- **ODE Simulation Engine**,
- **Stochastic Simulation Engine**,
- **SDE Simulation Engine**,
- **FBA Simulation Engine**,
- **Agent Model Simulation Engine**,
- **VirtualCell Simulation Engine**,
- **Covid-19 Simulation**.

Чтобы выбрать численный решатель для симуляции SBML-модели, нужно нажать ЛКМ справа от иконки |icon_option| **Simulator** и из раскрывающегося списка выбрать один из доступных вариантов (аналогично выбору движка).

Для каждого движка доступны собственные варианты решателей. Ниже представлены списки решателей для каждого движка:

- ODE Simulation Engine:
   - :raw-html:`«<u>Euler</u>»`,
   - :raw-html:`«<u>DormandPrince</u>»`,
   - :raw-html:`«<u>Imex</u>»`,
   - :raw-html:`«<u>Discrete</u>»`,
   - :raw-html:`«<u>JVode</u>»`,
   - :raw-html:`«<u>Radau5</u>»`.
- Stochastic Simulation Engine:
   - :raw-html:`«<u>Tau Leap Method</u>»`,
   - :raw-html:`«<u>Maximum Time Step algorithm</u>»`,
   - :raw-html:`«<u>Gibson and Bruck</u>»`,
   - :raw-html:`«<u>Gillespie</u>»`.
- SDE Simulation Engine:
   - :raw-html:`«<u>Heun stochastic</u>»`,
   - :raw-html:`«<u>Euler stochastic</u>»`.
- FBA Simulation Engine:
   - :raw-html:`«<u>Euler</u>»`,
   - :raw-html:`«<u>DormandPrince</u>»`,
   - :raw-html:`«<u>Imex</u>»`,
   - :raw-html:`«<u>Discrete</u>»`,
   - :raw-html:`«<u>JVode</u>»`,
   - :raw-html:`«<u>Radau5</u>»`.
- Agent Model Simulation Engine:
   - :raw-html:`«<u>Default Scheduler</u>»`.
- VirtualCell Simulation Engine:
   - :raw-html:`«<u>Virtual Cell Solver</u>»`.
- Covid-19 Simulation:
   - :raw-html:`<span style="color: red;">Решатель не указывается!</span>`

Чтобы выбрать размер шага симуляции SBML-модели, нужно нажать ЛКМ справа от иконки |icon_option| **Time increment** и вписать собственное значение :ref:`(Рисунок 49) <Physicell_cell_properties_Pic.49>`.

.. _Physicell_cell_properties_Pic.49:

.. figure:: images/Physicell/Physicell_cell_properties/Edit_time_increment.png
   :width: 100%
   :alt: Edit_time_increment
   :align: center

   Рисунок 49. Изменение шага симуляции SBML-модели.

Чтобы редактировать параметры выбранного решателя, нужно раскрыть вкладку **Simulator options** и справа от названия параметра вписать собственное значение, выбрать предложенное значение из раскрывающегося списка или отметить ☑ :ref:`(Рисунок 50) <Physicell_cell_properties_Pic.50>`.

.. _Physicell_cell_properties_Pic.50:

.. figure:: images/Physicell/Physicell_cell_properties/Simulator_options.png
   :width: 100%
   :alt: Simulator_options
   :align: center

   Рисунок 50. Настройка параметров решателя (показано на примере решателя JVode движка ODE Simulation Engine).

.. warning::
   - Для каждого решателя доступен свой набор параметров для редактирования.
   - Для некоторых решателей невозможно редактировать их параметры.

Правила, описывающие поведение клетки (Rules)
---------------------------------------------

Как работают правила?
~~~~~~~~~~~~~~~~~~~~~

Правила используются для того, чтобы регулировать поведение клетки в зависимости от различных сигналов. Для описания зависимости между уровнем сигнала (например, количеством субстрата) и интенсивностью определенного клеточного процесса (например, деления) используется закон Хилла :ref:`(Рисунок 51) <Physicell_cell_properties_Pic.51>`.

.. _Physicell_cell_properties_Pic.51:

.. figure:: images/Physicell/Physicell_cell_properties/Hill_equation.png
   :width: 50%
   :alt: Hill_equation
   :align: center

   Рисунок 51. Закон Хилла, по которому работают правила.

В формуле на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>` используются следующие обозначения:

- **B**: интенсивность определенного клеточного процесса,
- :raw-html:`<strong>B<sub>max</sub></strong>`: максимально возможная интенсивность определенного клеточного процесса,
- **S**: уровень сигнала,
- :raw-html:`<strong>S<sub>0.5</sub></strong>`: уровень сигнала, при котором интенсивность определенного клеточного процесса равна половине от максимально возможной,
- **h**: коэффициент Хилла.

В зависимости от знака (+ или -) связь между уровнем сигнала и интенсивностью клеточного процесса, описываемая уравнением Хилла, может быть либо прямопропорциональной (знак + перед уравнением), либо обратнопропорциональной (знак - перед уравнением).

График уравнения Хилла представлен на :ref:`рисунке 52 <Physicell_cell_properties_Pic.52>`.

.. _Physicell_cell_properties_Pic.52:

.. figure:: images/Physicell/Physicell_cell_properties/Hill_equation_plot.png
   :width: 100%
   :alt: Hill_equation_plot
   :align: center

   Рисунок 52. График уравнения Хилла с прямопропорциональной (А) и обратнопропорциональной (Б) зависимостями.

В зависимости от значений коэффициентов :raw-html:`<strong>B<sub>max</sub></strong>`, :raw-html:`<strong>S<sub>0.5</sub></strong>` и **h** кривая зависимости меняется следующим образом:

.. raw:: html

   <ul>
      <li><strong>B<sub>max</sub></strong>:
      <ul>
         <li><span style="color: green;">увеличение</span> значения увеличивает "высоту" кривой,</li>
         <li><span style="color: red;">уменьшение</span> значения уменьшает "высоту" кривой.</li>
      </ul>
      </li>
      <li><strong>S<sub>0.5</sub></strong>:
      <ul>
         <li><span style="color: green;">увеличение</span> значения способствует более плавному "подъему" кривой до максимального значения,</li>
         <li><span style="color: red;">уменьшение</span> значения способствует более резкому "подъему" кривой до максимального значения.</li>
      </ul>
      </li>
      <li><strong>h</strong>:
      <ul>
         <li><span style="color: green;">увеличение</span> значения приводит к появлению S-образной кривой,</li>
         <li><span style="color: red;">уменьшение</span> значения приводит к появлению плавноподнимающейся кривой.</li>
      </ul>
      </li>
   </ul>

На :ref:`рисунке 53 <Physicell_cell_properties_Pic.53>` приведены примеры графиков уравнения Хилла с разными значениями этих коэффициентов.

.. _Physicell_cell_properties_Pic.53:

.. figure:: images/Physicell/Physicell_cell_properties/Hill_equation_plot_dependancy.png
   :width: 100%
   :alt: Hill_equation_plot_dependancy
   :align: center

   Рисунок 53. Графики уравнения Хилла с прямопропорциональной (А, В, Д) и обратнопропорциональной (Б, Г, Е) зависимостями. Влияние параметров :raw-html:`B<sub>max</sub>` (А, Б), :raw-html:`S<sub>0.5</sub>` (В, Г) и h (Д, Е) на форму кривой.

Настройка правил в модели
~~~~~~~~~~~~~~~~~~~~~~~~~

После нажатия на вкладку **Rules** на панели свойств справа у вас появится меню, в котором, нажав ЛКМ на иконку |icon_plus|, можно добавить правило, описывающее поведение клетки :ref:`(Рисунок 54) <Physicell_cell_properties_Pic.54>`.

.. _Physicell_cell_properties_Pic.54:

.. figure:: images/Physicell/Physicell_cell_properties/Add_new_rule.png
   :width: 100%
   :alt: Add_new_rule
   :align: center

   Рисунок 54. Добавление правила, описывающего поведения клетки.

Таким образом можно добавить сколько угодно правил.

После этого в меню появится строка, в которой можно описывать определенное правило :ref:`(Рисунок 55) <Physicell_cell_properties_Pic.55>`.

.. _Physicell_cell_properties_Pic.55:

.. figure:: images/Physicell/Physicell_cell_properties/Raw_for_rule.png
   :width: 100%
   :alt: Raw_for_rule
   :align: center

   Рисунок 55. Строка для описания правила.

В данной строке можно настроить следующие параметры:

- **Signal**: сигнал (S на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Direction**: направление действия сигнала (± на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Behavior**: клеточный процесс (B на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Saturation value**: максимально возможная интенсивность клеточного процесса (:raw-html:`B<sub>max</sub>` на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Half-max**: уровень сигнала, при котором интенсивность клеточного процесса равна половине от максимально возможной (:raw-html:`S<sub>0.5</sub>` на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Hill power**: коэффициент Хилла (h на :ref:`рисунке 51 <Physicell_cell_properties_Pic.51>`),
- **Apply to dead**: отметьте ☑, если создаваемое правило должно распространяться не только на живые, но и на мертвые клетки.

.. note::
   - Значение increase параметра Direction соответствует знаку +.
   - Значение decrease параметра Direction соответствует знаку -.

Чтобы выбрать значение параметров **Signal**, **Direction** и **Behavior**, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и из раскрывающегося списка выбрать нужное значение :ref:`(Рисунок 56) <Physicell_cell_properties_Pic.56>`.

.. _Physicell_cell_properties_Pic.56:

.. figure:: images/Physicell/Physicell_cell_properties/Choose_signal.png
   :width: 100%
   :alt: Choose_signal
   :align: center

   Рисунок 56. Выбор значений параметров Signal, Direction и Behavior из раскрывающегося списка (показано на примере Signal).

Чтобы выбрать значение параметров **Saturation value**, **Half-max** и **Hill power**, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение.

Чтобы удалить правило, нужно:

- нажать ЛКМ в любое место строки, соответствующей этому правилу,
- нажать ЛКМ иконку |icon_minus| :ref:`(Рисунок 57) <Physicell_cell_properties_Pic.57>`.

.. _Physicell_cell_properties_Pic.57:

.. figure:: images/Physicell/Physicell_cell_properties/Delete_rule.png
   :width: 100%
   :alt: Delete_rule
   :align: center

   Рисунок 57. Удаление правила.

Начальное распределение характеристик клетки (Initial distribution)
----------------------------------------------------------------------------

После нажатия на вкладку **Initial distribution** на панели свойств справа у вас появится меню, в котором можно редактировать начальное распределение значений различных характеристик клетки в модели :ref:`(Рисунок 58) <Physicell_cell_properties_Pic.58>`.

.. _Physicell_cell_properties_Pic.58:

.. figure:: images/Physicell/Physicell_cell_properties/Initial_distribution_menu.png
   :width: 100%
   :alt: Initial_distribution_menu
   :align: center

   Рисунок 58. Меню редактирования начальных распределений характеристик клетки.

Чтобы добавить распределение одной характеристики клетки, нужно:

- нажать ЛКМ на строку со вкладкой |icon_option| **Distributions**,
- нажать ЛКМ на иконку |icon_add_new| :ref:`(Рисунок 59) <Physicell_cell_properties_Pic.59>`.

.. _Physicell_cell_properties_Pic.59:

.. figure:: images/Physicell/Physicell_cell_properties/Add_initial_distribution.png
   :width: 100%
   :alt: Add_initial_distribution
   :align: center

   Рисунок 59. Добавление нового распределения.

После добавления распределения у вас появится вкладка с его порядковым номером (начиная с [0]). Раскрыв эту вкладку, можно увидеть доступные для редактирования параметры :ref:`(Рисунок 60) <Physicell_cell_properties_Pic.60>`:

- **Model parameter**: характеристика клетки, начальное распределение значений которой мы хотим задать,
- **Distribution**: форма распределения,
- **Min**: минимально возможное значение характеристики,
- **Max**: максимально возможное значение характеристики.

.. _Physicell_cell_properties_Pic.60:

.. figure:: images/Physicell/Physicell_cell_properties/Initial_distribution_parameters.png
   :width: 100%
   :alt: Initial_distribution_parameters
   :align: center

   Рисунок 60. Параметры распределения.

Чтобы выбрать значение параметров **Model parameter** и **Distribution**, нужно нажать ЛКМ справа от соответствующей иконки и из раскрывающегося списка выбрать нужное значение :ref:`(Рисунок 61) <Physicell_cell_properties_Pic.61>`.

.. _Physicell_cell_properties_Pic.61:

.. figure:: images/Physicell/Physicell_cell_properties/Edit_model_parameter.png
   :width: 100%
   :alt: Edit_model_parameter
   :align: center

   Рисунок 61. Выбор значений параметров Model parameter и Distribution (показано на примере Model parameter).

Для каждого параметра доступны следующие формы распределений :ref:`(Рисунок 62) <Physicell_cell_properties_Pic.62>`:

- **Uniform**: равномерное распределение,
- **LogUniform**: лог-равномерное распределение,
- **Normal**: нормальное (Гауссово) распределение,
- **LogNormal**: лог-нормальное распределение,
- **Log10Normal**: лог10-нормальное распределение.

.. _Physicell_cell_properties_Pic.62:

.. figure:: images/Physicell/Physicell_cell_properties/Distributions.png
   :width: 100%
   :alt: Distributions
   :align: center

   Рисунок 62. Доступные распределения.

Чтобы выбрать значение параметров **Min** и **Max**, нужно нажать ЛКМ справа от соответствующей иконки и вписать собственное значение.

Для работы с уже существующими распределениями используйте тот же функционал, что и при редактировании фаз и переходов между ними в жизненном цикле клетки :ref:`(таблица 1) <Physicell_cell_properties_Tbl.1>`.