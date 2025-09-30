.. _PhysiCell_java_Templates_UpdatePhenotype:

Обновление фенотипа
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

Данный шаблон используется для написания java-класса, описывающего изменения, происходящие внутри клетки.

.. code-block:: console

   import ru.biosoft.physicell.core.CellFunctions.UpdatePhenotype;
   import ru.biosoft.physicell.core.Cell;
   import ru.biosoft.physicell.core.Model;
   import ru.biosoft.physicell.core.Phenotype;

   public class MyPhenotype extends UpdatePhenotype
   {

      //Поля для класса, если нужны

      public MyPhenotype(Model model)
      {
         // Код, инициализирующий класс
      }

      public void execute(Cell pCell, Phenotype phenotype, double dt) throws Exception
      {

         // Код, описывающий внутреннее изменение клетки pCell за время dt
         // Например:
         // signals.setSingleBehavior( pCell, "chemotactic response to oxygen", -1 );

      }

      // Дополнительные методы, если нужны

   }
