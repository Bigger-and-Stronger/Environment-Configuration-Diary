# OpenFOAM ���ü�¼���������

[OpenFOAM ����](https://www.openfoam.com)
[���Ľ�����̳��CFD��������](https://cfd-china.com/category/6/openfoam)

## macOS
Canjia Huang 23/2/2025 <<canjia7@gmail.com>>
- ����ƽ̨��MacBook Air (Apple M3) - macOS 15.3
- OpenFOAM �汾��OpenFOAM-v2412

### ��װ����
���ﰲװʹ�õ��� [openfoam-app](https://github.com/gerlero/openfoam-app) ��������README�еĲ�����а�װ���ɣ�
1. ��װ **Homebrew**
2. �ն������룺
    `brew install --no-quarantine gerlero/openfoam/openfoam`
3. ������̨�д� **OpenFOAM-v2412.app** ����

����ѡ��openFOAM ����ͨ�� paraFoam �ű����������ӻ���� [paraview](https://www.paraview.org) �Կ��ӻ������ͬʱ���԰�װ������ [brew/paraview](https://formulae.brew.sh/cask/paraview) �в�����а�װ���ɣ�
1. ��װ **Homebrew**
2. �ն������룺
   `brew install --cask paraview`

### ���Ų������նˣ�
���� **OpenFOAM-v2412.app** �󣬻��һ���ն˽��棬�����ڸ��ն˽�����ʹ�� openFOAM �����ָ�
![](.pic/image1.png)

����������ͨ�����Ӳ���һ�£����Բο�[��������ĵ�-Examples](https://doc.openfoam.com/2312/examples/)
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

??��Ҫע����ǣ�����Ĭ�Ϲ��صĴ���û�ж�дȨ�ޣ���ᵼ��ִ�в��������ɵ��ļ��޷��洢������ͨ���ı���̵�Ȩ�������������û�б�Ҫ�������Կ����Ƚ��ð����ļ��и��Ƶ�����·�����ҽ��и��ƺ�Ĳ��԰����ļ���·��Ϊ��/Users/canjia/CFD/cavity
���ڸð����Ѿ����� **Allrun** �ű������Կ���ͨ��ִ�иýű���������������Ĳ��ԣ�һ���Լ��İ�������Ҫ�ֶ��ּ�����������ɣ����Լ���д **Allrun** �ű���
�� **OpenFOAM-v2412.app** �򿪵��ն������룺
```
cd /Users/canjia/CFD/cavity
./Allrun
```

�ɹ�ִ�к���� /Users/canjia/CFD/cavity Ŀ¼����������������ص��ļ�

����Ѿ���װ�� **paraview**�����ԶԽ�����п��ӻ��������� **OpenFOAM-v2412.app** �򿪵��ն������룺
```
paraFoam
```

���ӻ�������£�
![](.pic/image2.png)

### ���Ų�����C++��