.. _PhysiCell_java_CartesianMesh:

CartesianMesh
=============

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

Класс CartesianMesh используется для работы с :ref:`декартовой системой координат <Physicell_microenvironment_Domain>`, в которой располагаются клетки и субстраты.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.biofvm.CartesianMesh

Все члены класса CartesianMesh представлены ниже.

.. list-table:: Члены класса CartesianMesh
   :header-rows: 1

   * - Член класса
     - Описание

   * - int[] moore_connected_voxel_indices
     - | Содержит массив индексов всех ячеек решетки в :ref:`окрестности Мура <Physicell_java_Moore_neighborhood>` 1-ого порядка от данной ячейки.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - voxels
     - | Содержит массив, состоящий из всех ячеек решетки.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - double[] voxels[int number].center
     - | number - номер ячейки решетки.
       |
       | Содержит координаты центра ячейки решетки с номером number.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.

.. _Physicell_java_Moore_neighborhood:

Окрестность Мура
----------------

Окрестность Мура порядка r — множество ячеек, расстояние Чебышёва до которых от данной ячейки не превышает r.

.. figure:: /images/Physicell/Physicell_java_code/Moore_neighborhood.png
   :width: 60%
   :alt: Moore_neighborhood
   :align: center

:raw-html:`<br>`