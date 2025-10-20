.. _PhysiCell_development_Secretion:

Создание секреции/потребления
=============================

.. |icon_secretion| image:: /images/icons/Physicell/secretion_corrected.png

При секреции клетка выделяет субстрат в среду, а при потреблении - поглощает его из среды.

Чтобы создать в модели секрецию/потребление, нужно:

1. Нажать ЛКМ на значок |icon_secretion| на панели инструментов.
2. Нажать ЛКМ на тип клеток, который будут выделять/поглощать определенный субстрат.
3. Нажать ЛКМ на субстрат, который клетки выбранного типа будут выделять/потреблять.

.. figure:: /images/Physicell/Physicell_model_development/Secretion_creation.png
   :width: 80%
   :alt: Secretion_creation
   :align: center

:raw-html:`<br>`
После этого на диаграмме появится стрелочка серого цвета, направленная от типа клеток к субстрату.

.. figure:: /images/Physicell/Physicell_model_development/Secretion_reaction.png
   :width: 80%
   :alt: Secretion_reaction
   :align: center

:raw-html:`<br>`
Чтобы настроить параметры созданной секреции/потребления, нужно нажать ПКМ на стрелку на диаграмме, обозначающую данную секрецию/потребление, и в раскрывающемся списке нажать ЛКМ на кнопку **Edit**.

.. figure:: /images/Physicell/Physicell_model_development/Edit_reaction.png
   :width: 80%
   :alt: Edit_reaction
   :align: center

:raw-html:`<br>`
После этого в появившемся окне необходимо задать параметры изменяемой секреции/потребления:

.. figure:: /images/Physicell/Physicell_model_development/Secretion_parameters.png
   :width: 80%
   :alt: Secretion_parameters
   :align: center

:raw-html:`<br>`

- **Title**: название секреции/потребления,
- **Comment**: комментарий,
- **Substrate**: название выделяемого/потребляемого субстрата (:raw-html:`<span style="color: red;">не изменяется!</span>`),
- **Secretiom Rate**: скорость секреции вещества,
- **Secretiom Target**: значение «насыщения», при котором прекращается секреция,
- **Uptake Rate**: скорость потребления вещества,
- **Net export rate**: постоянный уровень секреции/потребления субстрата, не зависящий от объема клетки.

.. warning::
   Положительные значения параметра Net export rate соответствуют постоянной секреции, а отрицательные - постоянному потреблению.

После того как заданы все параметры, нажмите **Ok**.

Ниже представлена формула расчета изменения концентрации субстрата (p) в трехмерной ячейке решетки одной клеткой за единицу времени dt:

.. math::

   p(t+dt) = \frac{p(t) + D * (V_{\mathrm{cell}} / V) * S * T}{1 + D * (V_{\mathrm{cell}} / V) * (S + U)} \, + \, D \, * \frac{E}{V},

где:

- D - Diffusion dt из настроек :ref:`симуляции <PhysiCell_simulation_Engine>`,
- :raw-html:`V<sub>cell</sub>` - :ref:`объем клетки <PhysiCell_cell_properties_Volume>`,
- V - :ref:`объем ячейки среды <PhysiCell_microenvironment_Domain>`,
- S - скорость секреции вещества (Secretion Rate),
- T - значение «насыщения», при котором прекращается секреция (Secretiom Target),
- U - скорость потребления вещества (Uptake Rate),
- E  - постоянный уровень секреции/потребления субстрата, не зависящий от объема клетки (Net export rate).

В случаях, когда все параметры секреции/потребления, кроме **Net export rate** (S, T и U), имеют нулевые значения, то формулу можно упростить до следующего вида:

.. math::

   p(t+dt) = p(t) + \, D \, * \frac{E}{V}.