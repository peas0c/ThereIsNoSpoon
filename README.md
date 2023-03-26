# Решение задачи There Is No Spoon с сайта Codingame.com

### Ссылка на задачу: https://www.codingame.com/ide/puzzle/there-is-no-spoon-episode-1
 

## Условие: 

Игра ведется на прямоугольной сетке заданного размера. Некоторые ячейки содержат ноды. Остальные ячейки пусты.

Цель состоит в том, чтобы найти, если они существуют, горизонтальных и вертикальных соседей каждой ноды в игровой сетке.
  
  ## Правила
Необходимо найти каждую координату (x1,y1), содержащую ноду, и отобразить координаты (x2,y2) соседней ноды справа и координаты (x3,y3) соседней ноды снизу.

Если соседняя нода не существует, вы должны вывести координаты -1 -1 вместо (x2,y2) и/или (x3,y3).

Вы проиграете, если:
Вы указываете неверного соседа для узла.
Даешь соседям за пустую клетку.
Вы вычисляете один и тот же узел дважды.
Вы забыли вычислить соседей узла.
 
Условия победы
Вы выигрываете, когда все ноды отображаются правильно.
  ### Пример
В этом примере есть три ноды в сетке 2 на 2 там, где стоят нули. 
Ячейка (1,1) с точкой пуста(нет ноды)
 
00   
0.


Узел в (0,0) имеет 2 соседей.
0 0 1 0 0 1


Узел в (1,0) не имеет соседей.
1 0 -1 -1 -1 -1

Узел в (0,1) не имеет соседей.
0 1 -1 -1 -1 -1
  


 ## Начало игры
Программа должна сначала прочитать данные инициализации из стандартного ввода. Затем выведите на стандартный вывод по одной строке на инструкцию.

### Вход данных для инициализации:

Строка 1: одна целочисленная ширина для количества ячеек по оси x.

Строка 2: одна целочисленная высота для количества ячеек по оси Y.

Строки следующей высоты: строковая строка, содержащая символы ширины. 
Точка '.' представляет собой пустую ячейку. Ноль '0' представляет ячейку, содержащую ноду.

Вывод за один игровой ход
Одна строка на ноду. 
Шесть целых чисел в каждой строке: x1 y1 x2 y2 x3 y3

Где:
(x1,y1) координаты узла

(x2,y2) координаты ближайшего соседа справа от узла

(x3,y3) координаты ближайшего нижнего соседа

Если соседа нет, координаты должны быть -1 -1.
### Ограничения
0 < width ≤ 30
0 < height ≤ 30
0 ≤ x1 < width
0 ≤ y1 < height
-1 ≤ x2, x3 < width
-1 ≤ y2, y3 < height
Время отклика от первого до последнего вывода ≤ 1s.
Время отклика между двумя выводами строк ≤ 100ms