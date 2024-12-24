# isaac_lab
## Getting Started(Windows)
**1. conda 가상환경 설정**

[anaconda 링크](https://www.anaconda.com/download)

anaconda 설치 후 anaconda prompt에 아래 코드 차례로 입력

```
    conda create -n isaac_lab python=3.10
    conda activate isaac_lab
```

**2. cuda 12.4 버전 설치**

[cuda 링크](https://developer.nvidia.com/cuda-12-4-0-download-archive?target_os=Windows&target_arch=x86_64&target_version=11&target_type=exe_local)

아래 코드로 설치 되었는지 확인
```
nvcc --version
```

**3. Pytorch cuda12.4 버전 맞춰 설치**

[Pytorch 링크](https://pytorch.org/)

**4. pip 최신버전 업그레이드**
```
pip install --upgrade pip
```

**5. Isaac Sim 다운로드**
```
pip install isaacsim==4.2.0.2 isaacsim-extscache-physics==4.2.0.2 isaacsim-extscache-kit==4.2.0.2 isaacsim-extscache-kit-sdk==4.2.0.2 --extra-index-url https://pypi.nvidia.com
```

**6. Isaac Sim 설치 확인**
```
isaacsim
```
Do you accept the EULA?->Yes
위 코드 입력하면 아래와 같은 창이 뜨면 제대로 설치된 것.
![image1](docs\source\_static\verify_isaacsim_window.jpg)

**7. Isacc Lab 다운로드**
isaac_lab환경 선택한 vscode에 Isaac Lab 클론 - [Isaac Lab 링크](https://github.com/isaac-sim/IsaacLab/tree/main)

vscode command prompt에 아래 코드 입력해 설치
```
isaaclab.bat -i
isaaclab.bat -i rl_games
#특정 프레임워크 선택하여 설치가능 위 코드는 모든 프레임워크 설치
#rl_games, rsl_rl, sb3, skrl, robomimic, none 옵션있음
```

**8. Isaac Lab 설치 확인**
아래 코드 실행 시 아래 사진처럼 나오면 설치 완료!
```
#bat파일 실행가능한 경우
isaaclab.bat -p source\standalone\tutorials\00_sim\spawn_prims.py

#파이썬 가상환경에서
python source\standalone\tutorials\00_sim\spawn_prims.py
```
![image2](docs\source\_static\verify_isaaclab_window.jpg)