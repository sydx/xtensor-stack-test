# xtensor-stack-test
A simple project to test the installation of xtensor-stack

Follow the following steps:

    conda create -n cleanenv
    conda activate cleanenv
    conda install --offline /c/Users/paul/conda-bld/win-64/xtensorstack-1.0.0-h2e52968_0.tar.bz2
    conda install clang
    conda install m2w64-gcc
    conda install m2w64-gcc-fortran
    conda install m2w64-make
    conda install m2-make
    conda install ninja
    conda install cmake
    cd ~/dev/xtensor-stack-test
    build.bat

You should see something like:

    C:\Users\paul\dev\xtensor-stack-test\build>cmake -G"Ninja" -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang ..
    -- The C compiler identification is Clang 14.0.6
    -- The CXX compiler identification is Clang 14.0.6
    -- Detecting C compiler ABI info
    -- Detecting C compiler ABI info - done
    -- Check for working C compiler: C:/Users/paul/.conda/envs/cleanenv/Library/bin/clang.exe - skipped
    -- Detecting C compile features
    -- Detecting C compile features - done
    -- Detecting CXX compiler ABI info
    -- Detecting CXX compiler ABI info - done
    -- Check for working CXX compiler: C:/Users/paul/.conda/envs/cleanenv/Library/bin/clang.exe - skipped
    -- Detecting CXX compile features
    -- Detecting CXX compile features - done
    -- Configuring done (5.2s)
    -- Generating done (0.0s)
    -- Build files have been written to: C:/Users/paul/dev/xtensor-stack-test/build

    C:\Users\paul\dev\xtensor-stack-test\build>ninja
    [1/2] Building CXX object CMakeFiles/tests.dir/tests.cpp.obj
    [2/2] Linking CXX executable tests.exe

Then:

    build/tests.exe
    Testing the xtensor-blas stack
    xtensor
    {  7.,  11.,  14.}
    xtensor-blas
    {{ 1.      ,  0.      },
     {-0.5     ,  1.322876}}

