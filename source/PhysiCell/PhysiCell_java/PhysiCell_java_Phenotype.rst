.. _PhysiCell_java_Phenotype:

Phenotype
=========

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

.. note::
   Класс **Phenotype** является вложенным объектом внутри классов **Cell** и **CellDefinition**.

Класс Phenotype используется для работы с различными свойствами клеток.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.Phenotype

В этом классе можно выделить 12 отдельных классов, каждый из которых используется для работы с определенным набором свойств клетки.

.. list-table:: Классы Phenotype
   :header-rows: 1

   * - Класс
     - Описание

   * - Cycle cycle
     - | Используется для описания жизненного цикла клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.1 <Physicell_java_Phenotype_Tbl.1.1>`.
   * - Death death
     - | Используется для описания модели смерти клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.2 <Physicell_java_Phenotype_Tbl.1.2>`.
   * - Volume volume
     - | Используется для описания объемных свойств клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.3 <Physicell_java_Phenotype_Tbl.1.3>`.
   * - Geometry geometry
     - | Используется для описания размеров клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.4 <Physicell_java_Phenotype_Tbl.1.4>`.
   * - Mechanics mechanics
     - | Используется для описания механических свойств клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.5 <Physicell_java_Phenotype_Tbl.1.5>`.
   * - Motility motility
     - | Используется для описания подвижности клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.6 <Physicell_java_Phenotype_Tbl.1.6>`.
   * - Secretion secretion
     - | Используется для описания секреции и потребления веществ клеткой.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.7 <Physicell_java_Phenotype_Tbl.1.7>`.
   * - Molecular molecular
     - | Используется для описания содержания веществ внутри клетки.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.8 <Physicell_java_Phenotype_Tbl.1.8>`.
   * - CellInteractions cellInteractions
     - | Используется для описания взаимодействия между клетками разных типов.
   * - CellTransformations cellTransformations
     - | Используется для описания трансформации клетки из одного типа в другой.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.10 <Physicell_java_Phenotype_Tbl.1.10>`.
   * - Intracellular intracellular
     - | Используется для описания внутриклеточных процессов клетки с помощью обыкновенных дифференциальных уравнений или потоковой модели.
       |
       | Все члены данного класса представлены в :ref:`таблице 1.11 <Physicell_java_Phenotype_Tbl.1.11>`.
   * - CellIntegrity cellIntegrity
     - | Используется для описания целостности клетки.

.. _Physicell_java_Phenotype_Tbl.1.1:

.. list-table:: Таблица 1.1. Члены класса Cycle
   :header-rows: 1

   * - Член класса
     - Описание

   * - int code
     - | Содержит численный код жизненного цикла клетки.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Report_java>` использования.
   * - Phase currentPhase()
     - | Возвращает текущую фазу жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - int currentPhase().code
     - | Содержит численный код текущей фазы жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - int currentPhase().index
     - | Содержит внутренний текущей фазы жизненного цикла данной клетки.
   * - boolean currentPhase().divisionAtExit
     - | Содержит true, если клетка делится при выходе из данной фазы клеточного цикла.
   * - boolean currentPhase().removalAtExit
     - | Содержит true, если клетка исчезает при выходе из данной фазы клеточного цикла.
   * - String currentPhase().name
     - | Содержит название текущей фазы жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - CycleData data
     - | Содержит объект класса CycleData, хранящий численные данные жизненного цикла данной конкретной клети.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - double data.elapsedTimePhase
     - | Содержит время, проведенное клеткой в текущей фазе жизненного цикла.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - double data.getTransitionRate(int phase1, int phase2)
     - | phase1 - номер фазы жизненного цикла.
       | phase2 - номер фазы жизненного цикла.
       |
       | Возвращает скорость перехода между фазами жизненного цикла с номерами phase1 и phase2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - void data.setTransitionRate(int phase1, int phase2, double speed)
     - | phase1 - номер фазы жизненного цикла.
       | phase2 - номер фазы жизненного цикла.
       | speed - скорость перехода между фазами жизненного цикла.
       |
       | Устанавливает скорость перехода между фазами жизненного цикла с номерами phase1 и phase2, равную speed.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - double data.getExitRate(int phase)
     - | phase - номер фазы жизненного цикла.
       |
       | Возвращает вероятность выхода из фазы под номером phase*.
       |
       | \*Используется, если клетка может перейти из фазы phase только в одну другую фазу.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - void data.setExitRate(int phase, double probability)
     - | phase - номер фазы жизненного цикла.
       | probability - вероятность.
       |
       | Устанавливает вероятность выхода из фазы с номером phase равной probability.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.2:

