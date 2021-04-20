# 2\)    conda에서 파이썬 가상 환경 \(virtual environments\) 생성하기

  
가상환경\(virtualenv\)은 여러 개의 파이썬 프로젝트가 하나의 컴퓨터에서 충동을 일으키지 않고 존재할 수 있도록 해줍니다. virtualenv는 각 프로그램별로 완전히 독립적인 가상의 환경을 만들어서 각 프로그램별로 라이브러리 모듈등의 버전을 별도로 지정할 수 있게 합니다. 즉 한 컴퓨터에 여러 개발환경을 서로 독립적으로 설치, 실행할 수 있게 해줍니다.

왜 가상 환경을 만들어서 작업을 진행할까?  한마디로 요약하자면 "독립적인 작업환경에서 작업할 수 있다." 로 말할 수 있습니다.

프로젝트를 진행하다보면 여러 라이브러리, 패키지를 다운로드하여서 사용하게 됩니다. 그러다 보면 각 라이브러리들끼리 충돌을 일으키는 문제를 발생시키는 경우가 있습니다. 또는, 특정 버전과 호환하는 경우가 생겨서 최신 버전과 이전 버전 중 선택해야 하는 상황이 발생됩니다. 가상환경은 각 프로그램별로 라이브러리 모듈 등의 버전을 별도로 지정할 수 있게 합니다. 즉 한 컴퓨터에 여러 개발환경을 서로 독립적으로 설치, 실행할 수 있게 해줍니다.



다음 명령어를 통해 가상환경이 만들어 집니다.

```text
>conda create -n <환경명> python=<버전(ex:3.5이나 3.7 등)>
```

본 교재의 모든 예제들은 다음과 같은 명령으로 만들어 실행하도록 합니다. 본인 스스로 가상 환경을 관리할 수 있다면 다른 이름을 사용해도 관계없습니다.

```text
>conda create -n koreait python=3.7
```

-       koreait 은 가상환경 이름을 의미합니다.

-       python=3.7 는 파이썬 3.7 환경으로 가상환경을 만들어라 하는 것 입니다. 다른 패키지들과의 호환성을 위해 본 교재는 파이썬 3.7를 사용합니다.

-       numpy ~ statsmodels : 사용해야 할 라이브러리들을 지정할 수 있습니다. 필요시 pip install 을 사용하여 개별적으로 설치 할 수도 있습니다.

위의 명령을 실행하면 "c:\users\사용자계정\anaconda3\env\koreait" 라는 디렉토리가 생성되면서 그 안에 필요한 것들을 설치하겠냐고 묻게 됩니다. 당연히 "y" 를 눌러서 설치를 합니다.

![](../../../.gitbook/assets/2111-4.png)

내가 제대로 환경을 만들었는지 다음 명령을 실행하여 확인합니다.

&gt;conda env list

내가 만든 환경이 리스트에 존재한다면 성공적으로 만들어 진 것입니다.

![](../../../.gitbook/assets/2111-5.png)

이후에 가상환경을 활성화하고 싶으면 activate 명령어로 해당 가상환경을 활성화합니다.

activate 가상환경명 혹은 conda activate 가상환경명

&gt;conda activate koreait

&gt;activate koreait

![](../../../.gitbook/assets/2111-6.png)

\(base\)표시가 \(koreait\) 으로 변경되었음을 볼 수 있습니다.

비활성화 시키고 싶으면 koreait 이 활성화되어 있는 상태에서

&gt;deactivate    혹은     &gt;conda deactivate

라고 해 주면 됩니다.

가상 환경을 제거하고 싶으면 아나콘다 터미널에서 \(base\)환경을 확인하고 다음을 입력한 후 실행하면 됩니다.

&gt;conda remove -n name --all

만들어진 koreait 환경을 제거하고 다시 설치하고 싶다면 다음 명령으로 가상환경을 제거하고 다시 만들어 주시면 됩니다.

\(base\)&gt;conda remove -n koreait --all

Anaconda Prompt에서 \(koreait \)이 표시되어 있다면 deactivate 를 입력하여 \(base\)환경으로 돌아옵니다.  \(base\) 환경에서 python --version 을 실행해 봅니다. 그리고 “conda activate koreait ” 명령으로 가상환경 \(koreait \)을 활성화시킨 후 python --version 을 실행해 봅니다. \(base\) 환경에서 파이썬 버전은 3.7.2 이고 \(koreait \) 환경에서 파이썬 버전은 3.5.6 이 적용됨을 확인할 수 있습니다.

![](../../../.gitbook/assets/2111-7.png)

가상환경 \(koreait \)에서 파이썬이 제대로 동작하는지 “Hello Workd” 예제를 사용하여 확인해 보자.

Anaconda Prompt에서 \(koreait \) 환경에서 “python”을 입력합니다.

&gt;&gt;&gt; 표시가 나타나면 print\(“Hello World”\) 를 입력하고 엔터를 누릅니다.

![](../../../.gitbook/assets/2111-8.png)

“Hello World”가 화면에 제대로 출력이 된다면 Ctrl+C 혹은 Ctrl+D 혹은 Ctrl+Z 를 눌러 빠져나오면 됩니다.

* 가상환경 만들기 conda create –n 가상환경이름 python=3.7 
* 가상환경 활성화 conda activate 가상환경이름 
* 가상환경 비활성화 conda deactivate 가상환경이름 
* 가상환경에 패키지 설치 conda install 패키지이름 
* 가상환경 리스트 확인 conda env list 
* 가상환경 삭제 conda env remove -n 가상환경이름

