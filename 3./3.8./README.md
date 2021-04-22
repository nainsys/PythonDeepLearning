# 4.8.    숫자형 활용

숫자형\(Number\)이란 숫자 형태로 이루어진 자료형을 말합니다. 숫자형 변수의 객체는 값을 할당 할 때 만들어 진다.

```python
var1 = 1
var2 = 10
```

del 문을 사용하여 숫자 개체에 대한 참조를 삭제할 수도 있습니다. del 문을 사용하여 단일 개체 또는 여러 개체를 삭제할 수 있습니다.

```python
del var
del var_a, var_b
```

파이썬은 네 가지 다른 숫자 타입을 지원합니다.

*  int \(부호 있는 정수\) - 소수점이 없는 양수 또는 음수입니다.
*  long \(long integer\) - long이라고도하며 정수가 아닌 무한대의 정수이며 대문자 또는 소문자 L이 뒤에 온다.
*  float \(부동 소수점 실수 값\) - 실수를 말하며 정수와 소수 부분을 나누는 소수점으로 기록됩니다. 컴퓨터식 지수 표현 방식으로 E 또는 e가 10의 지수 \(2.5e2 = 2.5 x 102 = 250\)를 나타낼 수 있습니다.
*  복소수 \(복소수\) - a + bJ의 형식입니다. 여기서 a와 b는 부동이며 J \(또는 j\)는 -1의 제곱근 \(허수 임\)을 나타냅니다. 수의 실수 부분은 a이고, 허수 부분은 b입니다.  

#### 3.8.1.     숫자형 변환

숫자형 변환 함수는 다음과 같은 것들이 있습니다.

| **int\(x\)** | **x를** **일반** **정수로** **변환합니다.** |
| :--- | :--- |
| **long\(x\)**  | x를 long integer\(긴 정수\)로 변환합니다. |
| **float\(x\)**  | x를 부동 소수점 숫자로 변환합니다. |
| **complex\(x\)**  | x를 실수 부분 x와 허수 부분 0이있는 복소수로 변환 |
| **complex\(x, y\)**  | x와 y를 실수 부분 x와 허수 부분 y가있는 복소수로 변환 |

#### 3.8.2.     수학 함수

파이썬에는 다음과 같은 수학 함수들이 있습니다.

