# mypkg
![test](https://github.com/kit59/mypkg/actions/workflows/test.yml/badge.svg)

ロボットシステム学のROS2練習用リポジトリ
2つのノード間でデータのやり取りをすることが可能。

## Install
下記のコマンドでインストールが可能。
```
git clone https://github.com/kit59/mypkg.git
```

## talker.pyとlistener.py
mypkgというディレクトリ内に存在。
別々の端末でそれぞれを同時に実行することでデータのやり取りをすることが可能。
＊ 端末１
```
$ ros2 run mypkg talker

```
＊ 端末２
```
$ ros2 run mypkg listener
[INFO] [1704445484.918310094] [listener]: Listen: 34
[INFO] [1704445485.240505762] [listener]: Listen: 35
[INFO] [1704445485.740568980] [listener]: Listen: 36
[INFO] [1704445486.240195427] [listener]: Listen: 37
[INFO] [1704445486.740310432] [listener]: Listen: 38
[INFO] [1704445487.240282664] [listener]: Listen: 39
[INFO] [1704445487.740375605] [listener]: Listen: 40
```

## talk_listen.launch.py 
launchというディレクトリ内に存在。
下記のように実行することで１つの端末でtalker.pyとlistener.pyを通信させデータのやり取りをする事が可能。
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/kaito/.ros/log/2023-12-28-19-09-52-562601-Zora-5631
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [5633]
[INFO] [listener-2]: process started with pid [5635]
[listener-2] [INFO] [1703758193.644899645] [listener]: Listen: 0
[listener-2] [INFO] [1703758194.068820229] [listener]: Listen: 1
[listener-2] [INFO] [1703758194.567895246] [listener]: Listen: 2
[listener-2] [INFO] [1703758195.068341674] [listener]: Listen: 3
[listener-2] [INFO] [1703758195.568211421] [listener]: Listen: 4
[listener-2] [INFO] [1703758196.068853344] [listener]: Listen: 5
[listener-2] [INFO] [1703758196.571035567] [listener]: Listen: 6
[listener-2] [INFO] [1703758197.068374590] [listener]: Listen: 7
[listener-2] [INFO] [1703758197.570615760] [listener]: Listen: 8
[listener-2] [INFO] [1703758198.068581181] [listener]: Listen: 9
[listener-2] [INFO] [1703758198.568583861] [listener]: Listen: 10 
```

## 必要なソフトウェア
* Python
  * テスト済み: 3.7～3.10
* ROS2

## テスト環境
* Ubuntu 22.04 on Windows

## Licence
* このソフトウェアパッケージは, 3条項BSDライセンスの下, 再頒布および使用が許可されます 
* このパッケージのコードは, 下記のスライド (CC-BY-SA 4.0 by Ryuichi Ueda) のものを, 本人の許可を得て自身の著作としたものです.
    * [ryuichiueda/my_slides robosys_2022 lesson8.md](https://github.com/ryuichiueda/my_slides/blob/master/robosys_2022/lesson8.md)
    * [ryuichiueda/my_slides robosys_2022 lesson9.md](https://github.com/ryuichiueda/my_slides/blob/master/robosys_2022/lesson9.md)
    * [ryuichiueda/my_slides robosys_2022 lesson11.md](https://github.com/ryuichiueda/my_slides/blob/master/robosys_2022/lesson11.md)
* © 2023 Kaito Akiyama

