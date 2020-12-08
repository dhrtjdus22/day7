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
```
def first(a, b):
    print(locals())
    return a + b

first(10, 20)
```
> {'a': 10, 'b': 20}     
30
```
first(b = 10, a = 20)
```
> {'a': 20, 'b': 10}     
30
> 이름으로 전달하면 위치와 관련이 없다!
## 가변인자를 위한 *, **

# 데코레이터

# Comprehensions

