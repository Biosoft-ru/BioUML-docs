.. _PhysiCell_cell_properties_Custom_data:

Пользовательские данные клетки (Custom data)
============================================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png

Пользовательские данные применяются для расширения списка параметров клеток и могут использоваться в Java-коде, внутриклеточной ОДУ-модели или правилах, описывающих поведение клетки.

После нажатия на вкладку **Custom data** на панели свойств справа у вас появится меню, в котором можно редактировать пользовательские данные клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Custom_data_menu.png
   :width: 100%
   :alt: Custom_data_menu
   :align: center

:raw-html:`<br>`
Чтобы добавить новые данные, нужно:

1. Нажать ЛКМ на вкладку |icon_option| **Variables**.
2. Нажать ЛКМ на иконку |icon_add_new|.

.. figure:: /images/Physicell/Physicell_cell_properties/Add_new_custom_data.png
   :width: 100%
   :alt: Add_new_custom_data
   :align: center

:raw-html:`<br>`
Таким образом можно добавить сколько угодно пользовательских данных для выбранного типа клеток.

После этого появится новая вкладка, в которой можно редактировтаь следующие параметры:

.. figure:: /images/Physicell/Physicell_cell_properties/Edit_custom_data.png
   :width: 100%
   :alt: Edit_custom_data
   :align: center

:raw-html:`<br>`

- **Name**: название параметра,
- **Value**: начальное значение параметра,
- **Units**: единицы измерения параметра (необязательно),
- **Conserved**: отметьте ☑, если хотите, чтобы данный параметр подчинялся закону сохранения масс при делении клеток.

Изменить значение каждого из параметров можно, нажав ЛКМ на значение справа от соответствующего параметра и введя собственное значение.

Для работы с уже существующими пользовательскими данными клетки используйте :ref:`этот функционал <Physicell_cell_properties_Actions>`.