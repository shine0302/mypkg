# 課題2　ROSパッケージの作成

####  数字をカウントするパッケージを作成

#### 内容
	
------------------------


#### 動作環境
|||
|---|---|
|ターミナル|Linux(WSL) version4.4.0-|
|OS |ubuntu20.04.1 LTS|
|ROS|ROS kinetic|
-----------------------
	
#### 使用機材
||
|---|
|Raspberry Pi 3 Model B+ |
|ELECOM 有線LANアダプタ/USB2.0/Type-A/USBハブ付/ブラック #EDC-FUA2H-B|
|LANケーブル|
	
			
------------------------

#### 前準備
### ROSのインストール
1.[こちら](https://github.com/ryuichiueda/ros_setup_scripts_Ubuntu20.04_server)のリポジトリをgit cloneでインポート  
2.リンク先の手順に沿って実行

### ワークスペースの準備
1.  

	$ mkdir -p catkin_ws/src　　

2.

	$ cd ~/catkin_ws/src　　

3.

	$ cattkin_init_workspace


 4. .bashrcの末尾に以下を追加  

	    source /opt/ros/noetic/setup.bash       #これは元からある
	
	    source ~/catkin_ws/devel/setup.bash         #ここから3行追加　　
	
	    export ROS_MASTER_URI=http://localhost:11311　　
	
	    export ROS_HOSTNAME=localhost　　
	
-------------------------------------------------	
	


#### 操作手順
	1.>git clone  //このリポジトリを取得
	2.　　　//ディレクトリに入る
	3.　　　　　　　　　　//プログラムのコンパイル

	
		
------------------------

#### 動画
[YouTube]
※音はないです。

---------------------------
#### LICENCE
|Package|LICENCE NAME|
|---|---|
|mypkg|BSD-3|
