.. _PhysiCell_java_Templates_InitialCellsArranger:

Начальная расстановка клеток
============================

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

Данный шаблон используется для написания java-класса, описывающего позиции клеток в начале симуляции модели.

.. code-block:: console

   import ru.biosoft.physicell.core.InitialCellsArranger;
   import ru.biosoft.physicell.core.Model;

   public class MyInitial extends InitialCellsArranger
   {

      // Поля для класса, если нужны
    
      @Override
      public void arrange(Model model) throws Exception
      {
     
         // Код, создающий начальную расстановку агентов (клеток) в модели model
         // Например:
         // Cell.createCell( cd, m, position )
    
      }

      // Дополнительные методы, если нужны

   }
