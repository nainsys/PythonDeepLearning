# 4.9.    문자열\(Strings\) 활용



문자열은 파이썬에서 가장 인기있는 자료형입니다. 문자를 "" \(쌍따옴표\), ''\(작은따옴표\) 로 묶어 간단하게 만들 수 있습니다. 쌍따옴표와 작은따옴표를 혼용할 수는 없습니다. 큰따옴표 안에 작은따옴표가 들어갈 수 있고, 반대로 작은따옴표 안에 큰따옴표 들어갈 수 있습니다.

```python
var1 = 'Hello World!'
var2 = "It's a good thing"
```

문자열 부분집합에 액세스하려면 대괄호와 문자열 인덱스를 사용하여 문자열 부분을 가져오면 됩니다.

```python
var1 = 'Hello World!'
var2 = "Python Programming"
print "var1[0]: ", var1[0]
print "var2[1:5]: ", var2[1:5]
#출력된 결과
var1[0]:  H
var2[1:5]:  ytho
```

변수를 다른 문자열에 할당하여 기존 문자열을 "업데이트"할 수 있습니다. 새 값은 이전 값 또는 완전히 다른 문자열과 관련될 수 있습니다. 예를 들어

```python
var1 = 'Hello World!'
print "Updated String :- ", var1[:6] + 'Python'
#출력된 결과
Updated String :-  Hello Python
```

여러 줄의 문자를 입력할 때는 """ 큰따옴표 3개나, ''' 작은따옴표 3개를 입력합니다. \n 으로 표시되는 부분이 newline문자로 열을 바꿔주는 이스케이프 문자입니다.

```python
para_str = """this is a long string that is made up of
several lines and non-printable characters such as
TAB ( \t ) and they will show up that way when displayed.
NEWLINEs within the string, whether explicitly given like
this within the brackets [ \n ], or just a NEWLINE within
the variable assignment will also show up.
"""
print para_str
```

#### 

