.. _PhysiCell_java_Templates_Contact:

Клеточный контакт
=================

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

Данный шаблон используется для написания java-класса, описывающего контакт клеток друг с другом.

.. code-block:: console

   import ru.biosoft.physicell.core.CellFunctions.Contact;
   import ru.biosoft.physicell.core.Cell;
   import ru.biosoft.physicell.core.Phenotype;

   public class MyContact extends Contact
   {
	
      // Поля для класса, если нужны

      public void execute(Cell pActingOn, Phenotype pao, Cell pAttachedTo, Phenotype pat, double dt)
      {

         // Код, описывающий контакт между клетками pActingOn и pAttachedTo за время dt
         // Например:
         // Cell.detachCells( pActingOn, pAttachedTo );

      }

      //Дополнительные методы, если нужны

   }