| [**abs\(x\)**](https://www.tutorialspoint.com/python/number_abs.htm) | X의 절대값을 반환 |
| :--- | :--- |
| [**ceil\(x\)**](https://www.tutorialspoint.com/python/number_ceil.htm) | x보다 작지 않은 최소 정수, ceil\(2.1\) = 3 |
| [**cmp\(x, y\)**](https://www.tutorialspoint.com/python/number_cmp.htm) | x &lt;y의 경우는 -1, x == y의 경우는 0, x&gt; y의 경우는 1, Python 2.x에서만 사용 가능 |
| [**exp\(x\)**](https://www.tutorialspoint.com/python/number_exp.htm) | The exponential of x: ex |
| [**fabs\(x\)**](https://www.tutorialspoint.com/python/number_fabs.htm) | 실수 x의 절대 값 |
| [**floor\(x\)**](https://www.tutorialspoint.com/python/number_floor.htm) | x보다 크지 않은 가장 큰 정수. floor\(2.1\)=2 |
| [**log\(x\)**](https://www.tutorialspoint.com/python/number_log.htm) | x&gt; 0에 대한 x의 자연 로그 |
| [**log10\(x\)**](https://www.tutorialspoint.com/python/number_log10.htm) | x&gt; 0에 대한 x의 base-10인 대수입니다. |
| [**max\(x1, x2,...\)**](https://www.tutorialspoint.com/python/number_max.htm) | x1,x2… 중 가장 큰 인수 |
| [**min\(x1, x2,...\)**](https://www.tutorialspoint.com/python/number_min.htm) | X1,x2… 중 가장 작은 인수 |
| [**modf\(x\)**](https://www.tutorialspoint.com/python/number_modf.htm) | 두 항목 튜플의 x 부분 및 정수 부분. 두 부분의 부호는 x와 같습니다. 정수 부분은 float 형식으로 반환됩니다. |
| [**pow\(x, y\)**](https://www.tutorialspoint.com/python/number_pow.htm) | x \*\* y의 값. \(=x^y\)  x의 y승 예를 들어 pow\(2,3\)=8 |
| [**round\(x \[,n\]\)**](https://www.tutorialspoint.com/python/number_round.htm) | 소수점에서 n 자릿수로 반올림 한 값. round \(0,5\)는 1.0이고 round \(-0,5\)는 -1.0이다 |
| [**sqrt\(x\)**](https://www.tutorialspoint.com/python/number_sqrt.htm) | x&gt; 0에 대한 x의 제곱근 |

파이썬에는 다음과 같은 상수들이 있습니다.

| e | e |
| :--- | :--- |
| pi | π |
| tau | τ |
| inf | ∞ |
| nan | Not a Number |

수학 함수를 다음과 같은 코드로 테스트 해 봅니다.

```python
import math    #Python 3.x 버전부터는 cmp 함수를 지원하지 않으므로 함수를 별도로 선언해 준다.
def cmp(a, b):
    return (a > b) - (a < b)        

print('Absolute value of integer is:', abs(-54.26))     # floating point number    
print('Absolute value of float is:', abs(-94))          # An integer    
complex = (3 - 4j)                                           # A complex number    
print('Absolute value or Magnitude of complex is:', abs(complex))        
print("cmp(10,20): ", cmp(10,20))    
print("cmp(10,10): ", cmp(10,10))    
print("cmp(20,10): ", cmp(20,10))    
print("cmp('ABC','PQR'): ", cmp('ABC','PQR'))        
print("math.floor(-23.11) : ", math.floor(-23.11))    
print("math.floor(300.16) : ", math.floor(300.16))    
print("math.floor(300.72) : ", math.floor(300.72) )        
print("math.ceil(-23.11) : ", math.ceil(-23.11))    
print("math.ceil(300.16) : ", math.ceil(300.16))    
print("math.ceil(300.72) : ", math.ceil(300.72))        
print("math.exp(-45.17) : ", math.exp(-45.17))    
print("math.exp(100.12) : ", math.exp(100.12))        
print("math.fabs(-45.17) : ", math.fabs(-45.17))    
print("math.fabs(100.12) : ", math.fabs(100.12))        
print("Natural logarithm of 14 is : ", math.log(14))    
print("Logarithm base 5 of 14 is : ", math.log(14, 5))    
print ("Logarithm base 10 of 14 is : ", math.log10(14))    
num = [1, 3, 2, 8, 5, 10, 6]    
print('Maximum is:', max(num))    
print('Maximum is:', min(num))        
print("math.modf(100.12) : ", math.modf(100.12))
tpl = (33.12, -15.25, 3.15, -31.2)  

# positive x, positive y (x**y)    
print("modf() on Second tuple element : ", math.modf(tpl[1]))        
  
print("pow(2,3) : ",pow(2, 3))        # for floating point round    
print("round(51.6)  : ",round(51.6))    
print("round(51.5)  : ",round(51.5))    
print("round(51.4)  : ",round(51.4))        
print("math.sqrt(100) : ", math.sqrt(100))    
print("math.sqrt(7) : ", math.sqrt(7))    
print("math.sqrt(math.pi) : ", math.sqrt(math.pi)) 
```

![](../../.gitbook/assets/3820.png)

#### 3.8.3.     난수 함수, 삼각함수

난수\(임의의 숫자\)는 게임, 시뮬레이션, 테스트, 보안 및 개인 정보 보호 응용 프로그램에 사용됩니다. 파이썬에는 일반적으로 사용되는 다음과 같은 난수 함수가 있습니다.

| [**choice\(seq\)**](https://www.tutorialspoint.com/python/number_choice.htm) | 목록, 튜플 또는 문자열에서 임의 항목 선택. |
| :--- | :--- |
| [**randrange \(\[start,\] stop \[,step\]\)**](https://www.tutorialspoint.com/python/number_randrange.htm) | range\(start, stop, step\) 범위에서 임의로 선택된 요소 |
| [**random\(\)**](https://www.tutorialspoint.com/python/number_random.htm) | 0이 r보다 작거나 같고 r이 1보다 작은 임의의 부동 소수점 r |
| [**seed\(\[x\]\)**](https://www.tutorialspoint.com/python/number_seed.htm) | 난수 생성에 사용되는 정수 시작 값을 설정합니다. 다른 난수 함수를 호출하기 전에 이 함수를 호출해야 함 |
| [**shuffle\(lst\)**](https://www.tutorialspoint.com/python/number_shuffle.htm) | 목록의 항목을 무작위로 배치 |
| [**uniform\(x, y\)**](https://www.tutorialspoint.com/python/number_uniform.htm) | x가 r보다 작거나 같고 r이 y보다 작은 임의의 float r |

파이썬에는 삼각 함수 계산을 수행하는 함수가 포함되어 있습니다.

| Sr.No. | Function & Description |
| :--- | :--- |
| [**acos\(x\)**](https://www.tutorialspoint.com/python/number_acos.htm) | 라디안 단위의 x의 아크 코사인을 반환합니다. |
| [**asin\(x\)**](https://www.tutorialspoint.com/python/number_asin.htm) | 라디안 단위의 x의 아크 사인을 반환합니다. |
| [**atan\(x\)**](https://www.tutorialspoint.com/python/number_atan.htm) | x의 아크 탄젠트를 라디안 단위로 반환합니다. |
| [**atan2\(y, x\)**](https://www.tutorialspoint.com/python/number_atan2.htm) | atan \(y / x\)를 라디안 단위로 반환합니다. |
| [**cos\(x\)**](https://www.tutorialspoint.com/python/number_cos.htm) | x 라디안의 코사인을 반환합니다. |
| [**hypot\(x, y\)**](https://www.tutorialspoint.com/python/number_hypot.htm) | 유클리드 표준 인 sqrt \(x \* x + y \* y\)를 반환합니다. |
| [**sin\(x\)**](https://www.tutorialspoint.com/python/number_sin.htm) | x 라디안의 사인을 반환합니다. |
| [**tan\(x\)**](https://www.tutorialspoint.com/python/number_tan.htm) | x 라디안의 탄젠트를 반환합니다. |
| [**degrees\(x\)**](https://www.tutorialspoint.com/python/number_degrees.htm) | 각도 x를 라디안에서 각도로 변환합니다. |
| [**radians\(x\)**](https://www.tutorialspoint.com/python/number_radians.htm) | 각도 x를도 단위에서 라디안 단위로 변환합니다. |







