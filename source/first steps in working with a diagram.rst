Интерфейс BioUML при работе с диаграммами
=========================================

.. |diagram| image:: /images/icons/Type-Diagram-icon.png
.. |zoom in| image:: /images/icons/WebAction-toolbar-zoom_in-icon.png
.. |zoom out| image:: /images/icons/WebAction-toolbar-zoom_out-icon.png
.. |fit to screen| image:: /images/icons/fit_to_screen.png
.. |save| image:: /images/icons/save.gif
.. |saveas| image:: /images/icons/saveas.gif
.. |revert| image:: /images/icons/revert_save.gif
.. |export| image:: /images/icons/export.png
.. |import| image:: /images/icons/import.gif

*Открытие диаграммы* осуществляется путем двойного щелчка мыши на диаграмму, который отображается как |diagram| во вкладке :guilabel:`Data` области :doc:`репозитория </user_interface>`.
В :doc:`рабочем пространстве </user_interface>` отображается полноразмерная *часть диаграммы*, в то время как   
*общий вид диаграммы* — в :doc:`поле операций </user_interface>` во вкладке :guilabel:`Overview`. Область диаграммы, отображенная в рабочем пространстве выделяется пунктиром на общем виде диаграммы, расположенной
в области поля операций. Для облегчения ориентации на больших диаграммах отдельные ребры и узлы диаграммы подсвечиваются голубым цветом :ref:`(Рисунок 1) <Pic.1>`.

.. _Pic.1:

.. figure:: images/diagrams/opened_diagram.png
   :width: 100%
   :alt: Открытая диаграмма в веб-версии BioUML
   :align: center

   Рисунок 1. Открытая диаграмма в веб-версии BioUML
   
Текущую отображаемую область диаграммы можно сместить:

-     в рабочем пространстве, щелкнув и перетащив «холст» диаграммы, либо используя полосы прокрутки; 
-     сдвинув (щелкнув и перетащив) пунктирный прямоугольник (представляющий область, которая сейчас просматривается в рабочем пространстве) на вкладке :guilabel:`Overview` в области поля операций .

Для *создания новой диаграммы*, во вкладке :guilabel:`Data` области :doc:`репозитория </user_interface>` выберите проект и нажмите правой кнопкой мыши на нужную папку, в которой планируется
создание диаграммы. В выпадающем списке нажмите на поле |diagram| New diagram. Далее в открывшемся окне выберите нужный *тип диаграммы*. 

Диаграммы можно *экспортировать* в различных форматах, нажав инонку |export|, расположенной на общей панели управления, либо нажав
правой кнопкой мыши на диаграмму в репозитории и в выпадающем списке выбрать |export|.
*Импорт диаграммы* осуществляется нажатием на иконку |import|.

Панель инструментов
-------------------

В верхней части рабочего пространства находится *панель инструментов* :ref:`(Рисунок 2) <Pic.2>`, которая содержит элементы, которые могут быть добавлены на диаграмму. 
При этом, каждому отдельному типу диаграммы будет соответсвовать определенный набор элементов. 

.. _Pic.2:

.. figure:: /images/interface/modelling_icons.png
   :width: 80%
   :alt: Панель инструментов
   :align: center

   Рисунок 2. Панель инструментов

.. note::
   Детальное описание соответствующих элементов будет приведено в следующих главах. 
   
Общая панель управления
-----------------------

На *общей панели управления* :ref:`(Рисунок 3) <Pic.3>`, которая располагается сверху от рабочего пространства, представлены различные опции, используемые при работе с диаграммами:

.. _Pic.3:

.. figure:: /images/interface/general_panel.png
   :width: 90%
   :alt: Общая панель управления
   :align: center

   Рисунок 3. Общая панель управления при работе с диаграммами 

