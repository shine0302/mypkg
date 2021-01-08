# 課題2　「パブリッシャ」と「サブスクライバ」の確認

#### 数字を１ずつカウントするプログラムとその264倍の数値を出力するプログラムを使い「パブリッシャ」と「サブスクライバ」の確認をした

	
------------------------
##### 動作環境
|||
|---|---|
|ターミナル|Linux(WSL) version4.4.0-|
|OS |ubuntu20.04.1 LTS|
|ROS|Melodic Morenia|
	
##### 使用機材(
||
|---|
|Raspberry Pi 3 Model B+ |
|ELECOM 有線LANアダプタ/USB2.0/Type-A/USBハブ付/ブラック #EDC-FUA2H-B|
|LANケーブル|


------------------------

#### 前準備
### ROSのインストール

1.[こちら(Ubuntu20.04)](https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)のリポジトリをgit cloneで取得  

※ubuntu18.04の場合→https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu18.04_server

2.リンク先の手順に沿って実行

### 環境構築
1~3のコマンドを入力  

1.  

	$ mkdir -p catkin_ws/src/
	$ cd ~/catkin_ws/src/　　
	$ cattkin_init_workspace


 2. ~/.bashrcの末尾に以下を追加  

	   　source /opt/ros/noetic/setup.bash       #これは元からある
	
	    source ~/catkin_ws/devel/setup.bash         #ここから3行追加　　
	
	    export ROS_MASTER_URI=http://localhost:11311　　
	
	    export ROS_HOSTNAME=localhost　　

3．環境のビルド

	$ cd ~/catkin_ws
	$ catkin_make
	$ source ~/.bashrc
	
	
-------------------------------------------------	
	


#### 操作手順
	1.cd ~/catkin_ws/src/
	2.>git clone  https://github.com/shine0302/mypkg.git//このリポジトリを取得
	2.cd ~/catkin_ws/src/mypkg/  　//ディレクトリに入る
	3.$　　　　　　　　　　//プログラムのコンパイル

	
		
------------------------

#### 動画
[YouTube](https://youtu.be/AbxvaAvc580)
※音はないです。

---------------------------
#### LICENCE
|Package|LICENCE|
|---|---|
|mypkg|BSD-3|
