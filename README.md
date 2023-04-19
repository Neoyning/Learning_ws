# Neoy SLAM Programming Learning Space

----

> This learning space is aim for concrete study of SLAM-related Programming skills!

## IDE for C++, Python Code Editting and Documentation

<img src="https://cdn.worldvectorlogo.com/logos/eclipse-11.svg" alt="Eclipse-C++ " height="50" title="Eclipse-C++ "><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/128px-PyCharm_Icon.svg.png" alt="Pycharm" height="50" title="Pycharm"><img src="https://cdn.worldvectorlogo.com/logos/visual-studio-code-1.svg" alt="VS-Code"  height="50" title="VS-Code">

| IDE | Usage | 
| ------ | ----------- |
| Eclipse-C++  | C++ programming and coding reading |
| Pycharm  | Python programming and debugging |
| VS-Code  | Source coding upload to git and doxygen edit  |

### Eclipse-C++ Setup with Cmake 
<img src="https://cdn.worldvectorlogo.com/logos/eclipse-11.svg" alt="Eclipse-C++ "  height="50" title="Eclipse-C++ "><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/13/Cmake.svg/192px-Cmake.svg.png" alt="Cmake" height="50" title="Cmake">  <img src="https://images.squarespace-cdn.com/content/v1/606d378755a86f589aa297b7/1621897385511-NS0QWVKNHWBGWPM39B7L/ros_logo_large.png" alt="ROS" height="50" title="ROS">


 - **Cmake Project**, in build folder, use command `cmake -G "Eclipse CDT4 - Unix Makefiles"`
 - **ROS Package**, in catkin_ws folder, use command `catkin config -G"Eclipse CDT4 - Unix Makefiles" -DCMAKE_BUILD_TYPE=Release` or `catkin build packageName --cmake-args -G"Eclipse CDT4 - Unix Makefiles" -D CMAKE_BUILD_TYPE=Release`
 - **Cmake Project** use `cmake` [cmake CMakeLists.txt].
 - **ROS Package** use `catkin build` [catkin CMakeLists.txt] and  [catkin package.xml]
 - Configure **Cmake** and **Eclipse** for project *debug* or *run*


> **Method 1** `cmake -G"Eclipse CDT4 - Unix Makefiles" -D CMAKE_BUILD_TYPE=Debug -DEigen3_DIR=$HOME/git/eigen-3.3.7 ../../src/learnCeres/` (Preferred). Or 

> **Method 2** `set(CMAKE_BUILD_TYPE Debug)	#set to Debug or Release` in `CMakeLists.txt` file. 

**Method 1** should implement before Eclipse importing; [Cmake + Eclipse]

+ `-G"Eclipse CDT4` generate Eclipse readable project;
+ `-D CMAKE_BUILD_TYPE=Debug` is equivalent of **Method 2**;
+ `-D Eigen3_DIR=$HOME/git/eigen-3.3.7` specify the `Eigen3_DIR`;
+ `../../src/learnCeres/` means in `eclipse-workspace` folder has build and source directories as sisters `eclipse-workspace/src` and  `eclipse-workspace/build`. Note that the `.cpp` source files and `CMakeLists.txt` should inside `eclipse-workspace/src/projectName`.


 >NOTE 1: In Eclipse, set `Debug configuration`. Especially do search `C/C++ Application`. see [Debugging a Project]

 >NOTE 2: Use **cmake-gui** to check cmake VARIABLE like `Ceres_DIR`, `Eigen2_DIR`, `CMAKE_BUILD_TYPE`, `CMAKE_INSTALL_PREFIX`, install GUI by

 ```sh
 sudo apt-get install libceres-dev
 ```

**Method 2** can use after **Method 1**, then in Eclipse importing `Existing Projects into Workspace`.

+ For **Cmake Project** importing, select root directory at `/home/neoy/eclipse-workspace/build/projectName` 

cmake Workspace Folder Structure for Eclipse-C++
```
eclipse-workspace
├── build
│   ├── learnCeres
│   └── learnEigen
└── src
    ├── learnCeres
    └── learnEigen
```
+ For **ROS Package** importing, select root directory at `/home/neoy/catkin_ws/build/rosPackageName`

catkin Workspace Folder Structure for ROS

```
catkin_ws
├── build
│   ├── beginner_tutorials
│   └── ros_package_template
├── devel
├── logs
│   ├── beginner_tutorials
│   └── ros_package_template
└── src
    ├── beginner_tutorials
    └── ros_package_template -> /home/neoy/git/ros_package_template/
```



### Pycharm Setup with Anaconda
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/128px-PyCharm_Icon.svg.png" alt="Pycharm" height="50" title="Pycharm"><img src="https://upload.wikimedia.org/wikipedia/en/thumb/c/cd/Anaconda_Logo.png/240px-Anaconda_Logo.png" alt="Anaconda" height="50" title="Anaconda">

 - In Pycharm, use `Python Interpreter` to switch between different environments.

### VS-Code Setup with Git

<img src="https://cdn.worldvectorlogo.com/logos/visual-studio-code-1.svg" alt="VS-Code"  height="50" title="VS-Code"><img src="https://cdn.worldvectorlogo.com/logos/git-icon.svg" alt="Git" height="50" title="Git">

> NOTE: Clone remote github repositories and edit it locally

 - Create a New repository from github page [Github]
 - Install VS-Code in your Computer [VS-Code Download] and [VS Keyboard Shortcut]
 - Add Python and C++ Extension in VS-Code 
 - Clone a repository locally [Intro to Git in VS-Code]


## Learning-based Packages

<img src="https://pytorch.org/assets/images/pytorch-logo.png" alt="Pytorch" height="50" title="Pytorch">

| Package | Description | 
| ------ | ----------- |
| Pytorch   | NN Model Building, Training ,Testing and Evaluation|


## Model-based Packages 

<img src="https://eigen.tuxfamily.org/dox/Eigen_Silly_Professor_64x64.png" alt="Eigen"  height="50" title="Eigen">
<img src="https://avatars.githubusercontent.com/u/6327561?s=200&v=4" alt="Ceres"  height="50" title="Ceres">

| Package | Description |
| ------ | ----------- |
| Eigen   | Matrix Operation |
| Ceres   | Computer vision specified optimizatiopn tool | 
| g2o   | Computer vision specified optimizatiopn tool | 
| GTSAM   | Factor Graph based optimizatiopn tool | 


[Github]: <https://github.com/>
[VS-Code Download]: <https://code.visualstudio.com/download>
[VS Keyboard Shortcut]: <https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf>
[Intro to Git in VS-Code]: <https://code.visualstudio.com/docs/sourcecontrol/intro-to-git>
[cmake CMakeLists.txt]: <https://cmake.org/cmake/help/latest/guide/tutorial/index.html>
[catkin CMakeLists.txt]: <http://wiki.ros.org/catkin/CMakeLists.txt>
[catkin package.xml]: <http://wiki.ros.org/catkin/package.xml>
[Debugging a project]: <https://rtist.hcldoc.com/help/index.jsp?topic=%2Forg.eclipse.cdt.doc.user%2Fgetting_started%2Fcdt_w_debug.htm>
[Cmake + Eclipse]: <https://jvgomez.github.io/pages/how-to-configure-a-cc-project-with-eclipse-and-cmake.html>