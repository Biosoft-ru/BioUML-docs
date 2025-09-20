.. _PhysiCell_cell_properties_Intracellular:

Внутриклеточная модель клетки (Intracellular)
=============================================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_add_new| image:: /images/icons/Physicell/add_new.png

Чтобы задать внутриклеточные механизмы для клеток выбранного типа, можно применять SBML-модель, использующую обыкновенные дифференциальные уравнения, алгебраические уравнения и дискретные события. Данная модель может использовать в качестве параметров свойства клетки, количество потребленных и выделенных ей веществ, а также может менять значения самого свойства клетки.

После нажатия на вкладку **Intracellular** на панели свойств справа у вас появится меню, в котором напротив поля |icon_option| **Diagram** можно указать путь до SBML-модели, которая будет описывать поведение внутри клеток выбранного типа.

.. figure:: /images/Physicell/Physicell_cell_properties/Intracellular_menu.png
   :width: 100%
   :alt: Intracellular_menu
   :align: center

:raw-html:`<br>`
Чтобы указать путь до SBML-модели, нужно нажать ЛКМ на |icon_option| **(select element)** и в появившемся меню указать, где в вашем репозитории находится SBML-модель.

.. figure:: /images/Physicell/Physicell_cell_properties/SBML_model_path.png
   :width: 100%
   :alt: SBML_model_path
   :align: center

:raw-html:`<br>`
После этого у вас появятся два новых поля:

.. figure:: /images/Physicell/Physicell_cell_properties/New_fields_intracellular.png
   :width: 100%
   :alt: New_fields_intracellular
   :align: center

:raw-html:`<br>`

- **Variables**: список соответствий между переменными SBML-модели и свойствами клетки,
- **engine**: свойства численного метода.

Ниже разберем как редактировать каждое из этих полей.

Список соответствий между переменными SBML-модели и свойствами клетки (Variables)
---------------------------------------------------------------------------------

Чтобы добавить соответствие между одной переменной SBML-модели и одним свойством клетки, нужно:

1. Нажать ЛКМ на |icon_option| **Variables**.
2. Нажать ЛКМ на иконку |icon_add_new|.

.. figure:: /images/Physicell/Physicell_cell_properties/New_correspondance.png
   :width: 100%
   :alt: New_correspondance
   :align: center

:raw-html:`<br>`
Таким образом можно добавить сколько угодно соответствий.

После этого под |icon_option| **Variables** появится новая вкладка, в которой можно редактировать три параметра:

.. figure:: /images/Physicell/Physicell_cell_properties/Variable_phenotype_property_type.png
   :width: 100%
   :alt: Variable_phenotype_property_type
   :align: center

:raw-html:`<br>`

- **Variable**: название переменной SBML-модели, в соответствие которой мы хотим задать то или иное свойство клетки,
- **Phenotype property**: название свойства клетки, соответствующего выбранной переменной,
- **Type**: тип соответствия.

Чтобы указать значение каждого из этих трех параметров, нужно нажать ЛКМ справа от соответствующего поля (**Variable**, **Phenotype property** или **Type**) и из раскрывающегося списка выбрать нужное значение.

.. figure:: /images/Physicell/Physicell_cell_properties/Variable_selection.png
   :width: 100%
   :alt: Variable_selection
   :align: center

:raw-html:`<br>`
В раскрывающихся списках напротив полей |icon_option| **Variable** и |icon_option| **Phenotype property** можно найти любой параметр выбранной SBML-модели и любое свойство выбранного типа клеток, соответственно.

В раскрывающемся списке напротив |icon_option| **Type** всегда можно выбрать один из 3-ех типов соответствия:

- **Input**: значение определяется PhysiCell-моделью и SBML-модель никак на него не влияет; она только использует его в качестве значения одного из своих параметров.
- **Output**: значение определяется SBML-моделью и PhysiCell-модель никак на него не влияет; она только использует его в качестве значения одного из свойств клетки.
- **Contact**: значение определяется в обеих моделях: SBML и PhysiCell.

Для работы с уже существующими соответствиями используйте :ref:`этот функционал <Physicell_cell_properties_Actions>`.

Свойства численного метода (engine)
-----------------------------------

Свойства численного метода используются для решения SBML-модели.

Внутри вкладки **engine** можно редактировать значения следующих параметров:

.. figure:: /images/Physicell/Physicell_cell_properties/Engine_parameters.png
   :width: 100%
   :alt: Engine_parameters
   :align: center

:raw-html:`<br>`

- **Selected engine**: математический формализм, в рамках которого происходит численное решение SBML-модели,
- **Time increment**: размер шага симуляции SBML-модели,
- **Simulator**: численный решатель, используемый при симуляции SBML-модели,
- **Simulator options**: параметры численного решателя.

Чтобы выбрать математический формализм (Selected engine) или численный решатель для симуляции SBML-модели (Simulator), нужно нажать ЛКМ справа от иконки |icon_option| **Selected engine** или |icon_option| **Simulator**, соответственно, и из раскрывающегося списка выбрать один из доступных вариантов.

.. figure:: /images/Physicell/Physicell_cell_properties/Engine_selection.png
   :width: 100%
   :alt: Engine_selection
   :align: center

:raw-html:`<br>`
Чтобы указать размер шага симуляции SBML-модели (Time increment), нужно нажать ЛКМ справа от иконки |icon_option| **Time increment** и вписать собственное значение.

.. figure:: /images/Physicell/Physicell_cell_properties/Edit_time_increment.png
   :width: 100%
   :alt: Edit_time_increment
   :align: center

:raw-html:`<br>`
Чтобы редактировать параметры выбранного численного решателя (Simulator options), нужно раскрыть вкладку **Simulator options** и справа от названия параметра вписать собственное значение, выбрать предложенное значение из раскрывающегося списка или отметить ☑.

.. figure:: /images/Physicell/Physicell_cell_properties/Simulator_options.png
   :width: 100%
   :alt: Simulator_options
   :align: center

:raw-html:`<br>`

.. important::
   - Для каждого численного решателя доступен свой набор параметров для редактирования.
   - Для некоторых численных решателей параметры для редактирования отсутствуют.