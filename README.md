# 課題2　「パブリッシャ」と「サブスクライバ」の確認

#### 数字を１ずつカウントするプログラムとその264倍の数値を出力するプログラムを使い「パブリッシャ」と「サブスクライバ」の確認をした

	
------------------------
##### 動作環境
|||
|---|---|
|ターミナル|Linux(WSL) version4.4.0-,Tera Term|
|OS |ubuntu20.04.1 LTS|
|ROS|Melodic Morenia|
	
##### 使用機材(
||
|---|
|Raspberry Pi 3 Model B+ |
|ELECOM 有線LANアダプタ/USB2.0/Type-A/USBハブ付/ブラック #EDC-FUA2H-B|
|LANケーブル|


------------------------
### ROSのインストール

1.[こちら( ubuntu20.04)](https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)のページのリポジトリをgit cloneで取得  


※引用元:Ryuichi Ueda,https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server ,2021/1/8(last visit) 

2.以下のコマンドを実行
	
	$ cd ros_setup_scripts_Ubuntu20.04_server
	$ bash step0.bash
	$ bash step1.bash

### 環境構築
1.  ディレクトリの作成(以下のコマンドを入力）

	$ mkdir -p catkin_ws/src/
	$ cd ~/catkin_ws/src/　　
	$ cattkin_init_workspace


 2. ~/.bashrcの末尾に以下を追加  

	   　 source /opt/ros/noetic/setup.bash       #これは元からある
	
	    source ~/catkin_ws/devel/setup.bash         #ここから3行追加　　
	
	    export ROS_MASTER_URI=http://localhost:11311　　
	
	    export ROS_HOSTNAME=localhost　　

3．環境のビルド(以下のコマンドを入力)

	$ cd ~/catkin_ws
	$ catkin_make
	$ source ~/.bashrc
	
	
-------------------------------------------------	
	


#### 操作手順
	1.& cd ~/catkin_ws/src/                  
	2.$ git clone  https://github.com/shine0302/mypkg.git  //このリポジトリを取得
	3.$ cd ~/catkin_ws/src/mypkg/launch
	4.$ roscore & 　　　　　　　　　　　　　　　//バックグラウンドでrosを起動、ctrl+cで抜けていい
	5.$ roslaunch mypkg mypkg.launch          //実行
	6.別の端末を立ち上げる　
	7.$ rostopic echo /giant            //確認
　　　　　　　　　

※もし動かなかったら(パーミッションの設定）

	 1.cd ~/catkin_ws/src/mypkg/ 
	 2.$chmod +x count.py 
	 3.$chmod +x giant.py 
		
------------------------

#### 動画
[YouTube](https://youtu.be/AbxvaAvc580)
※音はないです。

---------------------------
#### LICENCE
|Package|LICENCE|
|---|---|
|mypkg|BSD-3|