.. raw:: html

    <style>
       table {
           border-collapse: collapse;
           width: 100%;
		   background-color: white;
       }
       th, td {
           border: 1px solid #dddddd;
           text-align: left;
           padding: 8px;
       }
       tr:nth-child(even) {
           background-color: white;
       }
       th {
           background-color: #2980B9;
           color: white;
       }
	   .table-bottom-margin {
           margin-top: 20px;
       }
   </style>
   
   <table style="table-layout: fixed; width: 100%; word-wrap: break-word;">
   <caption>Таблица 1. Элементы общей панели управления, используемой при работе с диаграммами</caption>
   <tr>
        <th>Описание</th>
        <th>Обозначение</th>
    </tr>
    <tr>
	    <th colspan="2">Управление версиями и экспортом/импортом диаграммы</th>
    </tr>
    <tr>
        <td>Сохранение текущей версии диаграммы</td>
        <td><img src="_images/save.gif" alt="Сохранение диаграммы"></td>
    </tr>
    <tr>
        <td>Сохранение копии диаграммы</td>
        <td><img src="_images/saveas.gif" alt="Сохранение копии диаграммы"></td>
    </tr>
    <tr>
        <td>Восстановление сохраненной версии диаграммы</td>
        <td><img src="_images/revert_save.gif" alt="Восстановление сохраненной версии диаграммы"></td>
    </tr>
    <tr>
        <td>Экспорт диаграммы</td>
        <td><img src="_images/export.png" alt="Экспорт диаграммы"></td>
    </tr>
    <tr>
        <td>Импорт диаграммы</td>
        <td><img src="_images/import.gif" alt="Импорт диаграммы"></td>
    </tr>
    <tr>
        <td>Изменить тип диаграммы</td>
        <td><img src="_images/convert_to_type.png" alt="Изменить тип диаграммы"></td>
    </tr>    
    <tr>
	    <th colspan="2">Операции отмены и повтора действий</th>
    </tr>
    <tr>
        <td>Отмена действия</td>
        <td><img src="_images/undo.gif" alt="Отмена действия"></td>
    </tr>
    <tr>
        <td>Повтор действия</td>
        <td><img src="_images/redo.gif" alt="Шина"></td>
    </tr>
    <tr>
        <th colspan="2">Операции масштабирования диаграммы</th>
    </tr>
    <tr>
        <td>Уменьшить масштаб диаграммы</td>
        <td><img src="_images/zoom_out.png" alt="Уменьшить масштаб диаграммы"></td>
    </tr>
    <tr>
        <td>Увеличить масштаб диаграммы</td>
        <td><img src="_images/zoom_in.png" alt="Увеличить масштаб диаграммы"></td>
    </tr>
    <tr>
        <td>Отобразить полноразмерный вид диаграммы</td>
        <td><img src="_images/fit_to_screen.png" alt="Отобразить полноразмерный вид диаграммы"></td>
	</tr>
	<tr>
        <th colspan="2">Опции отображения диаграмм</th>
    </tr>
	<tr>
        <td>Автоматическая расстановка ребер при перемещении узлов диаграммы</td>
        <td><img src="_images/set_auto_layout.gif" alt="Автоматическая расстановка ребер при перемещении узлов диаграммы"></td>
    </tr>
	<tr>
        <td>Настройки визуального отображения диаграммы</td>
        <td><img src="_images/options.gif" alt="Настройки визуального отображения диаграммы"></td>
    </tr>
	<tr>
	 <th colspan="2">Удаление и копирование элементов диаграммы</th>
    </tr>
    <tr>
        <td colspan="2">Для удаления либо копирования элементов диаграммы зажмите кнопку Control с правой кнопкой мыши и выделите нужные элементы диаграммы</td>
    </tr>
	<tr>
        <td>Удаление элемента/элементов диаграммы</td>
        <td><img src="_images/remove.png" alt="Удаление элемента/элементов диаграммы"></td>
    </tr>
	<tr>
        <td>Копирование элемента/элементов диаграммы в новую диаграмму</td>
        <td><img src="_images/copy.png" alt="Копирование элемента/элементов диаграммы в новую диаграмму"></td>
    </tr>
	<tr>
	 <th colspan="2">Опции выравнивания диаграммы</th>
    </tr>
	<tr>
        <td colspan="2">Для выравнивания зажмите кнопку Control с правой кнопкой мыши и выделите нужные элементы диаграммы</td>
    </tr>
	<tr>
       <td>Выравнивание по верхнему краю</td>
       <td><img src="_images/align_up.png" alt="Выравнивание по верхнему краю"></td>
    </tr>	
    <tr>
       <td>Выравнивание по середине</td>
       <td><img src="_images/align_middle.png" alt="Выравнивание по середине"></td>
    </tr>
    <tr>
       <td>Выравнивание по нижнему краю</td>
       <td><img src="_images/align_down.png" alt="Выравнивание по нижнему краю"></td>
    </tr>
    <tr>
       <td>Выравнивание по левому краю</td>
       <td><img src="_images/align_left.png" alt="Выравнивание по левому краю"></td>
    </tr>
    <tr>
       <td>Выравнивание по центру</td>
       <td><img src="_images/align_center.png" alt="Выравнивание по центру"></td>
    </tr>
    <tr>
       <td>Выравнивание по правому краю</td>
       <td><img src="_images/align_right.png" alt="Выравнивание по правому краю"></td>
    </tr>
	<tr>
       <td>Горизонтальное выравнивание</td>
       <td><img src="_images/distribute_horizontally.png" alt="Горизонтальное выравнивание"></td>
    </tr>
	<tr>
       <td>Вертикальное выравнивание</td>
       <td><img src="_images/distribute_vertically.png" alt="Вертикальное выравнивание"></td>
    </tr>
	<tr>
	 <th colspan="2">Add upstream/downstream</th>
    </tr>
	<tr>
       <td>Add upstream</td>
       <td><img src="_images/distribute_vertically.png" alt="Add upstream"></td>
    </tr>
	<tr>
       <td>Add downstream</td>
       <td><img src="_images/distribute_vertically.png" alt="Add downstream"></td>
    </tr>
	<tr>
	 <th colspan="2">Опции модульного моделирования</th>
    </tr>
	<tr>
       <td>Смена порта</td>
       <td><img src="_images/change_port.png" alt="Смена порта"></td>
    </tr>
	<tr>
       <td>Смена подмодуля</td>
       <td><img src="_images/change_subdiagram.png" alt="Смена подмодуля"></td>
    </tr>	
	<tr>
       <td>Разделение диаграммы на подмодули</td>
       <td><img src="_images/split_diagram.png" alt="Разделение диаграммы на подмодули"></td>
    </tr>	
    <tr>
       <td>Отобразить изменения в подмоделях на модульной диаграмме</td>
       <td><img src="_images/update_submodel.png" alt="Отобразить изменения в подмоделях на модульной диаграмме"></td>
    </tr>
    <tr>
	 <th colspan="2">Опции клонирования сущностей</th>
    </tr>
	<tr>
       <td>Создание клона сущности</td>
       <td><img src="_images/clone_node.png" alt="Создание клона сущности"></td>
    </tr>
	<tr>
       <td>Объединение клонов сущностей</td>
       <td><img src="_images/merge_node.png" alt="Объединение клонов сущностей"></td>
    </tr>
   </table>

   <div class="table-bottom-margin"></div>

