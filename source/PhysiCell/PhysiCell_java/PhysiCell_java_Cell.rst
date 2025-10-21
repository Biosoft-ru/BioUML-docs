.. _PhysiCell_java_Cell:

Cell
====

.. role:: raw-html(raw)
   :format: html

.. raw:: html

    <style>
    table {
        border-collapse: collapse;
        width: 100%;
        background-color: white;
        table-layout: fixed;
    }
    th, td {
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
        word-wrap: break-word;
        overflow-wrap: break-word;
        hyphens: auto;
        -webkit-hyphens: auto;
        -moz-hyphens: auto;
        white-space: normal;
    }
    td p {
        word-wrap: break-word;
        overflow-wrap: break-word;
        word-break: break-all;
        hyphens: auto;
        -webkit-hyphens: auto;
        -moz-hyphens: auto;
        white-space: normal;
        margin: 0; /* убираем лишние отступы, если нужно */
    }
    /* ДОБАВЬТЕ ЭТИ СТИЛИ — КЛЮЧЕВОЕ ИЗМЕНЕНИЕ! */
    .line-block,
    .line-block .line {
        white-space: normal !important;
        word-wrap: break-word !important;
        overflow-wrap: break-word !important;
        hyphens: auto !important;
        -webkit-hyphens: auto !important;
        -moz-hyphens: auto !important;
    }
    tr:nth-child(even) {
        background-color: white;
    }
    th {
        background-color: #2980B9;
        color: white;
    }
    .table-bottom-margin {
        margin-top: 20px;
    }
    </style>

Класс Cell используется для работы с отдельными агентами, т.е. клетками.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.Cell

В этом классе можно выделить 4 отдельных класса, каждый из которых используется для работы с определенной характеристикой клетки.

.. list-table::  Классы Cell
   :header-rows: 1

   * - Класс
     - Описание

   * - CellFunctions functions
     - | Используется для описания основных функций жизнедеятельности клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.1 <Physicell_java_Cell_Tbl.1.1>`.
   * - CellParameters parameters
     - | Используется для описания дополнительных встроенных параметров клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.2 <Physicell_java_Cell_Tbl.1.2>`.
   * - CellState state
     - | Используется для описания текущего состояния клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.3 <Physicell_java_Cell_Tbl.1.3>`.
   * - CustomCellData customData
     - | Используется для описания пользовательских переменных и параметров клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.4 <Physicell_java_Cell_Tbl.1.4>`.

Остальные члены класса Cell представлены в :ref:`таблице 1.5 <Physicell_java_Cell_Tbl.1.5>`.

.. _Physicell_java_Cell_Tbl.1.1:

.. list-table:: Таблица 1.1. Члены класса CellFunctions
   :header-rows: 1

   * - Член класса
     - Описание

   * - Instantiator instantiator
     - Содержит объект класса Instantiator, описывающий то, что происходит при создании новой клетки.
   * - VolumeUpdate updateVolume
     - | Содержит объект класса VolumeUpdate, описывающий, как изменяется объем клетки во время ее жизнедеятельности.
       |
       | Практически всегда используется StandardVolumeUpdate.
   * - UpdateMigrationBias updateMigration
     - | Содержит объект класса UpdateMigrationBias, описывающий целенаправленное движение клетки (например, на основе хемотаксиса).
       |
       | Примеры: Chemotaxis, Advanced Chemotaxis.
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.
   * - CustomCellRule customCellRule
     - | Содержит объект класса CustomCellRule, описывающий дополнительное правило для жизнедеятельности клетки (например, избегать границ решетки). 
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - UpdatePhenotype updatePhenotype
     - | Содержит объект класса UpdatePhenotype, описывающий, как изменяются основные внутренние параметры клетки.
       |
       | Например, "Default O2-based Phenotype" - на основе концентрации кислорода в среде.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - pre_update_intracellular pre_update_intracellular
     - | Содержит объект класса pre_update_intracellular.
       |
       | Вызывается до шага вычислений внутриклеточной ОДУ/FBA модели.
   * - post_update_intracellular post_update_intracellular
     - | Содержит объект класса post_update_intracellular.
       |
       | Вызывается после шага вычислений внутриклеточной ОДУ/FBA модели.
   * - UpdateVelocity updateVelocity
     - | Содержит объект класса UpdateVelocity, описывающий движение клетки в целом, учитывая целенаправленное и случайное движение, а также притяжение и отталкивание другими клетками.
       |
       | Практически всегда используется StandardUpdateVelocity.
   * - MembraneInteractions membraneInteraction
     - | Содержит объект класса MembraneInteractions, описывающий взаимодействие клетки с базальной мембраной.
       |
       | Пример, DomainEdgeAvoidance - устанавливает избегание базальной мембраны клетками.
   * - DistanceCalculator membraneDistanceCalculator
     - | Содержит объект класса DistanceCalculator, описывающий расчет расстояния от клетки до базальной мембраны.
       |
       | Например, DomainEdgeDistance - рассчитывает расстояние до базальной мембраны как расстояние до ближайшей границы решетки.
   * - set_orientation set_orientation
     - | Содержит объект класса set_orientation, описывающий, как устанавливается ориентация клетки в пространстве после деления.
       |
       | Например, UpOrientation - устанавливает ориентацию по оси Z.
   * - Contact contact
     - | Содержит объект класса Contact, описывающий взаимодействие между сцепленными клетками.
       |
       | Например, StandardElasticContact  -эластичное взаимодействие.
   * - CellDivision cellDivision
     - | Содержит объект класса CellDivision, описывающий, как происходит клеточное деление.
       |
       | Например, StandardAsymmetricDivision - асимметричное деление.
       |
       | Стандартное деление используется, если cellDivision не установлен (-).

