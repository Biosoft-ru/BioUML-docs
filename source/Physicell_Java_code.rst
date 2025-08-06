Методы Java-кода
================

.. role:: raw-html(raw)
   :format: html

.. raw:: html

    <style>
       table {
           border-collapse: collapse;
           width: 100%;
		   background-color: white;
       }
       th, td {
           border: 1px solid #dddddd;
           text-align: left;
           padding: 8px;
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

.. |icon_new_Java_code| image:: /images/icons/Physicell/new_java_code.png
.. |icon_opened_folder| image:: /images/icons/Physicell/opened_folder.png

Поведение клеток, а также другие аспекты модели могут быть заданы Java-кодом, описывающим подходящий Java-класс.

Java-код в модуле хранится в виде дерева каталогов репозитория и может создаваться/редактироваться через графический интерфейс BioUML.

Для создания Java-файла (Java-класса) нужно:

- нажать ПКМ на папку в репозитории, в которой вы хотите создать Java-класс,
- в раскрывающемся списке нажать ЛКМ на |icon_new_Java_code| **New Java code**,
- в появившемся окошке вписать название файла с расширением *.java*,
- нажать ЛКМ кнопку **Ok** :ref:`(Рисунок 1) <Physicell_java_code_Pic.1>`.

.. _Physicell_java_code_Pic.1:

.. figure:: images/Physicell/Physicell_java_code/Add_new_java_code.png
   :width: 100%
   :alt: Add_new_java_code
   :align: center

   Рисунок 1. Создание Java-класса.

После этого в указанной папке у вас появится Java-файл (обозначается значком |icon_new_Java_code|), который можно открыть, нажав на него 2 раза ЛКМ или нажав на него ПКМ и в раскрывающемся списке нажав ЛКМ на |icon_opened_folder| **Open**.

В открывшемся файле можно прописывать необходимый код :ref:`(Рисунок 2) <Physicell_java_code_Pic.2>`.

.. _Physicell_java_code_Pic.2:

.. figure:: images/Physicell/Physicell_java_code/Java_code_place.png
   :width: 100%
   :alt: Java_code_place
   :align: center

   Рисунок 2. Поле для записи Java-кода.

Далее мы подробно рассмотрим все классы пакета ru.biosoft.Physicell и стандартные Java-классы, а также их методы, которые используются для написания кода. 

ru.biosoft.physicell.biofvm.VectorUtil
--------------------------------------

Класс VectorUtil подпакета biofvm используется для работы с векторами.

Все члены класса VectorUtil представлены в :ref:`таблице 1 <Physicell_java_code_Tbl.1>`.

.. _Physicell_java_code_Tbl.1:

.. list-table:: Таблица 1. Члены класса VectorUtil
   :header-rows: 1

   * - Член класса
     - Описание

   * - .newDiff(vector1, vector2)
     - | Статический метод.
       |
       | Создать новый вектор, являющийся
       | :ref:`покоординатной разницей векторов <Physicell_java_code_coordinate_wise_difference_of_vectors>` vector1 и vector2.
   * - .norm_squared(vector)
     - | Статический метод.
       |
       | Рассчитать :ref:`L2-норму <Physicell_java_code_L2_norm>` вектора vector.
   * - .axpy(vector1, const, vector2)
     - | Статический метод.
       |
       | Модифицировать вектор vector1 покоординатно следующим
       | образом: vector1[i] = vector1[i] + a*vector2[i], где i - каждая
       | координата векторов vector1 и vector2.
   * - .newNormalize(vector)
     - | Статический метод.
       |
       | :ref:`Нормализовать <Physicell_java_code_Normalization>` вектор vector.
   * - .dist(cell1, cell2)
     - | Статический метод.
       |
       | Рассчитать :ref:`расстояние <Physicell_java_code_Distance>` между клетками cell1 и cell2.

Справка
~~~~~~~

.. _Physicell_java_code_coordinate_wise_difference_of_vectors:

Покоординатная разница векторов
"""""""""""""""""""""""""""""""

Покоординатная разница векторов — это операция вычитания векторов, при которой вычитаются соответствующие компоненты (координаты) векторов.

.. code-block:: text
   :caption: Пример

   // Дано
   Vector3D a = new Vector3D(5, 3, 7);
   Vector3D b = new Vector3D(1, 2, 4);

   // Покоординатная разница
   Vector3D difference = a.subtract(b); // Результат: (4, 1, 3)

.. _Physicell_java_code_L2_norm:

L2-норма вектора
""""""""""""""""

L2-норма вектора (евклидова норма) — это стандартный способ измерения длины вектора. Рассчитывается как квадратный корень из суммы квадратов всех компонент вектора:

:raw-html:`Для вектора v = (v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>n</sub>)` в n-мерном пространстве:

.. math::

   \|v\|_2 = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}

.. _Physicell_java_code_Normalization:

Нормализация вектора
""""""""""""""""""""

Нормализация вектора — это преобразование вектора в вектор единичной длины (с нормой = 1), сохраняющий его направление.

Нормализованная версия вектора :raw-html:`v = (v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>n</sub>)` представляет собой вектор v', каждая координата которого меньше
соответствующей координаты вектора v в :ref:`L2-норму <Physicell_java_code_L2_norm>` этого вектора:

.. math::

   {v'}_i = \frac{v_i}{\sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}}, \quad \text{где } i = 1, 2, \ldots, n.

.. _Physicell_java_code_Distance:

Расстояние между точками
""""""""""""""""""""""""

В двумерной системе координат расстояние (d) между точками :raw-html:`A(x<sub>1</sub>, y<sub>1</sub>) и B(x<sub>2</sub>, y<sub>2</sub>)` вычисляется следующим образом:

.. math::

  d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}

В трехмерной системе координат расстояние (d) между точками :raw-html:`A(x<sub>1</sub>, y<sub>1</sub>, z<sub>1</sub>) и B(x<sub>2</sub>, y<sub>2</sub>, z<sub>2</sub>)` вычисляется следующим образом:

.. math::

  d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}

ru.biosoft.physicell.core.Cell
------------------------------

Класс Cell подпакета core используется для работы с клетками.

Все члены класса Cell представлены в :ref:`таблице 2 <Physicell_java_code_Tbl.2>`.

.. _Physicell_java_code_Tbl.2:

.. list-table:: Таблица 2. Члены класса Cell
   :header-rows: 1

   * - Член класса
     - Описание

   * - .position
     - | Нестатическое поле.
       |
       | Трехмерный вектор - координаты клетки.
   * - .velocity
     - | Нестатическое поле.
       |
       | Трехмерный вектор - скорость клетки.
   * - .type
     - | Нестатическое поле.
       |
       | Числовой код типа данной клетки.
   * - .parameters.o2_proliferation_saturation
     - | Нестатическое поле.
       |
       | Количество кислорода, при котором он
       | перестает усиливать пролиферацию клетки.
       | Используется для клеток с :ref:`фенотипом <Physicell_cell_properties_Functions>`
       | «Default O2-based phenotype».
   * - .parameters.o2_reference
     - | Нестатическое поле.
       |
       | Референсное значение кислорода.
   * - .functions.customCellRule
     - | Нестатическое поле.
       |
       | Объект, описывающий пользовательское
       | правило для данного типа клетки.
   * - .functions.updatePhenotype
     - | Нестатическое поле.
       |
       | Объект, описывающий функцию обновления фенотипа
       | для данного типа клетки.
   * - .state.attachedCells
     - | Нестатическое поле.
       |
       | Список клеток, соединенных с данной клеткой.
   * - .detachCells(cell1, cell2)
     - | Статический метод.
       |
       | Расцепить клетки cell1 и cell2.
   * - .attachcCells(cell1, cell2)
     - | Статический метод.
       |
       | Соединить клетки cell1 и cell2.
   * - .createCell(cd, model, position)
     - | Статический метод.
       |
       | Создать клетку типа cd в модели model в точке position.
   * - .customData.findVariableIndex("a")
     - | Обычный метод.
       |
       | Получить индекс переменной "a" в списке переменных
       | типа клетки.
   * - | .state.attachedCells.size()
       | или
       | .state.numberAttachedCells()
     - | Обычный метод.
       |
       | Получить количество клеток, соединенных с данной
       | клеткой.
   * - .customData.get(index)
     - | Обычный метод.
       |
       | Получить численное значение переменной по ее
       | индексу (index) для данной клетки.
   * - .getMicroenvironment()
     - | Обычный метод.
       |
       | Возвращает объект среды, в которой сущетсвует
       | клетка.
   * - .nearest_gradient(index)
     - | Обычный метод.
       |
       | Возвращает знаение градиента плотности субстрата с
       | данным индексом (index) в ближайщей ячейке к клетке.
   * - .startDeath(index)
     - | Обычный метод.
       |
       | Запустить клеточную смерть с заданным индексом
       | (index).
   * - .cells_in_my_container()
     - | Обычный метод.
       |
       | Получить список клеток в ячейке данной клетки.
   * - .customData.set("x", x)
     - | Обычный метод.
       |
       | Установить значение x пользовательскому параметру "x".
   * - Cell cell = new Cell(cd, model)
     - | Конструктор.
       |
       | Создать новую клетку (cell) заданного типа (cd), в данной
       | модели (model).

ru.biosoft.physicell.core.Phenotype
-----------------------------------

Класс Phenotype подпакета core используется для работы с свойствами клеток.
   
.. note::
   Класс **Phenotype** является вложенным объектом внутри класса **Cell**.

Все члены класса Phenotype представлены в :ref:`таблице 3 <Physicell_java_code_Tbl.3>`.

.. _Physicell_java_code_Tbl.3:

.. list-table:: Таблица 3. Члены класса Phenotype
   :header-rows: 1

   * - Член класса
     - Описание

   * - .phenotype.death.dead
     - | Нестатическое поле.
       |
       | true, если клетка мертва;
       | false, если клетка жива.
   * - .phenotype.mechanics.attachmentElasticConstant
     - | Нестатическое поле.
       |
       | Коэффициент, с которым клетка притягивается
       | к другим клеткам.