.. _PhysiCell_java:

Пользовательский код для модели
===============================

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

.. raw:: html

   <style>
   pre {
      white-space: pre-wrap !important;       /* Сохраняет пробелы, но разрешает перенос */
      word-wrap: break-word !important;       /* Переносит длинные слова */
      overflow-wrap: break-word !important;   /* Альтернатива для совместимости */
      hyphens: auto !important;               /* Перенос с тире */
   }
   </style>

.. |icon_new_Java_code| image:: /images/icons/Physicell/new_java_code.png
.. |icon_opened_folder| image:: /images/icons/Physicell/opened_folder.png

.. note::
  Данный раздел предназначен для продвинутых пользователей и является необязательным - создавать модели можно и без использования кода.

Поведение клеток, а также другие аспекты модели могут быть заданы java-кодом, описывающим подходящий java-класс.

В частности, с помощью java-кода можно настроить:

- Различные функции клеток (изменение внутреннего состояния, подвижность, клеточный контакт и др.).
- Цвета отрисовки клеток в различных условиях.
- Начальное расположение клеток.
- Вывод отчета и логов при симуляции модели.
- События модели. 
- Правила создания новых клеток.

и др.

Java-код хранится в виде отдельных файлов в репозитории BioUML. Каждый файл описывает один java-класс.

Для создания java-файла (java-класса) нужно:

1. Нажать ПКМ на папку в репозитории, в которой вы хотите создать java-класс.
2. В раскрывающемся списке нажать ЛКМ на |icon_new_Java_code| **New Java code**.
3. В появившемся окошке вписать название файла с расширением *.java*.
4. Нажать ЛКМ кнопку **Ok**.

.. figure:: /images/Physicell/Physicell_java_code/Add_new_java_code.png
   :width: 100%
   :alt: Add_new_java_code
   :align: center

:raw-html:`<br>`
После этого в указанной папке у вас появится java-файл (обозначается значком |icon_new_Java_code|), который можно открыть, нажав на него 2 раза ЛКМ или нажав на него ПКМ и в раскрывающемся списке нажав ЛКМ на |icon_opened_folder| **Open**.

В открывшемся файле можно прописывать необходимый код.

.. figure:: /images/Physicell/Physicell_java_code/Java_code_place.png
   :width: 100%
   :alt: Java_code_place
   :align: center

:raw-html:`<br>`
Список основных java-классов пакета ru.biosoft.Physicell, используемых для задания пользовательского поведения клеток, и их краткое описание представлены ниже.

.. list-table:: Классы пакета ru.biosoft.Physicell
   :header-rows: 1

   * - Класс
     - Описание

   * - :ref:`VectorUtil <PhysiCell_java_VectorUtil>`
     - Работа с векторами
   * - :ref:`Cell <PhysiCell_java_Cell>`
     - Работа с отдельными агентами, т.е. клетками
   * - :ref:`Phenotype <PhysiCell_java_Phenotype>`
     - Работа с различными свойствами клеток
   * - :ref:`CellDefinition <PhysiCell_java_CellDefinition>`
     - Работа с типами клеток
   * - :ref:`Model <PhysiCell_java_Model>`
     - Работа с мультиклеточной моделью для численных расчетов
   * - :ref:`Microenvironment <PhysiCell_java_Microenvironment>`
     - Работа со средой модели, в которой находятся клетки и вещества
   * - :ref:`RandomGenerator <PhysiCell_java_RandomGenerator>`
     - Генерация случайных величин в модели
   * - :ref:`PhysiCellConstants <PhysiCell_java_PhysiCellConstants>`
     - Работа с константными численными значениями модели
   * - :ref:`StandardModels <PhysiCell_java_StandardModels>`
     - Работа со стандартными моделями клеточного цикла и клеточной смерти
   * - :ref:`SignalBehavior <PhysiCell_java_SignalBehavior>`
     - Управление передачи сигналов и поведения клеток
   * - :ref:`CellContainer <PhysiCell_java_CellContainer>`
     - Получение информации о расположении клеток в решетке модели
   * - :ref:`CartesianMesh <PhysiCell_java_CartesianMesh>`
     - Работа с декартовой системой координат, в которой располагаются клетки и субстраты
   * - :ref:`ModelReader <PhysiCell_java_ModelReader>`
     - Чтение модели из текстового файла
   * - :ref:`UpDownSignal <PhysiCell_java_UpDownSignal>`
     - Расчет эффекта выходного сигнала согласно многомерному закону Хилла на основе множественных входящих сигналов-эффектов
   * - :ref:`BasicSignaling <PhysiCell_java_BasicSignaling>`
     - Работа с методами, которые рассчитывают значение выходного сигнала на основе одного входящего сигнала
   * - :ref:`PhysiCellUtilities <PhysiCell_java_PhysiCellUtilities>`
     - Дополнительные методы работы с моделью
   * - AgentColorer
     - Интерфейс, используемый для определения того, каким цветом отрисовывать клетку (ее границу, внутреннюю часть, границу ядра и само ядро)
   * - InitialCellsArranger
     - Абстрактный класс, определяющий изначальную расстановку клеток в модели. Может использоваться в подвкладке Initial Condition вкладки Microenvironment.
   * - O2based
     - Подкласс UpdatePhenotype. Описывает стандартную жизнедеятельность клетки в зависимости от концентрации кислорода.
   * - Visualizer
     - Отрисовывает результат расчетов модели.
   * - ReportGenerator
     - Создает табличный отчет во время расчетов с отдельной строкой для каждой клетки в модели. Может использоваться в подвкладке Model Report вкладки Microenvironment.
   * - CustomCellData
     - Содержит пользовательские параметры конкретного типа клеток. Заполняется пользователем в подвкладке Custom Data вкладки Cell Types.
   * - AgentColorerDefault
     - Стандартная реализация класса AgentColorer. Раскрашивает агент в зависимости от его типа и того, жив ли он.
   * - FalseCellCytometryVisualizer
     - Подкласс AgentColorerDefault. Раскрашивает клетки, имеющие жизненный цикл типа Flow Cytometry model в зависимости от текущей фазы клеточного цикла.
   * - StandardElasticContact
     - Стандартная реализация класса Contact. Описывает эластичное взаимодействие клетки с другими клетками.
   * - Chemotaxis
     - Стандартная реализация класса UpdateMigrationBias. Описывает движение клетки по градиенту одного субстрата.
   


.. toctree::
   :maxdepth: 2
   :hidden:
   
   PhysiCell_java_Data_types
   PhysiCell_java_Description
   PhysiCell_java_Templates
   PhysiCell_java_VectorUtil
   PhysiCell_java_Cell
   PhysiCell_java_Phenotype
   PhysiCell_java_CellDefinition
   PhysiCell_java_Model
   PhysiCell_java_Microenvironment
   PhysiCell_java_RandomGenerator
   PhysiCell_java_PhysiCellConstants
   PhysiCell_java_StandardModels
   PhysiCell_java_SignalBehavior
   PhysiCell_java_CellContainer
   PhysiCell_java_CartesianMesh
   PhysiCell_java_ModelReader
   PhysiCell_java_UpDownSignal
   PhysiCell_java_BasicSignaling
   PhysiCell_java_PhysiCellUtilities
   PhysiCell_java_Examples

   
