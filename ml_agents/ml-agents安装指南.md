# 使用Unity进行机器学习

安装官方指南：https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md

以下是步骤：

* 下载[miniconda](https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe)并安装:
  https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe

* 打开`开始`菜单中新增的AnacondaPrompt 

* 执行 :

  * `conda create -n tf2 python=3.7 -y` 

  * `conda activate tf2`

  * 在D盘某目录新建一个文件夹准备存放接下来的项目, 如在windows中路径是`D:/guang`

  * 在AnacondaPrompt 中执行`cd D:/guang`

  * ```
    git clone --branch latest_release https://github.com/Unity-Technologies/ml-agents.git
    cd ml-agents/ml-agents-envs
  pip install -e ./
    cd ..
    cd ml-agents # 修改本文件夹中的setup.py：tensorflow->tensorflow-gpu
    pip install -e ./
    ```

* 在Unity新建一个Project 

  * 安装Barracuda：

    > To install the Barrcuda package in later versions of Unity, navigate to the Package Manager window by navigating to the menu `Window` -> `Package Manager`. Click on the `Adavanced` dropdown menu to the left of the search bar and make sure "Show Preview Packages" is checked. Search for or select the `Barracuda` package and install the latest version

  * 将目录 `ml-agents/ml-agents/UnitySDK` 下的Assets添加至你的project.

* 上述都成功之后，在AnacondaPrompt 中进入目录`D:/guang/ml-agents`执行：
  `mlagents-learn config/trainer_config.yaml --train`
  
* 然后在Unity中，定位至Assets>ML-Agents>Example>3DBall>Scenes 去play 3DBall开始训练.