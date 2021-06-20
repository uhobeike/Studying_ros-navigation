# studying_ros-navigation
[![turtlebot3_ci](https://github.com/uhobeike/studying_ros-navigation/workflows/turtlebot3_ci/badge.svg?branch=Turtlebot3_practice&event=push)](https://github.com/uhobeike/studying_ros-navigation/actions?query=workflow%3Aturtlebot3_ci)

#### 以下クリックして飛べます。

## [準備編（ros_install）](https://github.com/uhobeike/studying_ros-navigation/tree/ros_install)
## [実践編（Practical edition）](https://github.com/uhobeike/studying_ros-navigation/tree/Practical_edition)
## [実践編ソースコード（Turtlebot3_practice）](https://github.com/uhobeike/studying_ros-navigation/tree/Turtlebot3_practice)

## パッケージのインストール方法(ワークスペースの構築から)
```
*注意* catkin_makeを使用していたワークスペースでcatkin buildを行うには/build /installフォルダを削除する必要がある。
```

* `catkin build`を使用するためにインストール。
```
sudo apt install python-catkin-tools
```
* ワークスペースの構築
```
mkdir -p ~/turtlebot3pr_ws/src
cd turtlebot3pr_ws
catkin build
```
* ソースコードのクローン&依存パッケージのインストール
```
cd ~/turtlebot3pr_ws/src
git clone -b Turtlebot3_practice --recursive https://github.com/uhobeike/studying_ros-navigation.git
rosdep update
rosdep install -r -y --from-paths --ignore-src ./
```
* ビルド
```
catkin build
```
* ターミナル起動時に自動で設定を読み込むように設定
```
echo "source ~/turtlebot3pr_ws/devel/setup.bash" >> ~/.bashrc
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
source ~/.bashrc
```

