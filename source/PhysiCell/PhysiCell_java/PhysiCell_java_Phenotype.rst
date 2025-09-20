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

В этом классе можно выделить 12 отдельных подклассов, каждый из которых используется для работы с определенным набором свойств клетки.

.. list-table:: Подклассы Phenotype
   :header-rows: 1

   * - Класс
     - Описание

   * - Cycle
     - | Используется для описания жизненного цикла клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.cycle
       |
       | Все члены данного класса представлены в :ref:`таблице 1.1 <Physicell_java_Phenotype_Tbl.1.1>`.
   * - Death
     - | Используется для описания модели смерти клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.death
       |
       | Все члены данного класса представлены в :ref:`таблице 1.2 <Physicell_java_Phenotype_Tbl.1.2>`.
   * - Volume
     - | Используется для описания объемных свойств клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.volume
       |
       | Все члены данного класса представлены в :ref:`таблице 1.3 <Physicell_java_Phenotype_Tbl.1.3>`.
   * - Geometry
     - | Используется для описания размеров клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.geometry
       |
       | Все члены данного класса представлены в :ref:`таблице 1.4 <Physicell_java_Phenotype_Tbl.1.4>`.
   * - Mechanics
     - | Используется для описания механических свойств клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.mechanics
       |
       | Все члены данного класса представлены в :ref:`таблице 1.5 <Physicell_java_Phenotype_Tbl.1.5>`.
   * - Motility
     - | Используется для описания подвижности клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.motility
       |
       | Все члены данного класса представлены в :ref:`таблице 1.6 <Physicell_java_Phenotype_Tbl.1.6>`.
   * - Secretion
     - | Используется для описания секреции и потребления веществ клеткой.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.secretion
       |
       | Все члены данного класса представлены в :ref:`таблице 1.7 <Physicell_java_Phenotype_Tbl.1.7>`.
   * - Molecular
     - | Используется для описания содержания веществ внутри клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.molecular
       |
       | Все члены данного класса представлены в :ref:`таблице 1.8 <Physicell_java_Phenotype_Tbl.1.8>`.
   * - CellInteractions
     - | Используется для описания взаимодействия между клетками разных типов.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.cellInteractions
   * - CellTransformations
     - | Используется для описания трансформации клетки из одного типа в другой.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.cellTransformations
       |
       | Все члены данного класса представлены в :ref:`таблице 1.10 <Physicell_java_Phenotype_Tbl.1.10>`.
   * - Intracellular
     - | Используется для описания внутриклеточных процессов клетки с помощью обыкновенных дифференциальных уравнений или потоковой модели.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.intracellular
       |
       | Все члены данного класса представлены в :ref:`таблице 1.11 <Physicell_java_Phenotype_Tbl.1.11>`.
   * - CellIntegrity
     - | Используется для описания целостности клетки.
       |
       | Для вызова объекта данного класса используйте:
       | Phenotype.cellIntegrity

.. _Physicell_java_Phenotype_Tbl.1.1:

.. list-table:: Таблица 1.1. Члены класса Cycle
   :header-rows: 1

   * - Член класса
     - Описание

   * - int code
     - | Возвращает численный код жизненного цикла клетки.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Report_java>` использования.
   * - currentPhase()
     - | Возвращает текущую фазу жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - int currentPhase().code
     - | Возвращает численный код текущей фазы жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerImmunityVisualizer_java>` использования.
   * - String currentPhase().name
     - | Возвращает название текущей фазы жизненного цикла данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - CycleData data
     - | Возвращает объект класса CycleData, хранящий численные данные жизненного цикла данной конкретной клети.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - double data.elapsedTimePhase
     - | Возвращает время, проведенное клеткой в текущей фазе жизненного цикла.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_PPFReport_java>` использования.
   * - double data.getTransitionRate(int phase1, int phase2)
     - | phase1 - номер фазы жизненного цикла.
       | phase2 - номер фазы жизненного цикла.
       |
       | Возвращает скорость перехода между фазами жизненного цикла с номерами phase1 и phase2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - data.setTransitionRate(int phase1, int phase2, double speed)
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
   * - data.setExitRate(int phase, double probability)
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
     - | Возвращает true, если клетка мертва.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - int findDeathModelIndex(String name)
     - | name - название типа клеточной смерти.
       |
       | Возвращает индекс типа клеточной смерти с названием name.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double[] rates
     - | Возвращает массив вероятностей всех типов клеточных смертей.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeB_java>` использования.
   * - int rates.size()
     - | Возвращает количество вероятностей всех возможных клеточных смертей.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_Initial_java>` использования.
   * - rates.set(int index, double probability)
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

.. _Physicell_java_Phenotype_Tbl.1.3:

.. list-table:: Таблица 1.3. Члены класса Volume
   :header-rows: 1

   * - Член класса
     - Описание

   * - double total
     - | Возвращает значение общего объема клетки.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.4:

.. list-table:: Таблица 1.4. Члены класса Geometry
   :header-rows: 1

   * - Член класса
     - Описание

   * - double radius
     - | Возвращает радиус клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.5:

.. list-table:: Таблица 1.5. Члены класса Mechanics
   :header-rows: 1

   * - Член класса
     - Описание

   * - double attachmentElasticConstant
     - | Возвращает коэффициент, с которым клетка притягивается к другим клеткам.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_CancerInstantiator_java>` использования.
   * - double cellCellAdhesionStrength
     - | Возвращает силу межклеточной адгезии.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double cellCellRepulsionStrength
     - | Возвращает силу межклеточного отталкивания.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double relDetachmentDistance
     - | Возвращает относительное расстояние (множитель радуиса), на котором клетка отделяется от прикрепленной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.6:

