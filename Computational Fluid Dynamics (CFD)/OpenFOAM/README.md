# OpenFOAM ���ü�¼���������

[OpenFOAM ����](https://www.openfoam.com)
[OpenFOAM �ٷ�api�ĵ�](https://api.openfoam.com/2306/)
[���Ľ�����̳��CFD��������](https://cfd-china.com/category/6/openfoam)

# :apple: macOS
Canjia Huang 24/2/2025 <<canjia7@gmail.com>>
- ����ƽ̨��MacBook Air (Apple M3) - macOS 15.3
- OpenFOAM �汾��OpenFOAM-v2412

## ��װ����
���ﰲװ���� [openfoam-app](https://github.com/gerlero/openfoam-app) ����2�ְ�װ��ʽ��

### 1. ֱ��ʹ�� homebrew ��װ
:bangbang: ���ְ�װ��ʽ�ǳ����㣬���ǰ�װ�� **OpenFOAM** ���λ����λ�ڹ��ش����еģ�ʹ���ն�ִ�в�������Ӱ�죬����Ҫ�Լ������������ʱ���޷��ٱ��벢д�루ͨ���ı���ش��̵Ķ�дȨ�޿��ܿ��Խ����
���� [openfoam-app](https://github.com/gerlero/openfoam-app) �� [README](https://github.com/gerlero/openfoam-app/blob/main/README.md) �еĲ�����а�װ���ɣ�
1. ��װ **Homebrew**
2. �ն������룺
    `brew install --no-quarantine gerlero/openfoam/openfoam`

��װ��ɺ�������̨�л���һ��Ӧ�ó��� **OpenFOAM-v2412.app**����������ȡ���ڰ�װ�汾��������Դ˰汾Ϊ����

### 2. ����Դ����밲װ��:+1: �Ƽ���
�� [openfoam-app](https://github.com/gerlero/openfoam-app) �� [README Building from source](https://github.com/gerlero/openfoam-app/blob/main/README.md#-building-from-source) ��Ҳ���ᵽ�ð�װ��ʽ��
1. ��װ [**pixi**](https://pixi.sh/latest/)���Ƽ��� **Homebrew** ��װ�����Ȱ�װ **Homebrew**�������ն������룺
   `brew install pixi`
   ͬʱ���ܻ���Ҫ��װ **Xcode Command Line Tools**�����ҿ���֮ǰ��װ�����Բ�����Ҫ
2. �� **openfoam-app** �ֿ�git clone�����أ����ն����룺
    `git clone https://github.com/gerlero/openfoam-app.git`
3. ���� **openfoam-app** Ŀ¼�����룺
   `pixi run make`

��ɱ������ openfoam-app/build �л���һ��Ӧ�ó��� **OpenFOAM-v2412.app**����Ӧ����ʹ�� **Homebrew** ��װ���ƣ����λ��Ҳ�����ڴ��̣�
ͬʱ�� openfoam-app/build �»����һ�������ļ� **OpenFOAM-v2412-build.sparsebundle**���򿪺����ؿ�Ĵ��̣�����Ѿ������Ŵ��̣���Ҫ�Ƚ������ŵĴ����Ƴ�����:floppy_disk: ��ʱ���صĴ����ǿɱ༭��д���
   - ���ͨ���� **OpenFOAM-v2412-build.sparsebundle** �����ش��̵�����£�����ͨ���򿪹����ŵĴ����еĽű� **openfoam** �����նˣ��ýű���·��Ϊ��/Volumes/OpenFOAM-v2412/etc/**openfoam**��

���ֻ��Ҫ���� **OpenFOAM-v2412-build.sparsebundle** ������Ҫ���� **OpenFOAM-v2412.app**�����Խ���3���еı��������Ϊִ�У�
`pixi run make build`

### Paraview ��װ��:bulb: ��ѡ��
OpenFOAM ����ͨ�� paraFoam �ű����������ӻ���� [paraview](https://www.paraview.org) �Կ��ӻ������ͬ������ʹ�� **Homebrew** ��װ������ [brew/paraview](https://formulae.brew.sh/cask/paraview) �в�����а�װ���ɣ�
1. ��װ **Homebrew**
2. �ն������룺
   `brew install --cask paraview`

## ���Ų������նˣ�
ֱ������ **OpenFOAM-v2412.app**�����Ѿ����ش��̵���������������еĽű� etc/**openfoam**�������һ���ն˽��棬�����ڸ��ն˽�����ֱ��ʹ�� OpenFOAM �����ָ�
![](.pic/image1.png)
��
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
![](.pic/image2.png)

## ���Ų�����C++��
[](https://www.cfd-online.com/Forums/openfoam-programming-development/241735-how-develop-openfoam-cmake-popular-ides.html)
[openfoam-cmake-app](https://github.com/kvns/openfoam-cmake-app)