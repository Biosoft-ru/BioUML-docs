.. _PhysiCell_microenvironment_Substrates:
   
Субстраты (Substrates)
======================

.. role:: raw-html(raw)
   :format: html

.. |icon_increase_sorting| image:: /images/icons/Physicell/increase_sorting.png
.. |icon_decrease_sorting| image:: /images/icons/Physicell/decrease_sorting.png

Во вкладке **Substrates** в табличной форме приведен список всех субстратов в модели вместе с их свойствами. 

.. figure:: /images/Physicell/Physicell_microenvironment/Substrates_menu.png
   :width: 100%
   :alt: Substrates_menu
   :align: center

:raw-html:`<br>`
На данной вкладке можно редактировать все свойства субстратов:

- **Name**: название субстрата.
- **Initial condition**: исходное количество субстрата в каждой :ref:`ячейке среды <PhysiCell_microenvironment_Domain>`.
- **Decay rate**: скорость разложения субстрата в среде.
- **Diffusion coefficient**: скорость диффузии субстрата в среде.
- **X min**: :raw-html:`граничное условие для концентрации субстрата на границе среды X = X<sub>min</sub>`.
- **X max**: :raw-html:`граничное условие для концентрации субстрата на границе среды X = X<sub>max</sub>`.
- **Y min**: :raw-html:`граничное условие для концентрации субстрата на границе среды Y = Y<sub>min</sub>`.
- **Y max**: :raw-html:`граничное условие для концентрации субстрата на границе среды Y = Y<sub>max</sub>`.
- **Z min**: :raw-html:`граничное условие для концентрации субстрата на границе среды Z = Z<sub>min</sub>`.
- **Z max**: :raw-html:`граничное условие для концентрации субстрата на границе среды Z = Z<sub>max</sub>`.

Чтобы задать значение любого параметра, нужно нажать ЛКМ в ячейку строки под соответствующим заголовком и вписать собственное значение.

Также свойства субстратов можно настраивать напрямую на диаграмме при их создании или редактировании.

.. warning::
   Добавлять и удалять новые субстраты на данной вкладке нельзя.

На данной вкладке можно сортировать субстраты по значениям любой из их характеристик. Для этого нужно нажать ЛКМ на название того столбца, по значениям которого вы хотите отсортировать субстраты.

.. figure:: /images/Physicell/Physicell_microenvironment/Substrates_sorting.png
   :width: 100%
   :alt: Substrates_sorting
   :align: center

:raw-html:`<br>`
После этого рядом с названием выбранной характеристики появится значок |icon_increase_sorting|, обозначающий сортировку от наименьшего к наибольшему. Чтобы отсортировать от наибольшего к наименьшему, нужно нажать ЛКМ на название этой же характеристики еще раз, после чего рядом с ней появится значок |icon_decrease_sorting|.