# Alquerque
Реализация игры Alquerque на Haskell.

Описание : https://www.mastersofgames.com/rules/alquerque-rules.htm

Демо : https://www.youtube.com/watch?v=M3VARJ0uqjQ&t=4s

### Оборудование

Игра в Алькерке проводится на специальной доске размером 5 x 5 очков с линиями между ними, обозначающими разрешенные ходы. Нарисовать доску несложно. Сначала нарисуйте ортогональную сетку 5 x 5. Нарисуйте две диагональные линии - от каждого угла до противоположного угла. Наконец, нарисуйте четыре диагональные линии в форме квадрата, который соединяет середины каждой стороны. В Alquerque играют 12 черными и 12 белыми фигурами аналогично шашкам.

### Подготовка и цель

Подбросьте монету, чтобы решить, кто играет первым. Игра первым обычно считается невыгодной из-за отсутствия вариантов. Игрок, играющий черными фигурами, размещает их на 10 точках ближайших 2 рядов плюс 2 крайние правые точки в среднем ряду, когда игрок смотрит на них. Другой игрок расставляет белые фигуры точно так же. Остается только средняя точка без части. Цель игры - захватить все фишки противника или занять позицию, при которой противник не может двигаться.

### Игра

Игроки по очереди перемещают одну из своих фигур. Фигура может двигаться только по линиям, начертанным на доске. Каждый ход фигура делает либо захват, либо обычный ход.
Если к фигуре примыкает фигура соперника, а точка сразу за фигурой соперника свободна, фигура противника может быть взята. Фигура берется, просто перепрыгивая через нее в свободное место и удаляя ее с доски. В отличие от обычного хода, ход захвата может состоять из нескольких таких прыжков - если фигура берет фигуру соперника, и новое положение позволяет ей взять другую фигуру, то она может сделать это сразу. Ход заканчивается, когда позиция захватывающей фигуры больше не позволяет ей брать другие фигуры или игрок может сделать еще один захват, но решает не делать этого. Обычный ход делается простым перемещением фишки по линии в соседнюю точку.

### Завершение

Игра выигрывает игрок, которому первым удается взять все фишки своего противника, или игрок, у которого больше фишек, когда становится очевидным, что больше фишек не будет. В качестве альтернативы игрок может выиграть, лишив другого игрока возможности двигаться.
Ничья происходит по договоренности в любой момент игры. Если становится очевидным, что больше не будут взяты фишки и у обоих игроков останется одинаковое количество фишек, соглашается ничья. Розыгрыши очень распространены.
