# Neoy SLAM Programming Learning Space

----

> This learning space is aim for concrete study of SLAM-related Programming skills!

## IDE for C++, Python Code Editting and Documentation

<img src="https://cdn.worldvectorlogo.com/logos/eclipse-11.svg" alt="Eclipse-C++ " height="50" title="Eclipse-C++ ">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/128px-PyCharm_Icon.svg.png" alt="Pycharm" height="50" title="Pycharm">
<img src="https://cdn.worldvectorlogo.com/logos/visual-studio-code-1.svg" alt="VS-Code"  height="50" title="VS-Code">

| IDE | Usage | 
| ------ | ----------- |
| Eclipse-C++  | C++ programming and coding reading |
| Pycharm  | Python programming and debugging |
| VS-Code  | Source coding upload to git and doxygen edit  |

### Eclipse-C++ Setup with Cmake 
<img src="https://cdn.worldvectorlogo.com/logos/eclipse-11.svg" alt="Eclipse-C++ "  height="50" title="Eclipse-C++ "><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/13/Cmake.svg/192px-Cmake.svg.png" alt="Cmake" height="50" title="Cmake">  <img src="https://images.squarespace-cdn.com/content/v1/606d378755a86f589aa297b7/1621897385511-NS0QWVKNHWBGWPM39B7L/ros_logo_large.png" alt="ROS" height="50" title="ROS">


 - **Cmake Project**, in build folder, use command `cmake -G "Eclipse CDT4 - Unix Makefiles"`
 - **ROS Package**, in catkin_ws folder, use command `catkin config -G"Eclipse CDT4 - Unix Makefiles" -DCMAKE_BUILD_TYPE=Release` 
 - **Cmake Project** use `cmake` [cmake CMakeLists.txt].
 - **ROS Package** use `catkin build` [catkin CMakeLists.txt] and  [catkin package.xml]

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