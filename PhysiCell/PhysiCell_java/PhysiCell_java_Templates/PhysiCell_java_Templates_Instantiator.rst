.. _PhysiCell_java_Templates_Instantiator:

Инициализация
=============

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

Данный шаблон используется для написания java-класса, описывающего события, происходящие при появлении новой клетки.

.. code-block:: console

   import ru.biosoft.physicell.core.CellFunctions.Instantiator;
   import ru.biosoft.physicell.core.Cell;
   import ru.biosoft.physicell.core.CellDefinition;
   import ru.biosoft.physicell.core.Model;

   public class MyInstantiator extends Instantiator
   {

      // Поля для класса, если нужны

      @Override
      public Cell execute(CellDefinition cd, Model model) throws Exception
      {

         // Код, описывающий события, которые происходят в модели model при появлении в ней новой клетки типа cd.
         // Например:
         // Cell cell = new Cell( cd, model );
         // cell.phenotype.mechanics.attachmentElasticConstant = cd.custom_data.get( "elastic_coefficient" );

      }

      //Дополнительные методы, если нужны

   }
