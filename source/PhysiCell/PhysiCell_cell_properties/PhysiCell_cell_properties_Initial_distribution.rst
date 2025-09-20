.. _PhysiCell_cell_properties_Initial_distribution:

Начальное распределение характеристик клеток (Initial distribution)
===================================================================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png

После нажатия на вкладку **Initial distribution** на панели свойств справа у вас появится меню, в котором можно редактировать начальное распределение различных характеристик клеток выбранного типа в модели.

.. figure:: /images/Physicell/Physicell_cell_properties/Initial_distribution_menu.png
   :width: 100%
   :alt: Initial_distribution_menu
   :align: center

:raw-html:`<br>`
Чтобы добавить распределение одной характеристики, нужно:

1. Нажать ЛКМ на строку со вкладкой |icon_option| **Distributions**.
2. Нажать ЛКМ на иконку |icon_add_new|.

.. figure:: /images/Physicell/Physicell_cell_properties/Add_initial_distribution.png
   :width: 100%
   :alt: Add_initial_distribution
   :align: center

:raw-html:`<br>`
После добавления распределения у вас появится вкладка с его порядковым номером (начиная с [0]). Раскрыв эту вкладку, можно увидеть доступные для редактирования параметры:

.. figure:: /images/Physicell/Physicell_cell_properties/Initial_distribution_parameters.png
   :width: 100%
   :alt: Initial_distribution_parameters
   :align: center

:raw-html:`<br>`

- **Model parameter**: характеристика клеток выбранного типа, начальное распределение которой мы хотим задать,
- **Distribution**: форма распределения,
- **Min**: минимально возможное значение характеристики,
- **Max**: максимально возможное значение характеристики.

Чтобы выбрать значение параметров **Model parameter** и **Distribution**, нужно нажать ЛКМ справа от соответствующей иконки и из раскрывающегося списка выбрать нужное значение.

.. figure:: /images/Physicell/Physicell_cell_properties/Edit_model_parameter.png
   :width: 100%
   :alt: Edit_model_parameter
   :align: center

:raw-html:`<br>`
Для каждого параметра доступны следующие формы распределений:

.. figure:: /images/Physicell/Physicell_cell_properties/Distributions.png
   :width: 100%
   :alt: Distributions
   :align: center

:raw-html:`<br>`

- **Uniform**: равномерное распределение,
- **LogUniform**: лог-равномерное распределение,
- **Normal**: нормальное (Гауссово) распределение,
- **LogNormal**: лог-нормальное распределение,
- **Log10Normal**: лог10-нормальное распределение.

Чтобы выбрать значение параметров **Min** и **Max**, нужно нажать ЛКМ справа от соответствующей иконки и вписать собственное значение.

Для работы с уже существующими распределениями используйте :ref:`этот функционал <Physicell_cell_properties_Actions>`.