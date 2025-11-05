.. _PhysiCell_java_VectorUtil:

VectorUtil
==========

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

Класс VectorUtil используется для работы с векторами.

Для импорта данного класса используйте:

.. code-block:: text

   import ru.biosoft.physicell.biofvm.VectorUtil

Все члены класса VectorUtil представлены ниже.

.. list-table:: Члены класса VectorUtil
   :header-rows: 1

   * - Член класса
     - Описание

   * - static double[] newDiff(double[] vector1, double[] vector2)
     - | vector1 - трехмерный вектор.
       | vector2 - трехмерный вектор.
       |
       | Возвращает трехмерный вектор, являющийся :ref:`покоординатной разницей векторов <Physicell_java_Coordinate_wise_difference_of_vectors>` vector1 и vector2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - static double norm(double[] vector)
     - | vector - трехмерный вектор.
       |
       | Возвращает :ref:`L2-норму <Physicell_java_L2_norm>` вектора vector.
       |
       | :ref:`Пример <PhysiCell_java_CellTypes3_Initial_java>` использования.
   * - static double norm_squared(double[] vector)
     - | vector - трехмерный вектор.
       |
       | Возвращает квадрат :ref:`L2-нормы <PhysiCell_java_L2_norm>` вектора vector.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - static double[] newNormalize(double[] vector)
     - | vector - трехмерный вектор.
       |
       | Возвращает :ref:`нормализованный <PhysiCell_java_Normalization>` вектор vector.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - static void normalize(double[] vector)
     - | vector - трехмерный вектор.
       |
       | :ref:`Нормализует <PhysiCell_java_Normalization>` вектор vector.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_WeightedMotility_java>` использования.
   * - static double dist(double[] vector1, double[] vector2)
     - | vector1 - трехмерный вектор.
       | vector2 - трехмерный вектор.
       |
       | Возвращает :ref:`расстояние <PhysiCell_java_Distance>` между векторами vector1 и vector2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_ImmuneCellRule_java>` использования.
   * - static double[] newProd(double[] vector, double const)
     - | vector - трехмерный вектор.
       | const - число.
       |
       | Возвращает трехмерный вектор res_vector следующего вида:
       | res_vector[i] = const*vector[i],
       | где i - каждая координата векторов res_vector и vector.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_AvoidBoundariesRule_java>` использования.
   * - static double[] axpy(double[] vector1, double const, double[] vector2)
     - | vector1 - трехмерный вектор.
       | const - число.
       | vector2 - трехмерный вектор.
       |
       | Возвращает трехмерный вектор vector следующего вида:
       | vector[i] = vector1[i] + const*vector2[i],
       | где i - каждая координата векторов vector, vector1 и vector2.
       |
       | :ref:`Пример <PhysiCell_java_CancerImmune_AdhesionContact_java>` использования.
   * - static void zero(double[] vector)
     - | vector - трехмерный вектор.
       |
       | Зануляет все координаты вектора vector.
       |
       | :ref:`Пример <PhysiCell_java_PredatorPreyFarmer_WeightedMotility_java>` использования.

Справка по операциям с векторами
--------------------------------

.. _PhysiCell_java_Coordinate_wise_difference_of_vectors:

Покоординатная разница векторов
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Покоординатная разница векторов — это операция вычитания векторов, при которой вычитаются соответствующие компоненты (координаты) векторов.

.. code-block:: text
   :caption: Пример

   // Дано
   Vector3D a = new Vector3D(5, 3, 7);
   Vector3D b = new Vector3D(1, 2, 4);

   // Покоординатная разница
   Vector3D difference = a.subtract(b); // Результат: (4, 1, 3)

.. _PhysiCell_java_L2_norm:

L2-норма вектора
~~~~~~~~~~~~~~~~

L2-норма вектора (евклидова норма) — это стандартный способ измерения длины вектора. Рассчитывается как квадратный корень из суммы квадратов всех компонент вектора.

:raw-html:`Для вектора v = (v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>n</sub>)` в n-мерном пространстве:

.. math::

   \|v\|_2 = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}

.. _PhysiCell_java_Normalization:

Нормализация вектора
~~~~~~~~~~~~~~~~~~~~

Нормализация вектора — это преобразование вектора в вектор единичной длины (с :ref:`L2-нормой <PhysiCell_java_L2_norm>`, равной 1), сохраняющий его направление.

Нормализованная версия вектора :raw-html:`v = (v<sub>1</sub>, v<sub>2</sub>, ..., v<sub>n</sub>)` представляет собой вектор v`, каждая координата которого меньше
соответствующей координаты вектора v в L2-норму этого вектора:

.. math::

   {v'}_i = \frac{v_i}{\sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}}, \quad \text{где } i = 1, 2, \ldots, n.

.. _PhysiCell_java_Distance:

Расстояние между векторами
~~~~~~~~~~~~~~~~~~~~~~~~~~

В двумерной системе координат расстояние (d) между векторами :raw-html:`A(x<sub>1</sub>, y<sub>1</sub>) и B(x<sub>2</sub>, y<sub>2</sub>)` вычисляется следующим образом:

.. math::

  d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}

В трехмерной системе координат расстояние (d) между векторами :raw-html:`A(x<sub>1</sub>, y<sub>1</sub>, z<sub>1</sub>) и B(x<sub>2</sub>, y<sub>2</sub>, z<sub>2</sub>)` вычисляется следующим образом:

.. math::

  d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}