.. _PhysiCell_cell_properties_Motility:

Подвижность клетки (Motility)
-----------------------------

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_chemotaxis| image:: /images/icons/Physicell/chemotaxis_corrected.png

После нажатия на вкладку **Motility** на панели свойств справа у вас появится меню, в котором нужно поставить ☑ напротив |icon_option| **Is Motile**, если выбранный тип клеток должен быть подвижен.

.. figure:: /images/Physicell/Physicell_cell_properties/Is_motile.png
   :width: 100%
   :alt: Is_motile
   :align: center

:raw-html:`<br>`
Если выбранный тип клеток должен быть неподвижен, то оставьте вкладку **Motility** без изменений.

При отметке того, что клетки выбранного типа должны быть подвижны, у вас появится меню, в котором можно настроить параметры подвижности:

.. figure:: /images/Physicell/Physicell_cell_properties/Motility_menu.png
   :width: 100%
   :alt: Motility_menu
   :align: center

:raw-html:`<br>`

- **Migration speed**: скорость передвижения клетки,
- **Persistence time**: время, в течение которого клетка не меняет направление движения,
- **Migration bias**: склонность клетки к целенаправленному движению (1 - клетки движутся только целенаправленно, 0 - только случайно).
- **Restricted to 2D**: отметьте ☑, если клетки должны двигаться только в двух измерениях,
- **Chemotaxis**: настройка параметров хемотаксиса (рассмотрено ниже).

На рисунке выше выбранный тип клеток на диаграмме уже имеет хемотаксис (|icon_chemotaxis|), поэтому под полем **Chemotaxis** уже располагается поле с названием субстрата (в данном случае, **Substrate**), к или от которого двигаются клетки выбранного типа. Если бы клетки выбранного типа на диаграмме имели несколько хемотаксисов, то таких полей было бы несколько (отдельное поле для каждого хемотаксиса на диаграмме).

Раскрыв вкладку с названием субстрата, можно настроить чувствительность к этому субстрату.

.. figure:: /images/Physicell/Physicell_cell_properties/Sensitivity_setting.png
   :width: 100%
   :alt: Sensitivity_setting
   :align: center

:raw-html:`<br>`
Также чувствительность клетки к субстрату можно настроить непосредственно на диаграмме модели.

.. important::
   Во вкладке Motility не следует добавлять новые хемотаксисы -  добавляйте и удаляйте их только через диаграмму.