.. _PhysiCell_cell_properties_Transformations:

Трансформация клетки (Transformations)
======================================

.. role:: raw-html(raw)
   :format: html

.. |icon_transformation| image:: /images/icons/Physicell/transformation.png

После нажатия на вкладку **Transformations** на панели свойств справа у вас появится меню, в котором отображаются параметры трансформаций клеток выбранного типа.

.. figure:: /images/Physicell/Physicell_cell_properties/Transformations_menu.png
   :width: 100%
   :alt: Transformations_menu
   :align: center

:raw-html:`<br>`
Если выбранный тип клеток на диаграмме не имеет трансформаций, то на вкладке **Transformations** не будет доступных для редактирования параметров.

На рисунке выше выбранный тип клеток на диаграмме уже имеет трансформацию (|icon_transformation|), поэтому под полем **Cell types** уже располагается поле с названием типа клеток (в данном случае, **CellDefinition**), в который клетки выбранного типа трансформируются. Если бы выбранный тип клеток на диаграмме имел несколько трансформаций, то таких полей было бы несколько (отдельное поле для каждой трансформации на диаграмме).

Для каждого типа клеток, в который выбранные клетки трансформируются, можно настроить параметр **Transformation rate**, характеризующий скорость трансформации.

.. figure:: /images/Physicell/Physicell_cell_properties/Transformation_rate_setting.png
   :width: 100%
   :alt: Transformation_rate_setting
   :align: center

:raw-html:`<br>`
Также этот параметр можно настроить непосредственно на диаграмме модели.

.. important::
   Во вкладке Transformations не следует добавлять новые трансформации -  добавляйте и удаляйте их только через диаграмму.