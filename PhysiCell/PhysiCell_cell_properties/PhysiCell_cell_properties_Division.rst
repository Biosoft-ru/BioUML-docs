.. _PhysiCell_cell_properties_Division:

Тип деления клетки (Division)
=============================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png

После нажатия на вкладку **Division** на панели свойств справа у вас появится меню, в котором можно изменять параметры деления клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Division_menu.png
   :width: 100%
   :alt: Division_menu
   :align: center

:raw-html:`<br>`
Если деление выбранного вами типа клеток должно происходить асимметрично, то отметьте ☑ справа от поля |icon_option| **Asymmetric division**.

.. note::
   Асимметричное деление - деление, при котором из клетки одного типа могут образоваться клетки другого типа.

При выборе этого пункта ниже у вас появится поле **Probabilities** (вероятности появления клеток другого типа).

.. figure:: /images/Physicell/Physicell_cell_properties/Probabilities.png
   :width: 100%
   :alt: Probabilities
   :align: center

:raw-html:`<br>`
Чтобы добавить вероятность появления клетки другого типа при делении, нужно:

1. Нажать ЛКМ на строку с полем **Probabilities**.
2. Нажать ЛКМ на значок |icon_add_new|.

.. figure:: /images/Physicell/Physicell_cell_properties/Add_new_probability.png
   :width: 100%
   :alt: Add_new_probability
   :align: center

:raw-html:`<br>`
Таким образом можно добавить сколько угодно вероятностей для выбранного типа клеток (при открытии вкладки **Probabilities** каждая вероятность будет иметь свой порядковый номер, начиная с [0]).

Для работы с уже существующими вероятностями используйте :ref:`этот функционал <Physicell_cell_properties_Actions>`.

Для каждой вероятности можно настраивать 2 параметра.

.. figure:: /images/Physicell/Physicell_cell_properties/Probability_for_cell_type.png
   :width: 100%
   :alt: Probability_for_cell_type
   :align: center

:raw-html:`<br>`

- **Cell type**: тип клеток, который может получиться при делении родительской клетки,
- **Probability**: вероятность появления клетки другого типа (выбранного в Cell type) при делении родительской клетки.

Чтобы изменить значение каждого из этих параметров, нужно нажать ЛКМ справа от соответствующего параметра и вписать свое значение.

.. important::
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
