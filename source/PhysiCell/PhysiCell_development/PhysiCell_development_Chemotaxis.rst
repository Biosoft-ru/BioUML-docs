.. _PhysiCell_development_Chemotaxis:

Создание хемотаксиса
====================

.. |icon_chemotaxis| image:: /images/icons/Physicell/chemotaxis.png
.. |icon_option| image:: /images/icons/option.png

В результате хемотаксиса клетка движется по градиенту вещества к нему или от него.

Чтобы создать в модели хемотаксис, нужно:

1. Нажать ЛКМ на значок |icon_chemotaxis| на панели инструментов.
2. Нажать ЛКМ на тип клеток, который будет двигаться к/от определенного субстрата.
3. Нажать ЛКМ на субстрат, к/от которого клетки выбранного типа будут двигаться.

.. figure:: /images/Physicell/Physicell_model_development/Chemotaxis_creation.png
   :width: 80%
   :alt: Chemotaxis_creation
   :align: center

:raw-html:`<br>`
После этого на диаграмме появится стрелочка фиолетового цвета, направленная от субстрата к клетке.

.. figure:: /images/Physicell/Physicell_model_development/Chemotaxis_reaction.png
   :width: 80%
   :alt: Chemotaxis_reaction
   :align: center

:raw-html:`<br>`
Чтобы редактировать параметры созданного хемотаксиса, нужно нажать ПКМ на стрелку на диаграмме, обозначающую данный хемотаксис, и в раскрывающемся списке нажать ЛКМ на кнопку **Edit**.

После этого в появившемся окне необходимо задать параметры изменяемого хемотаксиса:

.. figure:: /images/Physicell/Physicell_model_development/Chemotaxis_parameters.png
   :width: 80%
   :alt: Chemotaxis_parameters
   :align: center

:raw-html:`<br>`

- **Title**: название хемотаксиса,
- **Comment**: комментарий,
- **Substrate**: название субстрата (:raw-html:`<span style="color: red;">не изменяется!</span>`),
- **Sensitivity**: чувствительность к выбранному веществу.

.. note::
   - Положительные значения Sensitivity указывают на то, что клетка будет двигаться к субстрату, а отрицательные - от субстрата.

   - Абсолютное значение Sensitivity указывает на "силу" движения клетки к/от определенного субстрата.

После того как заданы все параметры, нажмите **Ok**.
