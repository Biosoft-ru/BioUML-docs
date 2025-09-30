.. _PhysiCell_java_Templates_Event:

Событие
=======

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

Данный шаблон используется для написания java-класса, описывающего мгновенное изменение, происходящее в модели, под действием какого-либо сигнала.

.. code-block:: console

   import ru.biosoft.physicell.core.Model.Event;
   import ru.biosoft.physicell.core.Model;

   public class MyEvent extends Event
   {

      // Поля для класса, если нужны

      public MyEvent(Model model)
      {

         super( model );
         // Код, инициализирующий свойства события в модели model

      }

      @Override
      public void execute() throws Exception
      {

         // Код, выполняющий событие

      }

      // Дополнительные методы, если нужны

   }
