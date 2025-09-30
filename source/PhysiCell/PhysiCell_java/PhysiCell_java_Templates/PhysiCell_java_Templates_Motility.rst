.. _PhysiCell_java_Templates_Motility:

Подвижность
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

Данный шаблон используется для написания java-класса, описывающего изменение движения клеток.

.. code-block:: console

   import ru.biosoft.physicell.core.CellFunctions.UpdateMigrationBias;
   import ru.biosoft.physicell.core.Cell;
   import ru.biosoft.physicell.core.Phenotype;

   public class MyMotility extends UpdateMigrationBias
   {

      // Поля для класса, если нужны

      @Override
      public void execute(Cell pCell, Phenotype phenotype, double dt)
      {
		
         // Код, описывающий изменение подвижности клетки pCell за время dt
         // Например:
         // phenotype.motility.isMotile = true;
   	
      }

      // Дополнительные методы, если нужны

   }

