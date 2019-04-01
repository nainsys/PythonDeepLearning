# 1.6.5. 	싸이파이\(SciPy\)

  
SciPy\([https://www.scipy.org/scipylib](https://www.scipy.org/scipylib)\)는 과학 계산용 함수를 모아놓은 파이썬 패키지입니다. 

Numpy와 Scipy는 서로 떨어질 수 없을 정도로 밀접한 관계에 있으며 Scipy를 활용할 때에는 상당히 많이 Numpy를 이용하게 됩니다. 실제로 Scipy에 관한 책을 구매했을 때 책의 앞부분은 Scipy 관련 내용보다는 오히려 Numpy의 기초에 대한 내용 위주로 보게 되는 경우가 많습니다.

SciPy는 고성능 선형대수, 함수 최적화, 신호 처리, 특수한 수학 함수와 통계 분포 등을 포함한 많은 기능을 제공합니다. scikit-learn은 알고리즘을 구현할 때 SciPy의 여러 함수를 사용합니다. 그 중에서 가장 중요한 기능은 scipy.sparse입니다. 이 모듈은 scikit-learn에서 데이터를 표현하는 또 하나의 방법인 희소 행렬 기능을 제공합니다.

Scipy는 수치해석을 Numpy를 이용하여 보다 본격적으로 이용할 수 있게 해 줍니다. Scipy를 이용하면 Numpy만으로는 길게 코딩해야 하는 기법들을 단 2~3 줄에 구현할 수 있습니다. 게다가 Numpy로 구현하기 막막하거나 사실상 불가능한 것들도 Scipy로는 쉽게 결과를 얻을 수 있습니다. 따라서 Numpy와 Scipy를 적절하게 혼용하게 되면 더욱 생산성이 높습니다.

