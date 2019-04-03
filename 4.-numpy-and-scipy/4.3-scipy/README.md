# 4.3 SciPy

SciPy는 파이썬을 기반으로 하여 과학, 분석, 그리고 엔지니어링을 위한 과학\(계산\)적 컴퓨팅 영역의 여러 기본적인 작업을 위한 라이브러리입니다. Scipy는 기본적으로 Numpy, Matplotlib, Pandas, Sympy등 과 함께 동작을 합니다. NumPy와 Scipy를 함께 사용하면 확장 애드온을 포함한 MATLAB을 완벽하게 대체할 수 있습니다.

SciPy는 NumPy위에서 구동되는 라이브러리 정도로 이해해도 무방합니다. SciPy는 기본적으로 NumPy의 ndarray를 기본 자료형으로 사용합니다. 일부 패키지는 중복되지만 SciPy가 보다 풍부한 기능을 제공합니다. SciPy는 다른 과학 컴퓨팅 영역을 다루는 하위 패키지로 구성됩니다.

| scipy.cluster | Vector quantization / Kmeans |
| :--- | :--- |
| scipy.constants | Physical and mathematical constants |
| scipy.fftpack | Fourier transform |
| scipy.integrate | Integration routines 수치적분 루틴과 미분방정식 해법기 |
| [scipy.interpolate](https://docs.scipy.org/doc/scipy/reference/interpolate.html#module-scipy.interpolate) | Interpolation |
| [scipy.io](https://docs.scipy.org/doc/scipy/reference/io.html#module-scipy.io) | Data input and output |
| [scipy.linalg](https://docs.scipy.org/doc/scipy/reference/linalg.html#module-scipy.linalg) | numpy.linalg에서 제공하는 것보다 더 확장된 선형대수 루틴과 매트릭스 분해 |
| [scipy.ndimage](https://docs.scipy.org/doc/scipy/reference/ndimage.html#module-scipy.ndimage) | n-dimensional image package |
| [scipy.odr](https://docs.scipy.org/doc/scipy/reference/odr.html#module-scipy.odr) | Orthogonal distance regression |
| [scipy.optimize](https://docs.scipy.org/doc/scipy/reference/optimize.html#module-scipy.optimize) | 함수 최적화기와 방정식의 근을 구하는 알고리즘 |
| [scipy.signal](https://docs.scipy.org/doc/scipy/reference/signal.html#module-scipy.signal) | 시그널 프로세싱 도구 |
| [scipy.sparse](https://docs.scipy.org/doc/scipy/reference/sparse.html#module-scipy.sparse) | 희소 행렬과 희소 선형 시스템 풀이법 |
| [scipy.spatial](https://docs.scipy.org/doc/scipy/reference/spatial.html#module-scipy.spatial) | Spatial data structures and algorithms |
| [scipy.special](https://docs.scipy.org/doc/scipy/reference/special.html#module-scipy.special) | 감마 함수처럼 흔히 사용되는 수학 함수를 |
| [scipy.stats](https://docs.scipy.org/doc/scipy/reference/stats.html#module-scipy.stats) | 표준 연속/이산 확률 분포와 다양한 통계 테스트 |

SciPy에서 사용하는 기본 데이터 구조는 NumPy 모듈에서 제공하는 다차원 배열입니다. NumPy는 선형 대수학, 퓨리에 변환 및 난수 생성을 위한 몇 가지 기능을 제공하지만 SciPy에서 이와 동등한 기능을 제공하지는 않습니다.

기본적으로 모든 NumPy 함수는 SciPy 네임 스페이스를 통해 사용할 수 있습니다. SciPy를 가져올 때 NumPy 함수를 명시적으로 가져올 필요가 없습니다.

SciPy를 이해하기 위해서는 방대한 수학적 지식이 필요합니다. 여기에서 어렵고 복잡한 수학 이론은 저도잘 모르고 코드에 대한 이해를 위주로  몇 가지 예제를 돌려보겠습니다.

