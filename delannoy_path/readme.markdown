﻿Путь из (0, 0) в (n / 2, n / 2) &mdash;
строка из n чисел 0, 1, 2, 3, которые кодируют путь из (0, 0) в (n / 2, n / 2),
если можно ходить вверх, вправо и вверх-вправо, следующим образом: 1 - R, 2 - U, 3 - RU, 0 - если путь уже пришёл в (n / 2, n / 2).

Автор: Бабенко Михаил.

OEIS: [A001850](https://oeis.org/A001850) (Central Delannoy numbers).

Ссылки:
[Википедия](https://en.wikipedia.org/wiki/Delannoy_number),
[Mathworld](http://mathworld.wolfram.com/DelannoyNumber.html).

Числа Деланнуа показывают количество выравниваний двух строк размера n и m (к примеру, нуклеотидных последовательностей).

Предподсчёт: O(n^2), где n = MAXN = 26 * 2 &mdash; максимальное число,
для которого число путей на n &times; n помещается в `int64_t`.

Функция `total`: O(1).

Функция `generate_all`: O(n * answer).

Функция `is_valid`: O(n).

Функция `number_by_object`: O(n), если меньше MAXN, O(n^2) иначе.

Функция `object_by_number`: O(n), если меньше MAXN, O(n^2) иначе.

Функция `prev`: O(n), O(1) амортизированно при последовательном вызове `prev`.

Функция `next`: O(n), O(1) амортизированно при последовательном вызове `next`.
