# OpenFOAM ���ü�¼���������

# :apple: macOS

Canjia Huang <<canjia7@gmail.com>> last update 25/2/2025

- ����ƽ̨��MacBook Air (Apple M3) - macOS 15.3
- OpenFOAM �汾��OpenFOAM-v2412

## :round_pushpin: ��װ

���ﰲװ���� [openfoam-app](https://github.com/gerlero/openfoam-app) ����2�ְ�װ��ʽ��

### 1. ֱ��ʹ�� homebrew ��װ

:bangbang: ���ְ�װ��ʽ�ǳ����㣬���ǰ�װ�� **OpenFOAM** ���λ����λ�ڹ��ش����еģ�ʹ���ն�ִ�в�������Ӱ�죬����Ҫ�Լ������������ʱ���޷��ٱ��벢д�루ͨ���ı���ش��̵Ķ�дȨ�޿��ܿ��Խ����

���� [openfoam-app](https://github.com/gerlero/openfoam-app) �� [README](https://github.com/gerlero/openfoam-app/blob/main/README.md) �еĲ�����а�װ���ɣ�

1. ��װ **Homebrew**
2. �ն������룺
    `brew install --no-quarantine gerlero/openfoam/openfoam`

��װ��ɺ�������̨�л���һ��Ӧ�ó��� **OpenFOAM-v2412.app**����������ȡ���ڰ�װ�汾��������Դ˰汾Ϊ����

### 2. ����Դ����밲װ�� :+1: �Ƽ���

�� [openfoam-app](https://github.com/gerlero/openfoam-app) �� [README Building from source](https://github.com/gerlero/openfoam-app/blob/main/README.md#-building-from-source) ��Ҳ���ᵽ�ð�װ��ʽ��

1. ��װ [**pixi**](https://pixi.sh/latest/)���Ƽ��� **Homebrew** ��װ�����Ȱ�װ **Homebrew**�������ն������룺
   `brew install pixi`
   
   ͬʱ���ܻ���Ҫ��װ **Xcode Command Line Tools**�����ҿ���֮ǰ��װ�����Բ�����Ҫ
2. �� **openfoam-app** �ֿ�git clone�����أ����ն����룺
    `git clone https://github.com/gerlero/openfoam-app.git`
3. ���� **openfoam-app** Ŀ¼�����룺
   `pixi run make`

��ɱ������ openfoam-app/build �л���һ��Ӧ�ó��� **OpenFOAM-v2412.app**����Ӧ����ʹ�� **Homebrew** ��װ���ƣ����λ��Ҳ�����ڴ��̣�

ͬʱ�� openfoam-app/build �»����һ�������ļ� **OpenFOAM-v2412-build.sparsebundle**���򿪺����ؿ�Ĵ��̣�����Ѿ������Ŵ��̣���Ҫ�Ƚ������ŵĴ����Ƴ����� :floppy_disk: ��ʱ���صĴ����ǿɱ༭��д���

   - ���ͨ���� **OpenFOAM-v2412-build.sparsebundle** �����ش��̵�����£�����ͨ���򿪹����ŵĴ����еĽű� **openfoam** �����նˣ��ýű���·��Ϊ��/Volumes/OpenFOAM-v2412/etc/**openfoam**��;���߽� **OpenFOAM** ��صĻ���������ӵ�ϵͳ��������ز��������� *���Ų�����wmake�����������*�����������ն���ֱ��ִ��

���ֻ��Ҫ���� **OpenFOAM-v2412-build.sparsebundle** ������Ҫ���� **OpenFOAM-v2412.app**�����Խ���3���еı��������Ϊִ�У�`pixi run make build`

### Paraview ��װ�� :bulb: ��ѡ��

OpenFOAM ����ͨ�� paraFoam �ű����������ӻ���� [paraview](https://www.paraview.org) �Կ��ӻ������ͬ������ʹ�� **Homebrew** ��װ������ [brew/paraview](https://formulae.brew.sh/cask/paraview) �в�����а�װ���ɣ�

1. ��װ **Homebrew**
2. �ն������룺
   `brew install --cask paraview`

## :round_pushpin: ���Ų������նˣ�

ֱ������ **OpenFOAM-v2412.app**�����Ѿ����ش��̵���������������еĽű� etc/**openfoam**�������һ���ն˽��棬�����ڸ��ն˽�����ֱ��ʹ�� OpenFOAM �����ָ�

![image1](.pic/image1.png)

����������ͨ�����尸������һ�£����Բο�[��������ĵ�-Examples](https://doc.openfoam.com/2312/examples/)

�� **OpenFOAM-v2412.app** ������һ������ **OpenFOAM-v2412**���ô����� tutorials Ŀ¼�´����һЩ���԰���

������� /Volumes/OpenFOAM-v2412/tutorials/incompressible/pisoFoam/RAS/cavity �µ�����

 - OpenFOAM�ǽ�<u>Ҫ������������</u>�Լ�<u>������Ĳ���</u>���洢���ļ����еĸ����ļ��У�������Բο�[��������ĵ�-Quickstart](https://doc.openfoam.com/2312/quickstart/)�������Ҫ�г��ð������ļ��ṹ��
    ```
    cavity
        - 0.orig/ ��������0ʱ�̵ĳ�ʼ/�߽�������
        - constant/ ������������ģ����ʹ�õ��ļ��κ��������ʵĳ�����
        - system/ �����������������ģ�⹤�ߵȵ����ã�
        - Allclean ���ű���
        - Allrun ���ű���
        - Allrun-parallel ���ű���
    ```

:bangbang: ��Ҫע����ǣ��������ͨ���� **OpenFOAM-v2412.app** �������ն˵ģ���ʱ���صĴ���û�ж�дȨ�ޣ���ᵼ��ִ�������������ɵĽ���ļ��޷��洢�����ܿ���ͨ���ı���̵�Ȩ��������������Կ����Ƚ��ð����ļ��и��Ƶ�����·�����ҽ��и��ƺ�Ĳ��԰����ļ���·��Ϊ��/Users/canjia/CFD/cavity

���ڸð����Ѿ����� **Allrun** �ű�������ͨ��ִ�иýű���������������Ĳ��ԣ�һ���Լ��İ�������Ҫ�ֶ��ּ�����������ɣ����Լ���д **Allrun** �ű���

�� **OpenFOAM-v2412.app** �򿪵��ն������룺

```
cd /Users/canjia/CFD/cavity
./Allrun
```

�ɹ�ִ�к���� /Users/canjia/CFD/cavity Ŀ¼����������������ص��ļ�

����Ѿ���װ�� **paraview**�����ԶԽ�����п��ӻ�����ʱ������ **OpenFOAM-v2412.app** �򿪵��ն������룺

```
paraFoam
```

���Զ��� **Paraview**�����ӻ�������£�

![image2](.pic/image2.png)

���Ե�� **Paraview** �����Ϸ��Ĳ��ż������ӻ�ģ�����

## :round_pushpin: ���Ų�����wmake�����������

**wmake** �� **OpenFOAM** ��ʹ�õĹ������ߣ�ר�����ڱ�������� **OpenFOAM** ��Դ���뼰����ص�Ӧ�ó���Ϳ⣬�������ڱ����Զ��������

Ϊʹ�� **wmake**��������Ҫ�� **OpenFOAM** ��صĻ���������ӽ�ϵͳ����

ʹ�� bash shell����ֱ�������������д򿪵� **OpenFOAM** �ն��У���source ���ش����е� etc/**bashrc** �ļ�������·������ʵ�����ȷ������

```
cd /Volumes/OpenFOAM-v2412/etc
source bashrc
```

ִ�к�������ն������� `echo $WM_PROJECT_DIR` ������Ƿ�ɹ������˻�������

Ϊ���ں���������Ҳ������û������������Խ���������д�� ~/**.bashrc** �� ��/**.zshrc** �ļ���

�Ա�ƽ̨Ϊ������ ��/**.zshrc** �ļ������ļ�Ϊ�����ļ�������ͨ���ն˴򿪻��� **Finder** ��ʹ�ÿ�ݼ� `command + shift + .` ������/�ر���ʾ�����ļ��������ļ����������ϣ�����·������ʵ�����ȷ������

```
. /Volumes/OpenFOAM-v2412/etc/bashrc
```

�����ն�����������ϵͳ����������

```
source ~/.zshrc
```

ͬ������ͨ�� `echo` ����������Լ�黷�������Ƿ�ɹ�����

:sweat: ��Ҫע����ǣ����������ı�����������ϵͳ��������ʱ���� . /Volumes/OpenFOAM-v2412/etc/**bashrc**�����������û���� **OpenFOAM** ���̵�����£����޷�ʹ�� source ���뻷��������

   - ����ζ���������������Ժ�����Ҫ���¹����ϴ��̲�����ִ��һ�� `source ~/.zshrc` ָ�������Գ��Խ����ش����еĻ��������ļ������ڱ�������Ŀ¼...��
   - ��������ں���������ʼ���޷���û��������Ļ���������������...

:star: ������ͨ��һ��������ʹ�� **wmake** �������������ʹ�ø��������ⰸ�����ð���Դ�� [BasicOpenFOAMProgrammingTutorials](https://github.com/UnnamedMoose/BasicOpenFOAMProgrammingTutorials/tree/master) �� **OFtutorial13_waveEquationSolver**�����ð���ʹ�õ� **OpenFOAM** �汾���ϣ�ʹ�� **wmake** ���������ʱ����������ҽ��ð����������ʺϱ��ĵ�ʹ�õ� **OpenFOAM** �汾������������ڱ��ĵ�Ŀ¼�� [OFtutorial13_waveEquationSolver](OFtutorial13_waveEquationSolver)

:bangbang: ��Ҫע����ǣ��ڽ��б����ʱ����Ҫʼ�ձ��� **OpenFOAM** ���̹����ŵ�״̬��������Ҳ������·��

### ���� 1�����ذ���

�����ĵ�Ŀ¼�µ� [OFtutorial13_waveEquationSolver](OFtutorial13_waveEquationSolver) ����������Ŀ¼������ʾ����Ŀ¼Ϊ��/Users/canjia/CFD/OFtutorial13_waveEquationSolver�������ն��н����Ŀ¼��

```
cd /Users/canjia/CFD/OFtutorial13_waveEquationSolver
```

### ���� 2��wmake���������

**wmake** ��ͨ��ʹ�ø�Ŀ¼�µ� **Make** �ļ����е� **file** �� **options** �ļ������������������λ�ú�ѡ��

ʹ���ı��鿴���� **files** �ļ����Կ������õ����������λ�ã�`EXE = $(FOAM_USER_APPBIN)/ofTutorial13`���������ն���ʹ�� `echo $FOAM_USER_APPBIN` ָ�����鿴�����·��

������ִ�и�Ŀ¼�µ� **Allwmake** �ű�����ֱ��ִ�� `wmake` ָ���

```
./Allwmake
```

�ýű���������Ŀ¼ `EXE = $(FOAM_USER_APPBIN)` ����������� **ofTutorial13** �ű�

���Զ������ **ofTutorial13** ʹ�� `-help` ָ������ȡ������Ϣ�����ն������룺

```
$FOAM_USER_APPBIN/ofTutorial13 -help
```

### ���� 3��OpenFOAM�����������

����������ð����е� **testCase** �ļ��У���ִ�����е� **Allrun** �ű�����ģ���õ�����

```
cd /Users/canjia/CFD/OFtutorial13_waveEquationSolver/testCase
./Allrun
```

�ű�������ɺ���� **testCase** �ļ����������ļ� **log.blockMesh** �� **log.setFields**

��ʱ����ʹ�� `paraFoam` ���� **Paraview** �Կ��ӻ������񣬵����ڻ�û����ģ�⣬���Ը������޷��鿴ģ�⶯��

### ���� 4��ʹ���Ա������������ģ��

������ʹ�ò��� 2�б����������Ը��������ģ�⣬���ն�������

```
$FOAM_USER_APPBIN/ofTutorial13 -case /Users/canjia/CFD/OFtutorial13_waveEquationSolver/testCase
```

ģ����̻��� **testCase** �ļ��������ɽ����ص��ļ�������ʹ�� **Paraview** ��ģ����̽��п��ӻ����� **testCase** �ļ��������ն���ִ�У�

```
paraFoam
```

���ӻ��������£�

![image3](.pic/image3.png)

������ **Paraview** ���Ͻǵ������ӻ������ݣ�Ĭ���� **Solid Color**������Ϊ��Ҫ���ӻ��ı������� **h**��Ȼ��ʹ���Ϸ��Ĳ��ż��Բ���ģ�����

## :round_pushpin: ���Ų�����CMake��

����ʹ�� **CMake** ����������ʹ�� **OpenFOAM** �� C++ ��Ŀ�������������

- IDE��CLion 2024.3.2

����ͬ���Ա��ĵ�Ŀ¼�µ� [OFtutorial13_waveEquationSolver](OFtutorial13_waveEquationSolver) ����Ϊ��

### ���� 1�����ذ���

�����ĵ�Ŀ¼�µ� [OFtutorial13_waveEquationSolver](OFtutorial13_waveEquationSolver) ����������Ŀ¼������ʾ����Ŀ¼Ϊ��/Users/canjia/CFD/

### ���� 2����дCMakeLists

�ڸð���Ŀ¼�ĸ�Ŀ¼���½� **CMakeLists.txt**����������д�루�ο���[��OpenFOAM����VS Code����OpenFOAM](https://blog.csdn.net/weixin_43940314/article/details/123771467)����

```
cmake_minimum_required(VERSION 3.21)

if (DEFINED ENV{WM_PROJECT})
    message("Using $ENV{WM_PROJECT}-$ENV{WM_PROJECT_VERSION}")
    set(WM_PATH, ${CMAKE_SOURCE_DIR})
else()
    message(FATAL_ERROR "OpenFOAM environment not set. Aborting.")
endif ()

project(OFtutorial13)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
set(OpenFOAM_VERSION $ENV{WM_PROJECT_VERSION})
set(OpenFOAM_DIR $ENV{WM_PROJECT_DIR})
set(OpenFOAM_LIB_DIR $ENV{FOAM_LIBBIN})
set(OpenFOAM_SRC $ENV{FOAM_SRC})

set(DEFINITIONS_COMPILE *******)

add_definitions("${DEFINITIONS_COMPILE}")

include_directories(
        ${OpenFOAM_SRC}/finiteVolume/lnInclude
        ${OpenFOAM_SRC}/meshTools/lnInclude
        lnInclude
        .
        ${OpenFOAM_SRC}/OpenFOAM/lnInclude
        ${OpenFOAM_SRC}/OSspecific/POSIX/lnInclude
)

link_directories(${OpenFOAM_LIB_DIR} ${OpenFOAM_LIB_DIR}/dummy ${OpenFOAM_LIB_DIR}/${PATH_LIB_OPENMPI})

add_executable(${PROJECT_NAME} ofTutorial13.C)

target_link_libraries(${PROJECT_NAME} OpenFOAM dl m Pstream finiteVolume fvOptions meshTools )
```

:bangbang: ������Ҫע����ǵ�20�� `set(DEFINITIONS_COMPILE *******)` ������ǺŴ����룬��һ�����ᵽ

### ���� 3����ȡ DEFINITIONS_COMPILE

���� **wmake** ��������һ�������ն��н��밸������Ŀ¼����ִ��`wmake`��

```
cd /Users/canjia/CFD/OFtutorial13_waveEquationSolver
./Allwmake
```

ִ�к��ʹ�� **wmake** �԰�����������б��룬�������Ľ��������Ҫ��Ŀ�Ľ���Ϊ�˸����ն˵���������ȷ�� **DEFINITIONS_COMPILE** ��ֵ

ִ������ָ������ն��л�������������ݿ��ܸ���ƽ̨��ͬ���в��죩��

```
Making dependencies: ofTutorial13.C
clang++ -std=c++17 -m64 -pthread -ftrapping-math -ffp-contract=off -DOPENFOAM=2412 -DWM_DP -DWM_LABEL_SIZE=32 -Wall -Wextra -Wold-style-cast -Wnon-virtual-dtor -Wno-unused-parameter -Wno-invalid-offsetof -Wno-undefined-var-template -Wno-unknown-warning-option -O3  -DNoRepository -ftemplate-depth-100 -I/Volumes/OpenFOAM-v2412/env/include  -I/Volumes/OpenFOAM-v2412/src/finiteVolume/lnInclude -I/Volumes/OpenFOAM-v2412/src/meshTools/lnInclude -iquote. -IlnInclude -I/Volumes/OpenFOAM-v2412/src/OpenFOAM/lnInclude -I/Volumes/OpenFOAM-v2412/src/OSspecific/POSIX/lnInclude   -fPIC -c ofTutorial13.C -o Make/darwin64ClangDPInt32Opt/ofTutorial13.o
clang++ -std=c++17 -m64 -pthread -ftrapping-math -ffp-contract=off -DOPENFOAM=2412 -DWM_DP -DWM_LABEL_SIZE=32 -Wall -Wextra -Wold-style-cast -Wnon-virtual-dtor -Wno-unused-parameter -Wno-invalid-offsetof -Wno-undefined-var-template -Wno-unknown-warning-option -O3  -DNoRepository -ftemplate-depth-100 -I/Volumes/OpenFOAM-v2412/env/include  -I/Volumes/OpenFOAM-v2412/src/finiteVolume/lnInclude -I/Volumes/OpenFOAM-v2412/src/meshTools/lnInclude -iquote. -IlnInclude -I/Volumes/OpenFOAM-v2412/src/OpenFOAM/lnInclude -I/Volumes/OpenFOAM-v2412/src/OSspecific/POSIX/lnInclude   -fPIC  -rpath @executable_path/../lib/openmpi -rpath @executable_path/../lib -rpath @executable_path/../lib/dummy -rpath @executable_path/../lib/../../../env/lib -Wl,-execute,-undefined,dynamic_lookup -L/Volumes/OpenFOAM-v2412/env/lib  Make/darwin64ClangDPInt32Opt/ofTutorial13.o -L/Volumes/OpenFOAM-v2412/platforms/darwin64ClangDPInt32Opt/lib \
	    -lfiniteVolume -lmeshTools -lOpenFOAM -ldl  \
	     -lm -o /Users/canjia/OpenFOAM/canjia-v2412/platforms/darwin64ClangDPInt32Opt/bin/ofTutorial13
```

��������������е� `-std=c++17 -m64 -pthread -ftrapping-math -ffp-contract=off -DOPENFOAM=2412 -DWM_DP -DWM_LABEL_SIZE=32 -Wall -Wextra -Wold-style-cast -Wnon-virtual-dtor -Wno-unused-parameter -Wno-invalid-offsetof -Wno-undefined-var-template -Wno-unknown-warning-option -O3  -DNoRepository -ftemplate-depth-100 -I/Volumes/OpenFOAM-v2412/env/include  -I/Volumes/OpenFOAM-v2412/src/finiteVolume/lnInclude -I/Volumes/OpenFOAM-v2412/src/meshTools/lnInclude -iquote. -IlnInclude -I/Volumes/OpenFOAM-v2412/src/OpenFOAM/lnInclude -I/Volumes/OpenFOAM-v2412/src/OSspecific/POSIX/lnInclude   -fPIC` ���� **DEFINITIONS_COMPILE** ӦΪ��ֵ

����ֵ�滻�� **CMakeLists.txt** �� `set(DEFINITIONS_COMPILE *******)` ���ǺŴ�

### ���� 4��CMake���ɲ�ִ��

���������ݳ��õ� **CMake** ��Ŀ���ɷ�ʽ���ɼ��ɣ�

```
mkdir build
cd build
cmake ..
make
```

�����ͻ��� build Ŀ¼��������Ӧ������� **OFtutorial13**���������԰����Ĳ���ͬ :round_pushpin: **���Ų�����wmake�����������**���������Ŀ¼�б仯��

### Some Tips

- ���ʹ�� **CLion** IDE �Ļ������뻷�������������� IDE��������������޷����������Ҳ���Գ���һ������ IDE ��ϵͳ
- **OpenFOAM** ��ص�ͷ�ļ����ĺ�׺���Ǵ�д����ĸ�� ".H"��д��Сд�Ŀ��ܻ��Ҳ����ļ����������ƿ��Ե���ӦĿ¼����ȷ��

# Some Resources

- [OpenFOAM ����](https://www.openfoam.com)
- [OpenFOAM �ٷ�api�ĵ�](https://api.openfoam.com/2306/)
- [OpenFOAM v12 User Guide](https://doc.cfd.direct/openfoam/user-guide-v12/index) - [Tutorials](https://doc.cfd.direct/openfoam/user-guide-v12/tutorials)
- [BasicOpenFOAMProgrammingTutorials](https://github.com/UnnamedMoose/BasicOpenFOAMProgrammingTutorials/tree/master) - Introduces basic C++ concepts to beginner users of the OpenFOAM open-source CFD libraries.
   - ����Ŀ������ʹ�õ� **OpenFOAM** �汾���ϣ�����ʱ���ܻ������汾���µ��µĲ����ݴ��� 
- [���Ľ�����̳��CFD��������](https://cfd-china.com/category/6/openfoam)
- [DYFLUID OpenFOAM �����/�̳�/����/����](http://www.dyfluid.com/solvers.html)