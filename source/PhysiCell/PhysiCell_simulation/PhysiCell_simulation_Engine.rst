.. _PhysiCell_simulation_Engine: 

Область редактирования параметров симуляции модели (Engine)
===========================================================

.. role:: raw-html(raw)
   :format: html

При переключении на вкладку Engine в области редактирования можно будет настроить следующие параметры:

.. figure:: /images/Physicell/Physicell_simulation/Engine_parameters_full_list.png
   :width: 60%
   :alt: Engine_parameters_full_list
   :align: center

:raw-html:`<br>`

- **Simulator name**: :ref:`численный решатель <PhysiCell_simulation_Engine_Simulator_name>`,
- **Log Model report**: отметьте ☑, если хотите выводить :ref:`данные о модели в консоль перед началом расчетов <PhysiCell_simulation_Engine_Log_model_report>`,
- **Result path**: путь в репозитории модуля для :ref:`сохранения результатов <PhysiCell_simulation_Engine_Result_path>`,
- **Max Time**: модельное время, до которого будет продолжаться симуляция,
- **Parallel diffusion simulation**: отметьте ☑, если хотите использовать распараллеливание расчетов при моделировании процессов диффузии веществ,
- **Cell update type**: :ref:`способ расчета поведения отдельных клеток <PhysiCell_simulation_Engine_Cell_update_type>`,
- **Diffusion dt**: шаг модельного времени для расчета диффузии веществ,
- **Mechanics dt**: шаг модельного времени, с которым происходит взаимодействие клеток друг с другом и с веществами в среде,
- **Phenotype dt**: шаг модельного времени, с которым происходит обновление внутреннего состояния клеток,
- **Report interval**: шаг модельного времени, с которым выводится табличный отчет о состоянии модели при симуляции,
- **Image interval**: шаг модельного времени, с которым сохраняется визуальное отображение модели при симуляции,
- **Save report**: отметьте ☑, если хотите :ref:`сохранять таблицы <PhysiCell_simulation_Engine_Save_report>`,
- **Save cells data**: отметьте ☑, если хотите сохранять :ref:`данные о клетках в текстовых файлах <PhysiCell_simulation_Engine_Save_cells_data>`,
- **Save cells data as table**: отметьте ☑, если хотите сохранять :ref:`данные о клетках в таблицах <PhysiCell_simulation_Engine_Save_cells_data_as_table>`,
- **Save density**: отметьте ☑, если хотите сохранять :ref:`данные о веществах <PhysiCell_simulation_Engine_Save_density>`,
- **Save images**: отметьте ☑, если хотите сохранять :ref:`изображения модели в процессе симуляции <PhysiCell_simulation_Engine_Save_images>`,
- **Save GIF**: отметьте ☑, если хотите сохранять :ref:`GIF-изображение модели в процессе симуляции <PhysiCell_simulation_Engine_Save_GIF>`,
- **Save Video**: отметьте ☑, если хотите сохранять :ref:`видео модели в процессе симуляции <PhysiCell_simulation_Engine_Save_video>`,
- **Save plots**: отметьте ☑, если хотите :ref:`сохранять графики <PhysiCell_simulation_Engine_Save_plots>`,
- **Use manual seed**: отметьте ☑, если хотите использовать пользовательский seed для случайных процессов модели,
- **Manual seed**: пользовательский seed для случайных процессов модели,
- **Recalculate gradients**: отметьте ☑, если хотите пересчитывать градиенты веществ во время симуляции модели,
- **Track inner substrates in cells**: отметьте ☑, если хотите отслеживать содержание веществ внутри клеток во время симуляции модели,
- **Model type**: :ref:`тип модели <PhysiCell_simulation_Engine_Model_type>`.

.. note::
   Для симуляции диаграмм типа Physicell всегда используются свойства численного метода PhysicellSimulationEngine (не редактируется).

Далее мы рассмотрим некоторые параметры вкладки Engine более подробно.

.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Simulator_name
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Log_model_report
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Result_path
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Cell_update_type
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_report
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_cells_data
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_cells_data_as_table
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_density
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_images
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_GIF
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_video
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Save_plots
   PhysiCell_simulation_Engine/PhysiCell_simulation_Engine_Model_type
   