Interview [mitbbs](http://www.mitbbs.com/article_t/JobHunting/32651839.html) for Groupon 

```python
def find_five(n):
    ret = []
    helper(ret, [], n)
    return ret

def helper(ret, res, n):
    if len(res) > 0 and ( int(''.join(res)) > n or len(res) > len(str(n)) ):
        #print "out, res: ", int(''.join(res))
        return
    if '5' in res and int(''.join(res)) not in ret:
        ret.append(int(''.join(res)))
        print "ret: ", ret

    for i in range(10):
        res.append(str(i))
        print "res: ", res
        helper(ret, res, n)
        res.pop()

print find_five(60)

```

```
Output

[JINZH2-M-20GQ: ~/Desktop/Python_training/Leetcode]: python print_five.py
res:  ['0']
res:  ['0', '0']
res:  ['0', '0', '0']
res:  ['0', '0', '1']
res:  ['0', '0', '2']
res:  ['0', '0', '3']
res:  ['0', '0', '4']
res:  ['0', '0', '5']
res:  ['0', '0', '6']
res:  ['0', '0', '7']
res:  ['0', '0', '8']
res:  ['0', '0', '9']
res:  ['0', '1']
res:  ['0', '1', '0']
res:  ['0', '1', '1']
res:  ['0', '1', '2']
res:  ['0', '1', '3']
res:  ['0', '1', '4']
res:  ['0', '1', '5']
res:  ['0', '1', '6']
res:  ['0', '1', '7']
res:  ['0', '1', '8']
res:  ['0', '1', '9']
res:  ['0', '2']
res:  ['0', '2', '0']
res:  ['0', '2', '1']
res:  ['0', '2', '2']
res:  ['0', '2', '3']
res:  ['0', '2', '4']
res:  ['0', '2', '5']
res:  ['0', '2', '6']
res:  ['0', '2', '7']
res:  ['0', '2', '8']
res:  ['0', '2', '9']
res:  ['0', '3']
res:  ['0', '3', '0']
res:  ['0', '3', '1']
res:  ['0', '3', '2']
res:  ['0', '3', '3']
res:  ['0', '3', '4']
res:  ['0', '3', '5']
res:  ['0', '3', '6']
res:  ['0', '3', '7']
res:  ['0', '3', '8']
res:  ['0', '3', '9']
res:  ['0', '4']
res:  ['0', '4', '0']
res:  ['0', '4', '1']
res:  ['0', '4', '2']
res:  ['0', '4', '3']
res:  ['0', '4', '4']
res:  ['0', '4', '5']
res:  ['0', '4', '6']
res:  ['0', '4', '7']
res:  ['0', '4', '8']
res:  ['0', '4', '9']
res:  ['0', '5']
ret:  [5]
<skip>
res:  ['4', '3']
res:  ['4', '3', '0']
res:  ['4', '3', '1']
res:  ['4', '3', '2']
res:  ['4', '3', '3']
res:  ['4', '3', '4']
res:  ['4', '3', '5']
res:  ['4', '3', '6']
res:  ['4', '3', '7']
res:  ['4', '3', '8']
res:  ['4', '3', '9']
res:  ['4', '4']
res:  ['4', '4', '0']
res:  ['4', '4', '1']
res:  ['4', '4', '2']
res:  ['4', '4', '3']
res:  ['4', '4', '4']
res:  ['4', '4', '5']
res:  ['4', '4', '6']
res:  ['4', '4', '7']
res:  ['4', '4', '8']
res:  ['4', '4', '9']
res:  ['4', '5']
ret:  [5, 15, 25, 35, 45]
res:  ['4', '5', '0']
res:  ['4', '5', '1']
res:  ['4', '5', '2']
res:  ['4', '5', '3']
res:  ['4', '5', '4']
res:  ['4', '5', '5']
res:  ['4', '5', '6']
res:  ['4', '5', '7']
res:  ['4', '5', '8']
res:  ['4', '5', '9']
res:  ['4', '6']
res:  ['4', '6', '0']
res:  ['4', '6', '1']
res:  ['4', '6', '2']
res:  ['4', '6', '3']
res:  ['4', '6', '4']
res:  ['4', '6', '5']
res:  ['4', '6', '6']
res:  ['4', '6', '7']
res:  ['4', '6', '8']
res:  ['4', '6', '9']
res:  ['4', '7']
res:  ['4', '7', '0']
res:  ['4', '7', '1']
res:  ['4', '7', '2']
res:  ['4', '7', '3']
res:  ['4', '7', '4']
res:  ['4', '7', '5']
res:  ['4', '7', '6']
res:  ['4', '7', '7']
res:  ['4', '7', '8']
res:  ['4', '7', '9']
res:  ['4', '8']
res:  ['4', '8', '0']
res:  ['4', '8', '1']
res:  ['4', '8', '2']
res:  ['4', '8', '3']
res:  ['4', '8', '4']
res:  ['4', '8', '5']
res:  ['4', '8', '6']
res:  ['4', '8', '7']
res:  ['4', '8', '8']
res:  ['4', '8', '9']
res:  ['4', '9']
res:  ['4', '9', '0']
res:  ['4', '9', '1']
res:  ['4', '9', '2']
res:  ['4', '9', '3']
res:  ['4', '9', '4']
res:  ['4', '9', '5']
res:  ['4', '9', '6']
res:  ['4', '9', '7']
res:  ['4', '9', '8']
res:  ['4', '9', '9']
res:  ['5']
res:  ['5', '0']
ret:  [5, 15, 25, 35, 45, 50]
res:  ['5', '0', '0']
res:  ['5', '0', '1']
res:  ['5', '0', '2']
res:  ['5', '0', '3']
res:  ['5', '0', '4']
res:  ['5', '0', '5']
res:  ['5', '0', '6']
res:  ['5', '0', '7']
res:  ['5', '0', '8']
res:  ['5', '0', '9']
res:  ['5', '1']
ret:  [5, 15, 25, 35, 45, 50, 51]
res:  ['5', '1', '0']
res:  ['5', '1', '1']
res:  ['5', '1', '2']
res:  ['5', '1', '3']
res:  ['5', '1', '4']
res:  ['5', '1', '5']
res:  ['5', '1', '6']
res:  ['5', '1', '7']
res:  ['5', '1', '8']
res:  ['5', '1', '9']
res:  ['5', '2']
ret:  [5, 15, 25, 35, 45, 50, 51, 52]
res:  ['5', '2', '0']
res:  ['5', '2', '1']
res:  ['5', '2', '2']
res:  ['5', '2', '3']
res:  ['5', '2', '4']
res:  ['5', '2', '5']
res:  ['5', '2', '6']
res:  ['5', '2', '7']
res:  ['5', '2', '8']
res:  ['5', '2', '9']
res:  ['5', '3']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53]
res:  ['5', '3', '0']
res:  ['5', '3', '1']
res:  ['5', '3', '2']
res:  ['5', '3', '3']
res:  ['5', '3', '4']
res:  ['5', '3', '5']
res:  ['5', '3', '6']
res:  ['5', '3', '7']
res:  ['5', '3', '8']
res:  ['5', '3', '9']
res:  ['5', '4']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54]
res:  ['5', '4', '0']
res:  ['5', '4', '1']
res:  ['5', '4', '2']
res:  ['5', '4', '3']
res:  ['5', '4', '4']
res:  ['5', '4', '5']
res:  ['5', '4', '6']
res:  ['5', '4', '7']
res:  ['5', '4', '8']
res:  ['5', '4', '9']
res:  ['5', '5']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55]
res:  ['5', '5', '0']
res:  ['5', '5', '1']
res:  ['5', '5', '2']
res:  ['5', '5', '3']
res:  ['5', '5', '4']
res:  ['5', '5', '5']
res:  ['5', '5', '6']
res:  ['5', '5', '7']
res:  ['5', '5', '8']
res:  ['5', '5', '9']
res:  ['5', '6']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55, 56]
res:  ['5', '6', '0']
res:  ['5', '6', '1']
res:  ['5', '6', '2']
res:  ['5', '6', '3']
res:  ['5', '6', '4']
res:  ['5', '6', '5']
res:  ['5', '6', '6']
res:  ['5', '6', '7']
res:  ['5', '6', '8']
res:  ['5', '6', '9']
res:  ['5', '7']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55, 56, 57]
res:  ['5', '7', '0']
res:  ['5', '7', '1']
res:  ['5', '7', '2']
res:  ['5', '7', '3']
res:  ['5', '7', '4']
res:  ['5', '7', '5']
res:  ['5', '7', '6']
res:  ['5', '7', '7']
res:  ['5', '7', '8']
res:  ['5', '7', '9']
res:  ['5', '8']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55, 56, 57, 58]
res:  ['5', '8', '0']
res:  ['5', '8', '1']
res:  ['5', '8', '2']
res:  ['5', '8', '3']
res:  ['5', '8', '4']
res:  ['5', '8', '5']
res:  ['5', '8', '6']
res:  ['5', '8', '7']
res:  ['5', '8', '8']
res:  ['5', '8', '9']
res:  ['5', '9']
ret:  [5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59]
res:  ['5', '9', '0']
res:  ['5', '9', '1']
res:  ['5', '9', '2']
res:  ['5', '9', '3']
res:  ['5', '9', '4']
res:  ['5', '9', '5']
res:  ['5', '9', '6']
res:  ['5', '9', '7']
res:  ['5', '9', '8']
res:  ['5', '9', '9']
res:  ['6']
res:  ['6', '0']
res:  ['6', '0', '0']
res:  ['6', '0', '1']
res:  ['6', '0', '2']
res:  ['6', '0', '3']
res:  ['6', '0', '4']
res:  ['6', '0', '5']
res:  ['6', '0', '6']
res:  ['6', '0', '7']
res:  ['6', '0', '8']
res:  ['6', '0', '9']
res:  ['6', '1']
res:  ['6', '2']
res:  ['6', '3']
res:  ['6', '4']
res:  ['6', '5']
res:  ['6', '6']
res:  ['6', '7']
res:  ['6', '8']
res:  ['6', '9']
res:  ['7']
res:  ['7', '0']
res:  ['7', '1']
res:  ['7', '2']
res:  ['7', '3']
res:  ['7', '4']
res:  ['7', '5']
res:  ['7', '6']
res:  ['7', '7']
res:  ['7', '8']
res:  ['7', '9']
res:  ['8']
res:  ['8', '0']
res:  ['8', '1']
res:  ['8', '2']
res:  ['8', '3']
res:  ['8', '4']
res:  ['8', '5']
res:  ['8', '6']
res:  ['8', '7']
res:  ['8', '8']
res:  ['8', '9']
res:  ['9']
res:  ['9', '0']
res:  ['9', '1']
res:  ['9', '2']
res:  ['9', '3']
res:  ['9', '4']
res:  ['9', '5']
res:  ['9', '6']
res:  ['9', '7']
res:  ['9', '8']
res:  ['9', '9']
[5, 15, 25, 35, 45, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59]
```
