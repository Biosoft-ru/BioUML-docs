.. _PhysiCell_simulation_Engine_Log_model_report:

Вывод данных о модели в консоль (Log Model report)
==================================================

.. role:: raw-html(raw)
   :format: html

.. raw:: html

   <style>
   pre {
      white-space: pre-wrap !important;       /* Сохраняет пробелы, но разрешает перенос */
      word-wrap: break-word !important;       /* Переносит длинные слова */
      overflow-wrap: break-word !important;   /* Альтернатива для совместимости */
      hyphens: auto !important;               /* Перенос с тире */
   }
   </style>

.. |icon_option| image:: /images/icons/option.png

Если опция |icon_option| **Log Model report** НЕ включена, то при проведении симуляции в области вывода логов будет отображаться информация следующего вида:

.. code-block:: console
   :caption: Log Model report ☐

   INFO :  Analysis 'Simulation analysis' added to queue
   INFO :  Analysis 'Simulation analysis' started
   INFO :  [ 17:19:04 ] 	Elapsed	0.093	Time:	0	Cells	50
   INFO :  [ 17:19:04 ] 	Elapsed	0.248	Time:	10	Cells	50
   INFO :  [ 17:19:04 ] 	Elapsed	0.574	Time:	20	Cells	50
   INFO :  [ 17:19:05 ] 	Elapsed	0.843	Time:	30	Cells	50
   INFO :  [ 17:19:05 ] 	Elapsed	1.161	Time:	40	Cells	50
   INFO :  [ 17:19:05 ] 	Elapsed	1.426	Time:	50	Cells	50
   INFO :  [ 17:19:05 ] 	Elapsed	1.701	Time:	60	Cells	50
   INFO :  [ 17:19:06 ] 	Elapsed	1.966	Time:	70	Cells	50
   INFO :  [ 17:19:06 ] 	Elapsed	2.24	Time:	80	Cells	50
   INFO :  [ 17:19:06 ] 	Elapsed	2.523	Time:	90	Cells	50
   INFO :  [ 17:19:07 ] 	Elapsed	2.798	Time:	100	Cells	50
   INFO :  Analysis 'Simulation analysis' finished (3.01 s)

То есть будет указано, что задача (в данном случае, Simulation analysis) добавлена в очередь на выполнение:

.. code-block:: console

   INFO :  Analysis 'Simulation analysis' added to queue

То, что задача началась:

.. code-block:: console

   INFO :  Analysis 'Simulation analysis' started

Информация о каждом шаге симуляции модели:

.. code-block:: console

   INFO :  [ 17:19:04 ] 	Elapsed	0.093	Time:	0	Cells	50

А именно:

- Время, когда данный шаг завершился ([ 17:19:04 ]).
- Сколько всего прошло времени с момента начала выполнения задачи (Elapsed	0.093).
- Модельное время на данном шаге симуляции (Time:	0).
- Общее количество клеток в модели на данном шаге симуляции (Cells	50).

И то, что задача завершилась, а также ее общее время выполнения:

.. code-block:: console

   INFO :  Analysis 'Simulation analysis' finished (3.01 s)

Если опция |icon_option| **Log Model report** включена, то при проведении симуляции в области вывода логов будет отображаться информация следующего вида:

