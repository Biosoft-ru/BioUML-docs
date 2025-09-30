.. _PhysiCell_java_Templates_CustomCellRule:

Пользовательское правило
========================

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

Данный шаблон используется для написания java-класса, описывающего пользовательское правило поведения клеток определенного типа.

.. code-block:: console

   import ru.biosoft.physicell.core.CellFunctions.CustomCellRule;
   import ru.biosoft.physicell.core.Cell;
   import ru.biosoft.physicell.core.Model;
   import ru.biosoft.physicell.core.Phenotype;

   public class MyCellRule extends CustomCellRule
   {

      //Поля для класса, если нужны

      public MyCellRule(Model model)
      {
         // Код, инициализирующий класс
      }

      public void execute(Cell pCell, Phenotype phenotype, double dt) throws Exception
      {

         // Код, описывающий пользовательское правило изменения внутреннего состояния клетки pCell за время dt
         // Например:
         // signals.setSingleBehavior( pCell, "chemotactic response to oxygen", -1 );

      }

      // Дополнительные методы, если нужны

   }
