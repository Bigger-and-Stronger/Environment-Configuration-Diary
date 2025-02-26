# CGNS �����ü�¼

# :apple: macOS

Canjia Huang <<canjia7@gmail.com>> last update 26/2/2025

- ����ƽ̨��MacBook Air (Apple M3) - macOS 15.3

## ��װ����

1. ���Ȱ�װ **HDF5**���Ƽ�ʹ�� **Homebrew** ��װ�����ն������룺
   
   ```
   brew install hdf5
   ```
   
   ��װ��ɺ�������ն���ʹ��ָ�� `brew list hdf5` ���鿴 **HDF5** �İ�װ·�����ҵ�λ��Ϊ��/opt/homebrew/Cellar/hdf5/1.14.6 ������λ���Ӿ�����������ĵ��Դ�Ϊ����

2. �� [CGNS](https://github.com/CGNS/CGNS) �� clone �����أ����ն������룺
   
   ```
   git clone https://github.com/CGNS/CGNS.git
   ```

3. ���ն��н��� clone �� **CGNS** ��·�������ݳ��� **CMake** ��Ŀ�������� configuration��

    ```
    cd /Users/canjia/CGNS
    mkdir build
    cd build
    cmake .. -DCMAKE_PREFIX_PATH=******
    ```

    :warning: ע�⣬����� `cmake .. -DCMAKE_PREFIX_PATH=******` �е��Ǻ���Ҫ�滻Ϊ��� **HDF5** ��װ·���������������滻Ϊ `cmake .. -DCMAKE_PREFIX_PATH=/opt/homebrew/Cellar/hdf5/1.14.6`

    Ȼ��������ն��н��б��룺

    ```
    make -j
    make install
    ```

    :no_entry_sign: ִ�� `make install` ʱ���ܻᱨ�� ��file cannot create directory: /usr/local/lib.  Maybe need administrative
  privileges.������Ϊִ�� `sudo make install` ���������뼴��

## �� CMake ��Ŀ��ʹ��

��Ҫ�� **CMakeLists.txt** ��������¸��Ӱ���Ŀ¼�Լ����ӿ⣺

```
include_directories("******/src")
include_directories("******/build/src")

...

target_link_libraries(${PROJECT_NAME} "******/build/src/libcgns.dylib")
```

:warning: ע�⣬����������Ǻű�ע�ĵط���Ҫ�滻Ϊ������װ������ **CGNS** ������·�������������ｫ�Ǻ��滻Ϊ `/Users/canjia/CGNS`

## Some Resources

- [Some CGNS examples](https://cgns.github.io/current/examples.html)