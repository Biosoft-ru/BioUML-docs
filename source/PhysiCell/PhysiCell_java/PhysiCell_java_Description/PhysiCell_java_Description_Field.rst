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
