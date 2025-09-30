.. _PhysiCell_development_Transformation:

Создание трансформации
======================

.. |icon_transformation| image:: /images/icons/Physicell/transformation.png

При трансформации клетка одного типа превращается в клетку другого типа.

Чтобы создать в модели трансформацию, нужно:

1. Нажать ЛКМ на значок |icon_transformation| на панели инструментов.
2. Нажать ЛКМ на тип клеткок, которые будут трансформироваться в другой тип клеток.
3. Нажать ЛКМ на тип клеток, в которые будет происходить трансформация.

.. figure:: /images/Physicell/Physicell_model_development/Transformation_creation.png
   :width: 80%
   :alt: Transformation_creation
   :align: center

:raw-html:`<br>`
После этого на диаграмме появится стрелочка синего цвета, направленная от одного типа клеток, которые будут трансформироваться, к другому, в которые превратятся первые в результате трансформации.

.. figure:: /images/Physicell/Physicell_model_development/Transformation_reaction.png
   :width: 80%
   :alt: Transformation_reaction
   :align: center

:raw-html:`<br>`
Чтобы настроить параметры созданной трансформации, нужно нажать ПКМ на стрелку на диаграмме, обозначающую данную трансформацию, и в раскрывающемся списке нажать ЛКМ на кнопку **Edit**.

После этого в появившемся окне необходимо задать параметры изменяемой трансформации:

.. figure:: /images/Physicell/Physicell_model_development/Transformation_parameters.png
   :width: 80%
   :alt: Transformation_parameters
   :align: center

:raw-html:`<br>`

- **Title**: название трансформации,
- **Comment**: комментарий,
- **Cell type**: название типа клеток, к которому будут принадлежать клетки, возникающие в результате трансформации (:raw-html:`<span style="color: red;">не изменяется!</span>`),
- **Transformation rate**: скорость трансформации.

После того как заданы все параметры, нажмите **Ok**.