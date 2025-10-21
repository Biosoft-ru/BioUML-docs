.. _PhysiCell_java_Description_Field:

Поле
====

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

Поле — это переменная, объявленная внутри класса. Она хранит состояние объекта (или класса, если поле статическое).

Поле создается следующим образом:

.. code-block:: text

   static int MyField

   где:
    
   • static - указание на то, что поле статическое (применяется к классу). Если не указано, то считается, что поле нестатическое (применяется к объекту класса).
   • int - тип данных, которые содержит поле.
   • MyField - название поля.

Внутри класса поле объявляется следующим образом:

.. code-block:: console

   // Класс Circle
   public class Circle {

      // Поля класса:
      // radius - радиус круга (тип данных double)
      private double radius;

   }

Поля бывают статическими (при их объявлении указывается модификатор "static", такие поля относятся ко всему классу, а не к конкретным объектам этого класса) и нестатическими (относятся к конкретным объектам класса).

Обращение к статическому полю осуществляется через имя самого класса, например:

.. code-block:: console

   PhysiCellConstants.apoptotic;

   • PhysiCellConstants - название класса.

Обращение к нестатическому полю осуществляется через имя объекта какого-либо класса, например:

.. code-block:: console

   Cell cell1 = new Cell(CellDefinition cd, Model model);

   сell1.position;