.. _Physicell_java_Cell_Tbl.1.2:

.. list-table:: Таблица 1.2. Члены класса CellParameters
   :header-rows: 1

   * - Член класса
     - Описание

   * - double o2_proliferation_saturation
     - | Содержит количество кислорода, при котором он перестает усиливать пролиферацию клетки.
       |
       | Используется для клеток с :ref:`фенотипом <Physicell_cell_properties_Functions>` «Default O2-based phenotype».
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.
   * - double o2_reference
     - | Содержит референсное значение кислорода.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.

.. _Physicell_java_Cell_Tbl.1.3:

.. list-table:: Таблица 1.3. Члены класса CellState
   :header-rows: 1

   * - Член класса
     - Описание

   * - List<Cell> attachedCells
     - | Содержит список клеток, соединенных с данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double damage
     - | Содержит текущее количество повреждений, нанесенных клетке.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_TumorPhenotype_java>` использования.
   * - double simplePressure
     - | Содержит значение давления, оказываемого на клетку извне.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - List<Cell> neighbors
     - | Содержит массив клеток, являющихся соседями данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_MacrophagePhenotype_java>` использования.
   * - | int attachedCells.size()
       |
       | или
       |
       | int numberAttachedCells()
     - | Возвращают количество клеток, соединенных с данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.

.. _Physicell_java_Cell_Tbl.1.4:

.. list-table:: Таблица 1.4. Члены класса CustomCellData
   :header-rows: 1

   * - Член класса
     - Описание

   * - int findVariableIndex(String variable)
     - | variable - название переменной.
       |
       | Возвращает индекс переменной variable в списке всех переменных типа клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - double get(int index)
     - | index - индекс переменной.
       |
       | Возвращает значение переменной с индексом index для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - void set(String name, double value)
     - | name - название параметра.
       | value - значение.
       |
       | Устанавливает значение value пользовательскому параметру name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_Initial_java>` использования.

.. _Physicell_java_Cell_Tbl.1.5:

.. list-table:: Таблица 1.5. Остальные члены класса Cell
   :header-rows: 1

   * - Член класса
     - Описание

   * - Cell cell = new Cell(CellDefinition cd, Model model)
     - | cd - тип клеток.
       | model - модель.
       |
       | Конструктор, создает новую клетку cell типа cd в модели model.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.
   * - double[] position
     - | Содержит трехмерный вектор - координаты клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - double[] velocity
     - | Содержит трехмерный вектор - скорость клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - int type
     - | Содержит числовой код типа данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - int ID
     - | Содержит автоматически сгенерированный идентификатор клетки.
       |
       | :ref:`Пример <PhysiCell_java_Heterogeneity_Report_java>` использования.
   * - String typeName
     - | Содержит название типа клеток, к которому относится данная клетка.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - static void detachCells(Cell cell1, Cell cell2)
     - | cell1 - клетка.
       | cell2 - клетка.
       |
       | Расцепляет клетки cell1 и cell2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - static void attachcCells(Cell cell1, Cell cell2)
     - | cell1 - клетка.
       | cell2 - клетка.
       |
       | Сцепляет клетки cell1 и cell2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - static void createCell(CellDefinition cd, Model model, double[] position)
     - | cd - тип клеток.
       | model - модель.
       | position - координаты клетки.
       |
       | Создает клетку типа cd в модели model в точке position.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmunityEvent_java>` использования.
   * - Microenvironment getMicroenvironment()
     - | Возвращает среду, в которой сущетсвует клетка.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - double nearest_gradient(int index)
     - | index - индекс субстрата.
       |
       | Возвращает значение градиента плотности субстрата с индексом index в ближайшей к клетке ячейке решетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - void startDeath(int index)
     - | index - индекс типа клеточной смерти.
       |
       | Запускает клеточную смерть с индексом index.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - List<Cell> cells_in_my_container()
     - | Возвращает список клеток в ячейке данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - void removeAllAttachedCells()
     - | Отсоединяет все клетки, прикрепленные к данной клетке.
       |
       | :ref:`Пример <PhysiCell_java_CancerBiorobots_CargoPhenotype_java>` использования.
   * - Model getModel()
     - | Возвращает модель, в которой находится данная клетка.
       | 
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - double[] nearest_density_vector()
     - | Возвращает массив плотностей всех субстратов в ячейке решетки, где находится данная клетка.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - void ingestCell(Cell cell)
     - | cell - клетка.
       |
       | Клетка, к которой был применен данный метод, поглощает клетку cell.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PredatorPhenotype_java>` использования.
   * - double nearestGradient(String substrate)
     - | substrate - название субстрата.
       |
       | Возвращает градиент субстрата substrate в ячейке решетки, в которой находится данная клетка.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_WeightedMotility_java>` использования.
   * - void lyseCell()
     - | Активирует лизис данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Epithelial_java>` использования.
   * - int get_current_mechanics_voxel_index()
     - | Возвращает номер ячейки, в которой находится данная клетка.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - CellContainer get_container()
     - | Возвращает объект, обрабатывающий положение данной клетки в решетке.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - static boolean isNeighborVoxel(Cell cell, double[] coordinates, double[] center, int index)
     - | cell - клетка.
       | coordinates - координаты клетки.
       | center - центр ячейки среды.
       | index - индекс ячейки среды.
       |
       | Возвращает true, если ячейка среды с индексом index с центром в точке center является соседней* с клеткой cell, находящейся в точке coordinates.
       |
       | \*Под соседством подразумевается, что клетка может взаимодействовать с клетками в этих ячейках.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - List<Cell> nearby_interacting_cells()
     - | Возвращает массив клеток, являющихся соседями и находящихся достаточно близко для взаимодействия с данной клеткой. 
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.