Поле операций 
-------------

:doc:`Поле операций </user_interface>` располагается в правой нижней части и содержит ряд вкладок, предоставляющих
различные опции при работе с диаграммами :ref:`(Рисунок 4) <Pic.4>`.

.. _Pic.4:

.. figure:: /images/interface/operations_field.png
   :width: 100%
   :alt: Поле операций при работе с диаграммами
   :align: center

   Рисунок 4. Поле операций при работе с диаграммами

Overview
~~~~~~~~

Во вкладке Overview :ref:`(Рисунок 5) <Pic.5>`отображается *общий вид диаграммы*. Синим пунктиром выделена область диаграммы, которая отображается
в рабочем пространстве. 

.. _Pic.5:

.. figure:: /images/interface/overview.png
   :width: 100%
   :alt: Вкладка Overview в поле операций
   :align: center

   Рисунок 5. Вкладка Overview в поле операций

Layout
~~~~~~

.. |save_layout| image:: /images/icons/save_layout.gif
.. |simulate| image:: /images/icons/simulate.gif

Вкладка Layout :ref:`(Рисунок 6) <Pic.6>` содержит пять вариантов *макетов расстановки элементов на диаграмме* и соответствующие опции для выбранного макета: 

.. _Pic.6:

.. figure:: /images/interface/layout.png
   :width: 100%
   :alt: Вкладка Layout в поле операций
   :align: center

   Рисунок 6. Вкладка Layout в поле операций

-   Hierarchical layout;
-   Orthogonal layout;
-   Force directed layout;
-   Cross cost grid layout (with compartments);
-   Grid layout. 

При изменении опций нажмите иконку |save_layout| и затем для запуска расстановщика иконку |simulate|.

Model
~~~~~

Вкладка Model :ref:`(Рисунок 7) <Pic.7>` содержит горизонтальные вкладки, соответвующие добавленным типам элементов на диаграмму.

.. _Pic.7:

.. figure:: /images/interface/layout.png
   :width: 100%
   :alt: Вкладка Model в поле операций
   :align: center

   Рисунок 7. Вкладка Model в поле операций 






	 



