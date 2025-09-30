.. _PhysiCell_simulation_result_Settings:

Параметры настройки просмотра симуляции
=======================================

.. role:: raw-html(raw)
   :format: html

Редактировать можно следующие параметры просмотра симуляции:

- **Time**: :ref:`модельное время симуляции <PhysiCell_simulation_result_Settings_Time>`,
- **Time step**: :ref:`шаг модельного времени симуляции <PhysiCell_simulation_result_Settings_Time_step>`,
- **2D**: отметьте ☑, если хотите, чтобы изображение модели выводилось в :ref:`двух измерениях <PhysiCell_simulation_result_Settings_2D>`,
- **Options 2D**: опции просмотра модели в двух измерениях (:raw-html:`<span style="color: red;">доступно, только если выбрана опция 2D</span>`):

   - *Slice* - сечение внешней среды для просмотра симуляции,
   - *Section* - плоскость для просмотра симуляции,

- **Options 3D**: опции просмотра модели в :ref:`трех измерениях <PhysiCell_simulation_result_Settings_Options_3D>` (:raw-html:`<span style="color: red;">доступно, только если НЕ выбрана опция 2D</span>`):

   - *Heading* - угол поворота вокруг оси Y,
   - *Pitch* - угол поворота вокруг оси X,
   - *YZ slice, X =*: на каком расстоянии от точки X = 0 делать сечение по плоскости YZ,
   - *XZ slice, Y =*: на каком расстоянии от точки Y = 0 делать сечение по плоскости XZ,
   - *XY slice, Z =*: на каком расстоянии от точки Z = 0 делать сечение по плоскости XY,
   - *Density XY plane*: отметьте ☑, если хотите отображать субстраты в плоскости XY,
   - *Density XZ plane*: отметьте ☑, если хотите отображать субстраты в плоскости XZ,
   - *Density YZ plane*: отметьте ☑, если хотите отображать субстраты в плоскости YZ,
   - *Spheres quality*: качество рендеринга трехмерных сфер (клеток).

- **Statistics**: отметьте ☑, если хотите, чтобы отрисовывалась :ref:`дополнительная информация о модели <PhysiCell_simulation_result_Settings_Statistics>`,
- **Axes**: отметьте ☑, если хотите, чтобы на изображении модели отрисовывались :ref:`оси <PhysiCell_simulation_result_Settings_Axes>`,
- **Cells**: отметьте ☑, если хотите, чтобы на изображении модели отрисовывались :ref:`клетки <PhysiCell_simulation_result_Settings_Cells>`,
- **Draw nuclei**: отметьте ☑, если хотите, чтобы на изображении модели в клетках отрисовывались :ref:`ядра <PhysiCell_simulation_result_Settings_Draw_nuclei>`,
- **Substrate name**: название субстрата,
- **Substrate**: отметьте ☑, если хотите отображать :ref:`субстрат <PhysiCell_simulation_result_Settings_Substrate>`, выбранный в поле Substrate name, на изображении модели (:raw-html:`<span style="color: red;">проверьте, что при запуске симуляции было отмечено поле Save density, иначе субстраты не будут отображаться</span>`),
- **Density Color**: цвет, с помощью которого субстрат, выбранный в поле Substrate name, быдет вырисовываться на изображении модели,
- **Statistics X**: :ref:`координаты <PhysiCell_simulation_result_Settings_Statistics_XY>` отрисовки дополнительной информации о модели по оси X,
- **Statistics Y**: :ref:`координаты <PhysiCell_simulation_result_Settings_Statistics_XY>` отрисовки дополнительной информации о модели по оси Y,
- **Frame per second**: количество кадров в секунду в видео,
- **Result video path**: путь до директории для сохранения :ref:`видео <PhysiCell_simulation_result_Settings_Video>`.

Далее рассмотрим некоторые из этих параметров более подробно.

.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Time
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Time_step
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_2D
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Options_3D
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Statistics
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Axes
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Cells
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Draw_nuclei
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Substrate
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Statistics_XY
   PhysiCell_simulation_result_Settings/PhysiCell_simulation_result_Settings_Video
