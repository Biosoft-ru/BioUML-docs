.. _PhysiCell_microenvironment_Initial_Condition:
 
Начальное расположение клеток (Initial Condition)
=================================================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_Java_code| image:: /images/icons/Physicell/Java_code.png
.. |icon_table| image:: /images/icons/Physicell/table.png

После нажатия на вкладку **Initial Condition** на панели свойств справа у вас появится меню, в котором нужно поставить ☑ напротив |icon_option| **Custom condition**, если вы хотите задать определенное начальное расположение клеток.

.. figure:: /images/Physicell/Physicell_microenvironment/Initial_condition_menu.png
   :width: 100%
   :alt: Initial_condition_menu
   :align: center

:raw-html:`<br>`
Если вы не хотите настраивать определенное начальное расположение клеток (хотите оставить случайное расположение), то оставьте вкладку **Initial Condition** без изменений.

При выборе ☑ напротив |icon_option| **Custom condition** у вас появится меню, в котором можно настроить 2 параметра:

.. figure:: /images/Physicell/Physicell_microenvironment/Initial_condition_parameters.png
   :width: 100%
   :alt: Initial_condition_parameters
   :align: center

:raw-html:`<br>`

- |icon_option| **Custom Java code**: путь до Java-кода в репозитории, описывающего начальное расположение клеток в модели,
- |icon_option| **Custom table**: путь до таблицы в репозитории, описывающей начальное расположение клеток в модели.

Чтобы указать путь до Java-кода или таблицы, нужно нажать ЛКМ на |icon_Java_code| **(select element)** или |icon_table| **(select element)**, соответственно, и в появившемся окне выбрать нужный файл в репозитории.

.. warning::
   Нельзя одновременно указать и Java-код и таблицу, нужно выбрать что-то одно.