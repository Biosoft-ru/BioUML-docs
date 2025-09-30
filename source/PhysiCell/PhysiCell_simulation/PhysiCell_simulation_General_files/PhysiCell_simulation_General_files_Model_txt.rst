.. _PhysiCell_simulation_General_files_Model_txt:

model.txt
=========

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

В **model.txt** содержится краткая информация о всей модели.

.. code-block:: text
   :caption: Пример файла model.txt

   ================================
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
	   0. Substrate:	initial: 100.0	diffusion: 1.0E-4	decay: 0.0

   Cell Types: ( 1 total)
   --------------------------------
	   0. CellDefinition # 100

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
	   In 3D, speed: 5.0 micron/min, bias: 0.0, persistence: 2.0 min
	   Chemotaxis along 1 * ( Substrate )
	   Chemotaxis along  1.0 * ( Substrate )

   Secretion:
   --------------------------------
	   Uptakes Substrate, rate 1.0

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
	   Migration bias rule: Chemotaxis
	   Custom rule: Wrap microenvironment boundaries
	   Phenotype rule: Default O2-based phenotype: cell division and necrosis are based on oxygen density
	   Volume update function: Standard volume update.
	   Mechanics function: Standard velocity: cell-cell adhesion + biased motility

   Custom data: 
   --------------------------------

   ================================
   Global parameters
   ================================