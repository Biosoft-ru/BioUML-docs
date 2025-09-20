.. _PhysiCell_java_CellContainer:

CellContainer
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

Класс CellContainer используется для получения информации о расположении клеток в решетке модели.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.core.CellContainer

Все члены класса CellContainer представлены ниже.

.. list-table:: Члены класса CellContainer
   :header-rows: 1

   * - Член класса
     - Описание

   * - CartesianMesh mesh
     - | Возвращает объект, описывающий :ref:`решетку <PhysiCell_microenvironment_Domain>` в модели. Обычно это объект класса :ref:`CartesianMesh <PhysiCell_java_CartesianMesh>`.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - agentGrid
     - | Возвращает объект, хранящий расположение всех клеток в ячейках внешней среды.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.
   * - List<Cell> agentGrid.get(int number)
     - | number - номер ячейки решетки в модели.
       |
       | Возвращает массив из клеток в ячейке с номером number.
       |
       | :ref:`Пример <PhysiCell_java_VirusMacrophage_Macrophage_java>` использования.