.. list-table:: Таблица 1.6. Члены класса Motility
   :header-rows: 1

   * - Член класса
     - Описание

   * - boolean isMotile
     - | Возвращает true, если клетка подвижна.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - double migrationBias
     - | Возвращает число из интервала [0,1], где 0 обозначает, что клетка движется абсолютно случайно, а 1 - полностью целенаправленно.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - double[] migrationBiasDirection
     - | Возвращает :ref:`нормализованный <PhysiCell_java_Normalization>` вектор, описывающий направление, в котором клетка движется целенаправленно в данный момент времени.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellMotility_java>` использования.
   * - double migrationSpeed
     - | Возвращает скорость движения клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - double persistenceTime
     - | Возвращает время, в течение которого клетка сохраняет одно направление движения.
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.
   * - int chemotaxisDirection
     - | Возвращает "1", если клетка движется к субстрату во время хемотаксиса, или "-1", если клетка движется от него.
       |
       | :ref:`Пример <PhysiCell_java_Worm_WormRule_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.7:

.. list-table:: Таблица 1.7. Члены класса Secretion
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] secretionRates
     - | Возвращает массив скоростей секреции каждого из субстратов данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_TumorPhenotype_java>` использования.
   * - double[] uptakeRates
     - | Возвращает массив скоростей потребления каждого из субстратов данной клеткой.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneInstantiator_java>` использования.
   * - double[] netExportRates
     - | Возвращает массив, содержащий скорости постоянной (не зависящей от объема клетки) секреции/потребления всех возможных субстратов для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_BacterialPhenotype_java>` использования.
   * - setSecretionToZero()
     - | Устанавливает скорость секреции, равной 0, для всех субстратов в модели для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   * - setUptakeToZero()
     - | Устанавливает скорость потребления, равной 0, для всех субстратов в модели для данной клетки.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_PhenotypeA_java>` использования.
   
.. _Physicell_java_Phenotype_Tbl.1.8:

.. list-table:: Таблица 1.8. Члены класса Molecular
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] internSubstrates
     - | Возвращает массив, состоящий из количества всех возможных веществ внутри клетки.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Initial_java>` использования.
   * - double fractionReleasedDeath
     - | Возвращает долю внутренних веществ, которая выбрасывается из клетки в момент ее гибели.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_EpithelialInstantiator_java>` использования.
   * - double fractionTransferredIngested
     - | Возвращает долю внутренних веществ, которую получает клетка, поглотившая клетку данного типа.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_EpithelialInstantiator_java>` использования. 
   
.. _Physicell_java_Phenotype_Tbl.1.10:

.. list-table:: Таблица 1.10. Члены класса CellTransformations
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - double[] transformationRates
     - | Возвращает массив вероятностей трансформации клеток данного типа во все остальные типы клеток.
       |
       | :ref:`Пример <PhysiCell_java_Interactions_StemPhenotype_java>` использования.

.. _Physicell_java_Phenotype_Tbl.1.11:

.. list-table:: Таблица 1.11. Члены класса Intracellular
   :header-rows: 1

   * - Член класса
     - Описание
   
   * - start()
     - | Запускает расчеты внитриклеточной модели.
       |
       | :ref:`Пример <PhysiCell_java_ODEEnergy_Initial_java>` использования.
   * - setParameterValue(String name, double value)
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