.. code-block:: console
   :caption: Log Model report ☑

   INFO :  Analysis 'Simulation analysis' added to queue
   INFO :  Analysis 'Simulation analysis' started
   INFO :  [ 18:06:06 ] ================================
   Simulation Options
   ================================
	   Maximum Time: 100.0	Save interval 0.0	Seed -45786084958200968	Cell update: Parallel	Diffusion: Implicit 3-D LOD with Thomas Algorithm

   ================================
   Microenvironment summary: unnamed:
   ================================

   Uniform Cartesian Mesh
   --------------------------------
	   [-500.0,500.0]x[-500.0,500.0]x[-10.0,10.0] micron
	   Resolution: dx = 20.0,	voxels: 2500,	voxel faces: 0,	volume: 2.0E7

   Densities: (1 total)
   --------------------------------
	   0. Substrate:	initial: 10.0	diffusion: 10.0	decay: 0.5

   Cell Types: ( 1 total)
   --------------------------------
	   0. CellDefinition # 50

   ================================
	   CellDefinition (0)
   ================================

   Cycle Model: Live (5)
   --------------------------------
	   Live* -> Live*, duration: 1389.0 min

   Death models: 
   --------------------------------
	   0 : Apoptosis (100), rate 5.316666666666667E-5 1/min
		   Apoptotic -> Debris, duration 516.0 min
	   1 : Necrosis (101), rate 0.0 1/min
		   Necrotic (swelling) -> Necrotic (lysed), duration 0.0 min
		   Necrotic (lysed) -> Debris, duration 86400.0 min

   Motility
   --------------------------------
	   In 3D, speed: 5.0 micron/min, bias: 0.5, persistence: 1.0 min

   Secretion:
   --------------------------------
	   Secretes Substrate, rate 5.0

   Interactions Disabled.
   --------------------------------

   Transformations Disabled.
   --------------------------------

   Mechanics:
   --------------------------------
	   cell_cell_adhesion_strength: 0.4
	   cell_cell_repulsion_strength: 10.0
	   rel max adhesion dist: 1.25
	   cell_BM_adhesion_strength: 4.0
	   cell_BM_repulsion_strength: 100.0
	   attachment_elastic_constant: 0.01
	   attachment_rate: 0.0
	   detachment_rate: 0.0

   Volume:
   --------------------------------
	   total volume: 2494.0
	   nuclear: 540.0
	   fluid fraction: 0.75
	   fluid change rate: 0.05
	   cytoplasmic biomass change_rate: 0.0045000000000000005
	   nuclear biomass_change rate: 0.0055000000000000005
	   calcification rate: 0.0
	   relative rupture volume: 4988.0

   Key functions: 
   --------------------------------
	   Custom rule: Avoid microenvironment boundaries
	   Phenotype rule: Default O2-based phenotype: cell division and necrosis are based on oxygen density
	   Volume update function: Standard volume update.
	   Mechanics function: Standard velocity: cell-cell adhesion + biased motility

   Custom data: 
   --------------------------------
	   A: 1.0 

   ================================
   Global parameters
   ================================
   INFO :  [ 18:06:06 ] 	Elapsed	0.068	Time:	0	Cells	50
   INFO :  [ 18:06:06 ] 	Elapsed	0.369	Time:	10	Cells	50
   INFO :  [ 18:06:07 ] 	Elapsed	0.746	Time:	20	Cells	50
   INFO :  [ 18:06:07 ] 	Elapsed	1.085	Time:	30	Cells	50
   INFO :  [ 18:06:07 ] 	Elapsed	1.396	Time:	40	Cells	50
   INFO :  [ 18:06:08 ] 	Elapsed	1.698	Time:	50	Cells	50
   INFO :  [ 18:06:08 ] 	Elapsed	2.012	Time:	60	Cells	50
   INFO :  [ 18:06:08 ] 	Elapsed	2.286	Time:	70	Cells	50
   INFO :  [ 18:06:09 ] 	Elapsed	2.572	Time:	80	Cells	50
   INFO :  [ 18:06:09 ] 	Elapsed	2.909	Time:	90	Cells	50
   INFO :  [ 18:06:09 ] 	Elapsed	3.202	Time:	100	Cells	50
   INFO :  Analysis 'Simulation analysis' finished (3.522 s)

.. important::
   Выводимые данные можно поменять, указав пользовательский java-код в поле **global report** в подвкладке **Model report** вкладки **Microenvironment**, предварительно отметив ☑ напротив **Custom global report**.

То есть, помимо основной информации о симуляции, которая отображается при выключенной опции Log Model report, будут также выводиться краткая информация о всей модели.

Также краткую информацию о всей модели можно просмотреть, не запуская симуляцию. Для этого нужно нажать ЛКМ на любое свободное место на диаграмме, а затем в левом нижнем углу выбрать в раскрывающемся списке **Summary**.

.. figure:: /images/Physicell/Physicell_simulation/Summary.png
   :width: 100%
   :alt: Summary
   :align: center

:raw-html:`<br>`