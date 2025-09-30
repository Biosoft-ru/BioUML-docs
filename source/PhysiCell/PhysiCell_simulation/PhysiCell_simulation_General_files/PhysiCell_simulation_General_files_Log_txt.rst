.. _PhysiCell_simulation_General_files_Log_txt:

log.txt
=======

.. |icon_option| image:: /images/icons/option.png

В **log.txt** содержится информация о каждом шаге симуляции модели.

.. code-block:: text
   :caption: Пример файла log.txt

   [ 16:45:46 ] 	Elapsed	0.118	Time:	0     Cells	100
   [ 16:45:47 ] 	Elapsed	0.249	Time:	10    Cells	100
   [ 16:45:47 ] 	Elapsed	0.488	Time:	20    Cells	100
   [ 16:45:47 ] 	Elapsed	0.895	Time:	30    Cells	100
   [ 16:45:48 ] 	Elapsed	1.139	Time:	40    Cells	100
   [ 16:45:48 ] 	Elapsed	1.498	Time:	50    Cells	100
   [ 16:45:48 ] 	Elapsed	1.809	Time:	60    Cells	100
   [ 16:45:49 ] 	Elapsed	2.172	Time:	70    Cells	100
   [ 16:45:49 ] 	Elapsed	2.385	Time:	80    Cells	100
   [ 16:45:49 ] 	Elapsed	2.703	Time:	90    Cells	100
   [ 16:45:50 ] 	Elapsed	2.909	Time:	100   Cells	100

Каждая строка файла **log.txt** соответствует отдельному шагу симуляции и содержит информацию о:

- времени, когда данный шаг симуляции завершился ([ 16:45:46 ]),
- времени, прошедшего с момента начала симуляции (Elapsed	0.118),
- модельном времени на данном шаге симуляции (Time:	0),
- общем количестве клеток в модели на данном шаге симуляции (Cells	100).

.. important::
   Выводимые данные можно поменять, указав пользовательский java-код в поле **global report** в подвкладке **Model report** вкладки **Microenvironment**, предварительно отметив ☑ напротив **Custom global report**.
