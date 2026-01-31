# copy code
```python
def find_kth_non_divisible(wer1, wer2):
    wer3, wer4 = wer2, wer2 + wer1
    while wer3 < wer4:
        wer5 = (wer3 + wer4) // 2
        if wer5 - wer5 // wer1 >= wer2:
            wer4 = wer5
        else:
            wer3 = wer5 + 1
    return wer3

wer6 = int(input())
for wer7 in range(wer6):
    wer8, wer9 = map(int, input().split())
    print(find_kth_non_divisible(wer8, wer9))

```
