.. _PhysiCell_java:

Методы java-кода
================

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

Поведение клеток, а также другие аспекты модели могут быть заданы java-кодом, описывающим подходящий java-класс.

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
Далее мы подробно рассмотрим все классы пакета ru.biosoft.Physicell, а также их поля и методы, которые используются для написания java-кода. 

Для описания методов и полей мы будем использовать следующие обозначения:

.. code-block:: text
    :caption: Пример описания метода

    Метод/поле:

    static double[] newDiff(double[] vector1, double[] vector2)

    где:
    
    • static - метод/поле статическое (применяется к классу). Если не указано, то считается, что метод/поле нестатическое (применяется к объекту класса).
    • double[] - тип данных, который возращает метод/поле. Если не указано, то считается, что метод/поле ничего не возвращает.
    • newDiff - название метода/поля.
    • double[] vector1 - название аргумента (vector1) и его тип данных (double[]).

.. toctree::
   :maxdepth: 2
   :hidden:
   
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
