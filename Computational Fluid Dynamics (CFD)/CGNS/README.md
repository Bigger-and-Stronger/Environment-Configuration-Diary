# CGNS �����ü�¼

# :apple: macOS

Canjia Huang <<canjia7@gmail.com>> last update 26/2/2025

[CFD General Notation System (CGNS) ����](https://cgns.github.io/index.html)

- ����ƽ̨��MacBook Air (Apple M3) - macOS 15.3

## ��װ����

��ϸ�������Ĳ�����Բο� [https://github.com/CGNS/CGNS](https://github.com/CGNS/CGNS) �� README������Ϊ�򵥿��еİ�װ���裺

1. ���Ȱ�װ **HDF5**���Ƽ�ʹ�� **Homebrew** ��װ�����ն������룺
   
   ```
   brew install hdf5
   ```
   
   ��װ��ɺ�������ն���ʹ��ָ�� `brew list hdf5` ���鿴 **HDF5** �İ�װ·�����ҵ�λ��Ϊ��/opt/homebrew/Cellar/hdf5/1.14.6 ��:warning: ����λ���Ӿ�����������ĵ��Դ�Ϊ����

2. �� [CGNS](https://github.com/CGNS/CGNS) �� clone �����أ����ն������룺
   
   ```
   git clone https://github.com/CGNS/CGNS.git
   ```

   ���ĵ����� clone ��·��Ϊ��/Users/canjia/CGNS���������Դ�·��Ϊ����:warning: ����·�����˶��죬������Ӧ�޸ģ�

3. ���ն��н��� clone �� **CGNS** ��·�������ݳ��� **CMake** ��Ŀ�������� configuration��

    ```
    cd /Users/canjia/CGNS
    mkdir build
    cd build
    cmake .. -DCMAKE_PREFIX_PATH=******
    ```

    :warning: ע�⣬����� `cmake .. -DCMAKE_PREFIX_PATH=******` �е��Ǻ���Ҫ�滻Ϊ��� **HDF5** ��װ·���������������滻Ϊ `cmake .. -DCMAKE_PREFIX_PATH=/opt/homebrew/Cellar/hdf5/1.14.6`

    Ȼ��������ն��н��б��밲װ��

    ```
    make -j
    make install
    ```

    :no_entry_sign: ִ�� `make install` ʱ���ܻᱨ�� ��file cannot create directory: /usr/local/lib.  Maybe need administrative
  privileges.������Ϊִ�� `sudo make install` Ȼ���������뼴��

## �� CMake ��Ŀ��ʹ��

��Ҫ�� **CMakeLists.txt** ��������¸��Ӱ���Ŀ¼�Լ����ӿ⣺

```
find_package(CGNS REQUIRED)
include_directories("${CGNS_ROOT}/src")
include_directories("${CGNS_ROOT}/build/src")

...

target_link_libraries(${PROJECT_NAME} "${CGNS_ROOT}/build/src/libcgns.dylib")
```

:bulb: ����ı��� **CGNS_ROOT** ��������ϵͳ���������ж���ģ������� `find_package(CGNS)` ���� **CGNS** �е� config.cmake ������ģ����Բ�����Ҫ��ǰ����

## Some Resources

- [Some CGNS examples](https://cgns.github.io/current/examples.html)