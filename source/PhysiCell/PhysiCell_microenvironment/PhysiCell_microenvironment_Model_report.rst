.. _PhysiCell_microenvironment_Model_Report:
 
Отчет по модели (Model Report)
==============================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png
.. |icon_Java_code| image:: /images/icons/Physicell/Java_code.png

После нажатия на вкладку **Model Report** на панели свойств справа у вас появится меню, в котором можно редактировать следующие параметры:

.. figure:: /images/Physicell/Physicell_microenvironment/Model_report_menu.png
   :width: 100%
   :alt: Model_report_menu
   :align: center

:raw-html:`<br>`

- |icon_option| **Custom report**: поставьте ☑, если хотите задать Java-код, по которому будет создаваться отчет по модели в табличной форме,
- |icon_option| **Custom global report**: поставьте ☑, если хотите задать Java-код, который будет определять вывод логов в консль во время симуляции модели,
- |icon_option| **Custom visualizer**: поставьте ☑, если хотите задать Java-код, по которому будет изменяться расцветка клеток при симуляции модели.

При указании ☑ напротив |icon_option| **Custom report**, |icon_option| **Custom global report** или |icon_option| **Custom visualizer** ниже выбранного поля появится новое поле |icon_option| **Report**, |icon_option| **Global report** или |icon_option| **Visualizer**, соответственно. Напротив этих полей можно нажать ЛКМ на |icon_Java_code| **(select element)**, а затем в появившемся окне указать путь до нужного Java-кода в репозитории.

.. figure:: /images/Physicell/Physicell_microenvironment/Choose_appropriate_Java_code.png
   :width: 100%
   :alt: Choose_appropriate_Java_code
   :align: center

:raw-html:`<br>`