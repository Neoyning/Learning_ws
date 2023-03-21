# Ceres Learning Note
 ---

## Ceres Setup

 - Download Ceres, [Ceres Download]. Current Ceres version 2.1.0
 - Install Ceres from source by cmake, [Ceres Make Install]
 - Using Ceres in CMake Projects [Cmake Ceres]
 
 > NOTE: `cmake -DCMAKE_INSTALL_PREFIX=/usr ..` or `cmake -DCMAKE_INSTALL_PREFIX=/usr/local ..`  (in build folder) for `sudo make install` install directory

Construct `AutoDiffCostFunction`, Fixed size example:
 
```sh
CostFunction* cost_function
    = new AutoDiffCostFunction<MyScalarCostFunctor, 1, 2, 2>(
        new MyScalarCostFunctor(1.0));              ^  ^  ^
                                                    |  |  |
                        Dimension of residual ------+  |  |
                        Dimension of x1 ---------------+  |
                        Dimension of x2 ------------------+
```
Construct `AutoDiffCostFunction`, Runtime-determined residuals size example:

```sh
CostFunction* cost_function
    = new AutoDiffCostFunction<MyScalarCostFunctor, DYNAMIC, 2, 2>(
        new CostFunctorWithDynamicNumResiduals(1.0),   ^     ^  ^
        runtime_number_of_residuals); <----+           |     |  |
                                           |           |     |  |
                                           |           |     |  |
          Actual number of residuals ------+           |     |  |
          Indicate dynamic number of residuals --------+     |  |
          Dimension of x1 -----------------------------------+  |
          Dimension of x2 --------------------------------------+
```

Check out

`usr/include/ceres/rotation.h`

`snavely_reprojection_error.h`

 [Ceres Download]:<https://ceres-solver.googlesource.com/ceres-solver/>
 [Ceres Make Install]:<http://ceres-solver.org/installation.html#linux>
 [Cmake Ceres]:<http://ceres-solver.org/installation.html#using-ceres-with-cmake>