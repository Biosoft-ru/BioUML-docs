Свойства типа клеток
====================

.. role:: raw-html(raw)
   :format: html

У каждого типа клеток в модели есть определенный набор свойств. Чтобы настроить эти свойства, нужно:

1. Выбрать на диаграмме тип клеток, свойства которого вы хотите изменить.
2. В правом нижнем окошке нажать ЛКМ на вкладку **Cell Types**.

.. figure:: /images/Physicell/Physicell_cell_properties/Cell_Types_button.png
   :width: 100%
   :alt: Cell_Types_buttton
   :align: center

:raw-html:`<br>`
После этого в правом нижнем окошке у вас появится перечень свойств типа клеток.

.. figure:: /images/Physicell/Physicell_cell_properties/Cell_properties_panel.png
   :width: 100%
   :alt: Cell_properties_panel
   :align: center

:raw-html:`<br>`

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

Чтобы перейти к редактированию того или иного свойства типа клеток, нужно нажать ЛКМ на соответствующую вкладку в панели свойств.

.. important::
   Здесь указываются начальные значения характеристик - в процессе расчетов для каждой конкретной клетки они могут меняться.

Далее мы рассмотрим каждое из свойст подробно.

.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_cell_properties_Cycle
   PhysiCell_cell_properties_Division
   PhysiCell_cell_properties_Death
   PhysiCell_cell_properties_Volume
   PhysiCell_cell_properties_Mechanics
   PhysiCell_cell_properties_Integrity
   PhysiCell_cell_properties_Motility
   PhysiCell_cell_properties_Secretion
   PhysiCell_cell_properties_Interactions
   PhysiCell_cell_properties_Transformations
   PhysiCell_cell_properties_Custom_data
   PhysiCell_cell_properties_Functions
   PhysiCell_cell_properties_Intracellular
   PhysiCell_cell_properties_Rules
   PhysiCell_cell_properties_Initial_distribution
