.. _PhysiCell_java_Templates_Report:

Отчет
=====

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

Данный шаблон используется для написания java-класса, описывающего создание таблицы отчета по модели.

.. code-block:: console

   import ru.biosoft.physicell.core.ReportGenerator;
   import ru.biosoft.physicell.core.Cell;

   public class MyReport extends ReportGenerator
   {

      // Поля для класса, если нужны

      public String[] getReportHeaderElements()
      {

         // Код, создающий и возвращающий массив строк. Каждая строка - название колонки в таблице отчета
         // Например:
         // return new String[] {"ID", "X", "Y", "Z", "Oncoprotein"};

      }

      public Object[] getReportElements(Cell cell) throws Exception
      {

         // Код, создающий и возвращающий массив компонентов клетки cell. Порядок компонентов должен соответствовать порядку колонок
         // Например:
         // return new Object[] {cell.ID, cell.position[0], cell.position[1], cell.position[2], cell.getModel().signals.getSingleSignal( cell, "custom:oncoprotein" )};
    
      }

      // Дополнительные методы, если нужны

   }
