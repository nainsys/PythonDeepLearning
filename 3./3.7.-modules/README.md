# 3.7.    모듈\(Modules\)

일반적으로 모듈은 부품을 의미합니다. 프로그램에서 자주 사용되는 일반적인 기능을 모듈로 한번 만들어 두면, 필요할 때 마다 활용할 수 있습니다. 모듈을 사용하면 논리적으로 파이썬 코드를 구성할 수 있습니다. 관련 코드를 모듈로 그룹화하면 코드를 더 쉽게 이해하고 사용할 수 있습니다. 모듈은 바인딩하고 참조할 수 있는, 임의로 명명 된 속성을 가진 Python 객체를 말합니다. 간단히 말해, 모듈은 파이썬 코드로 구성된 이미 존재하는 파일입니다. 파이썬에서 모듈은 관련이 있는 함수나 변수 또는 클래스 들을 모아 놓은 파일입니다. 함수는 모듈의 한 형태입니다. 모듈이 함수보다 좀 더 큰 범위를 나타낸다. 모듈보다 더 큰 개념이 패키지\(package\)입니다. 모듈은 하나의 파이썬 파일이지만 패키지는 파이썬 모듈이 들어있는 디렉토리를 말합니다.

그동안 모듈을 몇 차례 사용해 본 적이 있습니다. 예를 들어, 제곱근을 구하는 함수 sys.path\(\)를 사용기 위해 import sys 명령을 실행해야 합니다. 이 때의 import 문은 모듈을 프로그램 안으로 가져와 사용하기 위한 명령이고, sys 모듈은 시스템과 관련된 기능을 모아 놓은 모듈입니다.

다음과 같은 support.py 파이썬 파일이 있다면

```python
def print_func( par ):
   print "Hello : ", par
   return
```

다음과 같은 import 문에 의해 모듈로 support.py 모듈을 사용할 수 있습니다.

```python
# Import module support
import support
# Now you can call defined function that module as follows
support.print_func("Zara")
```

Python의 from 문을 사용하면 모듈의 특정 속성을 현재 네임스페이스로 가져올 수 있습니다. 예를 들어 fib 모듈에서 fibonacci 함수를 가져오려면 다음과 같이 사용합니다.

```text
from fib import fibonacci
```

위의 from 문은 fib 모듈 전체를 현재 네임스페이스로 가져오지 않습니다. 이것은 모듈 fib에서 fibonacci라는 항목을 import 모듈의 전역 심볼 테이블로 가져옵니다.

다음 import 문을 사용하여 모듈의 모든 이름을 현재 네임스페이스로 가져올 수도 있습니다.

```text
from modname import *
```

이렇게 하면 모듈의 모든 항목을 현재 네임 스페이스로 쉽게 가져올 수 있지만, 이런 사용 방법은 권장하지 않는다고 합니다.

