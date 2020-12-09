# day7
-------
# 함수의 매개변수
## 위치기반
```
def first(a, b):   # 위치기반으로 인자 전달!
    return a + b

first(1,2)
```
> 3
```
def first(a, b = 0):   # 위치 기반 기본값
    return a + b
    
first(10)
```
> 10
## 이름기반
### 함수 매개변수 이름이 로컬 네임스페이스의 객체 이름!!!
```
def first(a, b):
    print(locals())
    return a + b

first(10, 20)
```
> {'a': 10, 'b': 20}     
30

### 이름으로 전달하면 위치와 관련이 없다!
```
first(b = 10, a = 20)
```
> {'a': 20, 'b': 10}     
30

## 가변인자를 위한 ```*```, ```**```
```
def second(*args):
    print(locals())
   
second(1,2,3,4,5)
```
> {'args': (1, 2, 3, 4, 5)}

```*``` 매개변수하고 위치기반이 함께 쓰이면!    
```
def third(x, *args):
    print(locals())
```
```
third(100)
```
> {'x': 100, 'args': ()}
```
third(10,20, 30, 40)
```
> {'x': 10, 'args': (20, 30, 40)}
# 데코레이터

# Comprehensions

