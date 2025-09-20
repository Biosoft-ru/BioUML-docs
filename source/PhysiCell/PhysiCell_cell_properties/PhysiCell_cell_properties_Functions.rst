.. _PhysiCell_cell_properties_Functions:

Функции, описывающие поведение клетки (Functions)
=================================================

.. role:: raw-html(raw)
   :format: html

.. |icon_option| image:: /images/icons/option.png

После нажатия на вкладку **Functions** на панели свойств справа у вас появится меню, в котором можно редактировать функции, описывающие поведение клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Functions_menu.png
   :width: 100%
   :alt: Functions_menu
   :align: center

:raw-html:`<br>`
Всего можно редактировать 11 функций, каждая из которых описывает отдельный аспект жизни клетки.

.. figure:: /images/Physicell/Physicell_cell_properties/Functions_all.png
   :width: 100%
   :alt: Functions_all
   :align: center

:raw-html:`<br>`
Для каждой из этих функций доступно на выбор несколько сценариев поведения. Выбрать тот или иной сценарий можно, нажав ЛКМ справа от соответствующей функции и выбрав в раскрывающемся списке нужный сценарий.

.. figure:: /images/Physicell/Physicell_cell_properties/Many_scenario.png
   :width: 100%
   :alt: Many_scenario
   :align: center

:raw-html:`<br>`
Ниже представлен список всех функций и доступных сценариев для каждой из них:

.. raw:: html

   <ul>
      <li><b>Phenotype update</b>: общее описание поведения клетки, изменения ее поведения в зависимости от внешних и внутренних сигналов.
      <ul>
         <li><u>Default O2-based phenotype</u> - описывает жизнедеятельность клетки в зависимости от концентрации кислорода в среде.</li>
      </ul>
      </li>
      <li><b>Volume update</b>: описывает изменение всех объемных свойств клетки (количество жидкости, объем ядра и т.д.), включая и сам общий объем клетки.
      <ul>
         <li><u>Standard volume update</u> - задает зависимость свойств от объема по умолчанию.</li>
      </ul>
      </li>
      <li><b>Custom rule</b>: дополнительная функция поведения клетки.
      <ul>
         <li><u>Avoid microenvironment boundaries</u> - клетка избегает границ внешней среды,</li>
         <li><u>Wrap microenvironment boundaries</u> - клетка проходит сквозь границу на другой край внешней среды.</li>
      </ul>
      </li>
      <li><b>Velocity update</b>: описывает изменение скорости передвижения клетки.
      <ul>
         <li><u>Standard Velocity</u> - скорость клетки меняется по правилам по умолчанию в зависимости от заданных свойств хемотаксисов, степеней адгезии и отклонения и присутствия других клеток вокруг.</li>
      </ul>
      </li>
      <li><b>Migration update</b>: описывает передвижения клетки.
      <ul>
         <li><u>Chemotaxis</u> - хемотаксис по градиенту одного вещества,</li>
         <li><u>Advanced chemotaxis (weighted combination of gradients)</u> - хемотаксис по градиентам нескольких веществ с соответствующими чувствительностями,</li>
         <li><u>Advanced normalize chemotaxis (weighted combination of normalized gradients)</u> - хемотаксис по нормализованным градиентам нескольких веществ с соответствующими чувствительностями.</li>
      </ul>
      </li>
      <li><b>Membrane interaction</b>: описывает взаимодействие клетки с базальной мембраной (<span style="color: red;">сама базальная мембрана не моделируется, предполагается, что вся система расположена на ней</span>).
      <ul>
         <li><u>Avoid domain edge</u> - клетка избегает границы мембраны.</li>
      </ul>
      </li>
      <li><b>Membrane distance calculator</b>: описывает расчет клеткой расстояния до базальной мембраны.
      <ul>
         <li><u>Domain edge distance</u> - рассчитывает расстояние до края мембраны.</li>
      </ul>
      </li>
      <li><b>Orientation</b>: описывает изменение ориентации клетки в пространстве.
      <ul>
         <li><u>Up orientation</u> - ориентация параллельно оси Z.</li>
      </ul>
      </li>
      <li><b>Contact</b>: описывает контакт клетки с другими клетками.
      <ul>
         <li><u>Standard Elastic Contact</u> - эластичная адгезия/отталкивание от других типов клеток.</li>
      </ul>
      </li>
      <li><b>Cell creation</b>: описывает процесс создания новой клетки во время деления или при начальной инициализации.</li>
      <li><b>Cell division</b>: описывает процесс деления клетки.
      <ul>
         <li><u>Standard asymmetric division</u> - клетка делится асимметрично.</li>
      </ul>
      </li>
   </ul>

Также для каждой функции можно выбрать сценарий «**Custom...**». При таком выборе ниже функции, для которой был выбран данный сценарий, появится дополнительная вкладка |icon_option| «**Custom [название функции]**», в которой нужно указать путь до Java-кода, который будет описывать поведение клетки в рамках соответствующей функции.

.. figure:: /images/Physicell/Physicell_cell_properties/Custom_scenario.png
   :width: 100%
   :alt: Custom_scenario
   :align: center

:raw-html:`<br>`