# copy code
```python
import bisect

n = int(input())
a = list(map(int, input().split()))
m = int(input())
q = list(map(int, input().split()))

# Создаём префиксные суммы
prefix = []
current_sum = 0
for x in a:
    current_sum += x
    prefix.append(current_sum)

# Для каждого номера червя находим кучку
for worm_num in q:
    # Бинарный поиск позиции, где worm_num <= prefix[i]
    index = bisect.bisect_left(prefix, worm_num)
    print(index + 1)  # +1, так как нумерация кучек с 1
```
