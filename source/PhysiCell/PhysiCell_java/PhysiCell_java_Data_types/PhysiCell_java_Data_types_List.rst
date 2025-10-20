.. _PhysiCell_java_Data_types_List:

List
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

List — это интерфейс, описывающий упорядоченную коллекцию объектов какого-либо класса (не может содержать примитивные типы данных, такие как int, double, boolean и т.д.).

Основные характеристики List:

- **Упорядоченность**: элементы хранятся в том порядке, в котором они были добавлены.
- **Допускает дубликаты**: один и тот же объект может присутствовать в списке несколько раз.
- **Поддержка индексации**: каждый элемент имеет индекс (начиная с 0), что позволяет обращаться к элементам по позиции.

Поскольку List является интерфейсом, то создать объект непосредственно этого типа нельзя — можно создавать объекты классов, реализующих этот интерфейс, например:

- **ArrayList** (основан на динамическом массиве, быстрый доступ по индексу, медленные вставки/удаления в середине). 
- **LinkedList** (двусвязный список, быстрые вставки/удаления, медленный доступ по индексу).

и др.

Создание таких объектов выполняется следующим образом:

.. code-block:: text

  List<Cell> cells = new ArrayList<>();

  где,

  • List - указание на то, что реализуется интерфейс List.
  • <Cell> - указание на то, что коллекция будет содержать только объекты класса "Cell".
  • cells - имя создаваемой коллекции.
  • new — оператор, который создаёт новый объект.
  • ArrayList<>() - конкретный класс, реализующий интерфейс List.

Для того, чтобы все-таки добавить в коллекцию объекты примитивного типа, необходимо передать в коллекцию не сам этот тип, а соответствующий класс (см. пример ниже).

.. code-block:: text

  List<Double> my_list = ArrayList<>(); // Правильный вариант, т.к. Double (с заглавной буквы) является классом

  List<double> my_list = ArrayList<>(); // Неправильный вариант, т.к. double (со строчной буквы) является примитивным типом данных

Ниже приведены основные методы работы с интерфейсом List:

1. Добавление элемента в конец коллекции.

.. code-block:: text
  
  cells.add(cell1);
  cells.add(cell2);
  cells.add(cell3);

  System.out.println(cells); // [cell1, cell2, cell3]

2. Вставка элемента по индексу.

.. code-block:: text
  
  cells.add(1, extra_cell);

  System.out.println(cells); // [cell1, extra_cell, cell2, cell3]

3. Получение элемента по индексу.

.. code-block:: text
  
  Cell first_cell = cells.get(0);

  System.out.println(first_cell); // cell1

.. important::

  Индексы элементов в коллекции начинаются с 0.

4. Изменение элемента по индексу.

.. code-block:: text
  
  cells.set(1, new_extra_cell);

  System.out.println(cells); // [cell1, new_extra_cell, cell2, cell3]

5. Поиск индекса элемента.

.. code-block:: text
  
  int index = cells.indexOf(cell2);

  System.out.println(index); // 2

.. important::

  Если элемент в коллекции отсутствует, то метод "indexOf" вернет -1.

6. Проверка наличия элемента.

.. code-block:: text
  
  boolean has_cell3 = cells.contains(cell3);

  System.out.println(has_cell3); // true

7. Удаление по индексу.

.. code-block:: text
  
  Cell removed_cell = cells.remove(0);

  System.out.println(removed_cell); // cell1
  System.out.println(cells); // [new_extra_cell, cell2, cell3]

8. Удаление по значению.

.. code-block:: text
  
  boolean removed = cells.remove(new_extra_cell);

  System.out.println(removed); // true
  System.out.println(cells); // [cell2, cell3]

.. important::
  
  Если элемент в коллекции отсутствует, то метод "remove" вернет false.

9. Размер коллекции.

.. code-block:: text

  System.out.println(cells.size()); // 2

10. Проверка на пустоту.

.. code-block:: text

  System.out.println(cells.isEmpty()); // false

.. important::

  Если коллекция не содержит ни одного элемента, то метод "isEmpty()" вернет true.

11. Добавление коллекции.

.. code-block:: text

  List<Cell> more_cells = Arrays.asList(big_cell, small_cell);

  cells.addAll(more_cells);

  System.out.println(cells); // [cell2, cell3, big_cell, small_cell]

12. Подсписок.

.. code-block:: text

  List<Cell> first_two_cells = cells.subList(0, 2); // элементы коллекции с индекса 0 до 2 (не включая 2)

  System.out.println(first_two_cells); // [cell2, cell3]

.. important::

  Любые изменения, вносимые в подсписок, автоматически происходят и с оригинальным списком, и наоборот (см. пример ниже).

.. code-block:: text

  first_two_cells.set(0, new_cell);

  System.out.println(first_two_cells); // [new_cell, cell3]
  System.out.println(cells); // [new_cell, cell3, big_cell, small_cell]

13. Преобразование в массив.

.. code-block:: text

  Cell[] arr_cells = cells.toArray(new Cell[0]);

  System.out.println(Arrays.toString(arr_cells)); // [new_cell, cell3, big_cell, small_cell]

14. Очистка коллекции.

.. code-block:: text

  cells.clear();

  System.out.println(cells); // []