.. list-table:: Таблица 1.2. Члены класса Death
   :header-rows: 1

   * - Член класса
     - Описание

   * - boolean dead
     - | Содержит true, если клетка мертва.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double[] rates
     - | Содержит массив вероятностей всех типов клеточных смертей.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeB_java>` использования.
   * - int rates.size()
     - | Возвращает количество вероятностей всех возможных клеточных смертей.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_Initial_java>` использования.
   * - void rates.set(int index, double probability)
     - | index - индекс типа клеточной смерти.
       | probability - вероятность.
       |
       | Устанавливает вероятность типа клеточной смерти с индексом index равной probability.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_Initial_java>` использования.
   * - double rates.get(int index)
     - | index - индекс типа клеточной смерти.
       |
       | Возвращает вероятность типа клеточной смерти с индексом index.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - int findDeathModelIndex(String name)
     - | name - название типа клеточной смерти.
       |
       | Возвращает индекс типа клеточной смерти с названием name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.3:

.. list-table:: Таблица 1.3. Члены класса Volume
   :header-rows: 1

   * - Член класса
     - Описание

   * - double total
     - | Содержит значение общего объема клетки.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.4:

.. list-table:: Таблица 1.4. Члены класса Geometry
   :header-rows: 1

   * - Член класса
     - Описание

   * - double radius
     - | Содержит радиус клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.5:

.. list-table:: Таблица 1.5. Члены класса Mechanics
   :header-rows: 1

   * - Член класса
     - Описание

   * - double attachmentElasticConstant
     - | Содержит коэффициент, с которым клетка притягивается к другим клеткам.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.
   * - double cellCellAdhesionStrength
     - | Содержит силу межклеточной адгезии.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double cellCellRepulsionStrength
     - | Содержит силу межклеточного отталкивания.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double relDetachmentDistance
     - | Содержит относительное расстояние (множитель радуиса), на котором клетка отделяется от прикрепленной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.6:

.. list-table:: Таблица 1.6. Члены класса Motility
   :header-rows: 1

   * - Член класса
     - Описание

   * - boolean isMotile
     - | Содержит true, если клетка подвижна.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double migrationBias
     - | Содержит число из интервала [0,1], где 0 обозначает, что клетка движется абсолютно случайно, а 1 - полностью целенаправленно.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - double[] migrationBiasDirection
     - | Содержит :ref:`нормализованный <PhysiCell_java_Normalization>` вектор, описывающий направление, в котором клетка движется целенаправленно в данный момент времени.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - double migrationSpeed
     - | Содержит скорость движения клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - double persistenceTime
     - | Содержит время, в течение которого клетка сохраняет одно направление движения.
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.
   * - int chemotaxisDirection
     - | Содержит "1", если клетка движется к субстрату во время хемотаксиса, или "-1", если клетка движется от него.
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.7:

.. list-table:: Таблица 1.7. Члены класса Secretion
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] secretionRates
     - | Содержит массив скоростей секреции каждого из субстратов данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - double[] uptakeRates
     - | Содержит массив скоростей потребления каждого из субстратов данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double[] netExportRates
     - | Содержит массив, содержащий скорости постоянной (не зависящей от объема клетки) секреции/потребления всех возможных субстратов для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - void setSecretionToZero()
     - | Устанавливает скорость секреции, равной 0, для всех субстратов в модели для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - void setUptakeToZero()
     - | Устанавливает скорость потребления, равной 0, для всех субстратов в модели для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.8:

.. list-table:: Таблица 1.8. Члены класса Molecular
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] internSubstrates
     - | Содержит массив, состоящий из количества всех возможных веществ внутри клетки.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Initial_java>` использования.
   * - double fractionReleasedDeath
     - | Содержит долю внутренних веществ, которая выбрасывается из клетки в момент ее гибели.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_EpithelialInstantiator_java>` использования.
   * - double fractionTransferredIngested
     - | Содержит долю внутренних веществ, которую получает клетка, поглотившая клетку данного типа.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_EpithelialInstantiator_java>` использования. 
   
.. _Physicell_java_Phenotype_Tbl.1.10:

.. list-table:: Таблица 1.10. Члены класса CellTransformations
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] transformationRates
     - | Содержит массив вероятностей трансформации клеток данного типа во все остальные типы клеток.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_StemPhenotype_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.11:

.. list-table:: Таблица 1.11. Члены класса Intracellular
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - void start()
     - | Запускает расчеты внитриклеточной модели.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Initial_java>` использования.
   * - void setParameterValue(String name, double value)
     - | name - название параметра внутриклеточной модели.
       | value - значение.
       |
       | Устанавлиает численное значение value параметру name во внутриклеточной модели.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Initial_java>` использования.
   * - double getParameterValue(String name)
     - | name - название параметра внутриклеточной модели.
       |
       | Возвращает значение параметра name во внутриклеточной модели.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_ODEVisualizer_java>` использования.