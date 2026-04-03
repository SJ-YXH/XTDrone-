若要使用这个代码，你首先需要安装好XTDrone，详细信息你可以查阅https://github.com/robin-shaun/XTDrone
其中launch文件请放置在PX4_Firmware/launch路径下
takeoff为主要工作包，包含代码，请将其解压后放置在catkin_ws/src目录下，然后对其进行编译，详细请参考如下位置：

<img width="471" height="1325" alt="image" src="https://github.com/user-attachments/assets/a3126b4c-4276-4e93-bf43-65e086ea1a17" />
<img width="455" height="1330" alt="image" src="https://github.com/user-attachments/assets/a882f86e-f4de-4d39-8bd0-848a1c9d0f86" />
打开终端运行roslaunch px4 takeoff.launch
新建终端输入 cd ~/XTDrone/communication/    python multirotor_communication.py iris 0 #建立通讯
新建终端输入cd ~/XTDrone/control/keyboard   python multirotor_keyboard_control.py iris 1 vel #打开键盘控制
将速度拉到0.4以上，按t解锁无人机，按b切换到offboard执行，此时无人机就会自动执行矩形路径飞行动作
