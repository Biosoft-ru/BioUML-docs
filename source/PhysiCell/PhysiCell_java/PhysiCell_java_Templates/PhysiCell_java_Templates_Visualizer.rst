.. _PhysiCell_java_Templates_Visualizer:

Визуализация клеток
===================

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

Данный шаблон используется для написания java-класса, описывающего отрисовку клеток разных типов в зависимости от тех или иных условий.

.. code-block:: console

   import ru.biosoft.physicell.ui.AgentColorer;
   import java.awt.Color;

   public class Visualizer implements AgentColorer
   {

      // поля для класса, если нужны

      @Override
      public Color[] findColors(Cell cell)
      {

         // Код, создающий и возвращающий массив, каждый элемент которого - цвет. Массив может быть из 4, 2 или 1 элемента.
         // Например:
         // Color[] result = new Color[2];
         // result[0] = Color.cyan;
         // result[1] = new Color( 250, 138, 38 );
         // return result;

      }

      // дополнительные методы, если нужны

   }

.. important::
  Если массив (например, result), который возвращает метод findColors, состоит из 4 цветов, то:

  - result[0] - цвет внутреннего содержимого клетки.
  - result[1] - цвет контура клетки.
  - result[3] - цвет ядра клетки.
  - result[4] - цвет контура ядра.

  Если массив состоит из 2 цветов, то:

  - result[0] - цвет внутреннего содержимого клетки.
  - result[1] - цвет контура клетки.

  Если массив состоит из 1 цвета, то этим цветом будет отрисовываться внутренее содержимое клетки, а ее контур будет черным.

  В последних двух случаях ядро у клетки отрисовываться не будет.
