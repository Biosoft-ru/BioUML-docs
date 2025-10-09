.. _PhysiCell_java_Description_Constructor:

Конструктор
===========

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

Конструктор — это специальный метод, который вызывается при создании нового объекта того или иного класса с помощью оператора "new".

Основные правила объявления конструктора в java:

- Имя конструктора должно совпадать с именем класса.
- У конструктора нет возвращаемого типа.

Внутри класса конструктор объявляется следующим образом:

.. code-block:: text

   // Класс Cell
   public class Cell {

      // Поля класса:
      // cd - объект класса CellDefinition
      // model - объект класса Model
      private CellDefinition cd;
      private Model model;

      // Конструктор, принимающий на вход два параметра  
      public Cell(CellDefinition cd, Model model) {

         //Устанавливаем в поля класса параметры, которые принимает на вход конструктор
         this.cd = cd;
         this.model = model;
      }

   }

Конструктор вызывается следующим образом:

.. code-block:: text

   Cell cell1 = new Cell(CellDefinition cd, Model model)

   • Cell cell1 - указание на то, что создается объект cell1, принадлежащий классу Cell.
   • new Cell - создание нового объекта.
   • CellDefinition cd - аргумент (cd) и его тип/класс (CellDefinition), передаваемый в конструктор.
