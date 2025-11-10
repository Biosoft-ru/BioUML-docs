.. _PhysiCell_development_Interaction:

Создание взаимодействия
=======================

.. |icon_interaction| image:: /images/icons/Physicell/interaction_corrected.png
.. |icon_remove_element| image:: /images/icons/remove_element.png

В результате взаимодействия клетки одного типа оказывают то или иное воздействие на клетки другого типа.

Чтобы создать в модели взаимодействие, нужно:

1. Нажать ЛКМ на значок |icon_interaction| на панели инструментов.
2. Нажать ЛКМ на тип клеток, который будет тем или иным образом воздействовать на другой тип клеток.
3. Нажать ЛКМ на тип клеток, над которым будет совершаться то или иное действие.

.. figure:: /images/Physicell/Physicell_model_development/Interaction_creation.png
   :width: 80%
   :alt: Interaction_creation
   :align: center

:raw-html:`<br>`
После этого на диаграмме появится стрелочка красного цвета, направленная от одного типа клеток, оказывающих воздействие, к другому, над которыми совершается действие.

.. figure:: /images/Physicell/Physicell_model_development/Interaction_reaction.png
   :width: 80%
   :alt: Interaction_reaction
   :align: center

:raw-html:`<br>`
Чтобы настроить параметры созданного взаимодействия, нужно нажать ПКМ на стрелку на диаграмме, обозначающую данное взаимодействие, и в раскрывающемся списке нажать ЛКМ на кнопку **Edit**.

.. figure:: /images/Physicell/Physicell_model_development/Edit_interaction.png
   :width: 80%
   :alt: Edit_interaction
   :align: center

:raw-html:`<br>`
После этого в появившемся окне необходимо задать параметры изменяемого взаимодействия:

.. figure:: /images/Physicell/Physicell_model_development/Interaction_parameters.png
   :width: 80%
   :alt: Interaction_parameters
   :align: center

:raw-html:`<br>`

- **Title**: название взаимодействия,
- **Comment**: комментарий,
- **Cell type**: название типа клеток, над которыми совершается действие (:raw-html:`<span style="color: red;">не изменяется!</span>`),
- **Attack rate**: интенсивность атаки,
- **Fuse rate**: интенсивность слияния двух клеток,
- **Phagocytosis rate**: интенсивность фагоцитоза.

.. note::
   При слияния двух клеток у результирующей клетки будет 2 ядра, а при поглощении одной клеткой другой в результате фагоцитоза у первой будет только одно ядро.

После того как заданы все параметры, нажмите **Ok**.

Чтобы удалить взаимодействие из модели, необходимо нажать на него ЛКМ и нажать клавишу **Delete**.

Если вы работаете в веб-версии BioUML, то для удаления нужно:

1. Нажать на обозначение взаимодействия ПКМ.
2. В раскрывающемся списке нажать ЛКМ на **Remove** |icon_remove_element|. 