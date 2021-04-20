# 3\) NVIDIA GPU 환경 설정하기

사용하는 컴퓨터에 NVIDIA Graphic Card 를 장착되어 있다면 NVIDIA CUDA, cuDNN 을 사용하여 GPU 환경에서 좀더 빠르게 실습할수 있습니다.  

GPU 를 이용한 프로그래밍을 하는 방법은 NVIDIA 의 CUDA 라이브러리를 사용하는 것입니다. CUDA 를 이용하면 C, C++ 등의 언어로 GPU 프로그래밍을 할 수 있습니다. 또한 CUDA 보다 high-level API 로 cuBLAS, cuDNN 등 이 있습니다. high-level API 의 경우 CUDA 를 기반으로 행렬 연산, 딥러닝 등을 구현하는 것에 초점을 맞추어져 있기 때문에 이러한 작업들에 GPU 를 더욱 쉽게 이용할 수 있습니다.

CUDA를 설치하려면 먼저 내가 설치하고자 하는 tensorflow gpu와 호환되는 CUDA, cuDNN 버전을 확인해야 합니다. 호환되는 CUDA와 cuDNN 버전은 아래 링크에서 확인할 수 있습다.

[https://www.tensorflow.org/install/source\_windows\#tested\_build\_configurations](https://www.tensorflow.org/install/source_windows#tested_build_configurations)

2021년 1/4 분기인 현재 까지 cuDNN 은 7.6. cuda는 10.1 을 설치하면 무난합니다. NVIDIA 사이트의 CUDA Archive에서 원하는 버전의 CUDA를 선택해서 다운로드한후 설치한다.

•NVIDA CUDA Toolkit Archive 링크: [https://developer.nvidia.com/cuda-toolkit-archive](https://developer.nvidia.com/cuda-toolkit-archive)

그 다음 내 Tensorflow와 호환되면서 내 CUDA와도 호환되는 버전의 cuDNN을 다운로드하고 설치합니다. NVIDIA 회원가입을 해야 cuDNN을 다운로드할 수 있습니다.

•NVIDIA cuDNN Archive 링크: [https://developer.nvidia.com/rdp/cudnn-archive](https://developer.nvidia.com/rdp/cudnn-archive)

다운로드한 cuDNN 파일의 압축을 풀고 각각의 폴더에 해당하는 파일들을 C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v 버전의 폴더로 옮깁니다. 만약 CUDA 버전이 10.1이라면 옮길 경로는 C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v10.1이 됩니다. \(C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA에는 v버전명 폴더 하나만 있을 것이다. 그렇기 때문에 경로를 혼동할 일은 크게 없을 것 같다\)



