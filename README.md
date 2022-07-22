# ROS_Installation
First you need to download VirtualBox which is an Open Source Software that you use it to install other OS in your device.

Second is installing Ubuntu and here is the steps on how to install it :

1-Download ubuntu https://releases.ubuntu.com/20.04/

2-Open VirtualBox then click on new.

3-When you name it ubuntu the virtualbox is smart enough to automaically configure the type and version
 to Linux and Ubuntu(64bit) then click next.
 
 4-In memory size it better to put the mark in the end of the green line then click next.
 
 5-In Hard disk choose whatever you like then click create.
 
 6-In Hard disk file type Leave as it is (VDI) then click next.
 
 7-In Storage on physical hard disk choose what you like then click next.
 
 8-In file location and size choose what you like but and make sure to have enough space in the disk then click create.
 
 9-Right Click on the created OS then click setting. In general go to advance and make Shared Clipboard and Drag/Drop to Bidirictional. so you can copy and paste from the virtual OS and your real OS. Then go to system then processor it better to put the mark in the end of the green.
 
 10-Then go to storage and here you going to link the ubuntu that you privisolly downloaded with the VOS you created by clicking the empty word then click on the blue circle > choose disk file > click on the ubuntu version that you downloaded then click ok.And you done configure it in you VirtualBox but still there is a couple of things to do.
 
 11-Click start , install ubuntu then choose your keyboard language then click continue.
 
 12-Here make sure to click on Install third-paty etc... then click continue.
 
 13-Then Install Now and dont worry it will not erase anything in your hard disk. 
 
 14-Choose your city then click continue.
 
 15-Your Name,Password etc... then continue.
 
 16-It will take some time to install and when it done installing restart the VOS and you done! Congrats.
 
 To install ROS follow the guide in https://wiki.ros.org/noetic/Installation/Ubuntu to install ROS neotic, it very easy if you follow the guide step by step it will not take much time to do it.


How to install ROS Melodic on Jetson Nano

1- Open new Terminal and copy paste the following command: (sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list')

2- Update the package list: (sudo apt update)

3- Then type: (sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654) After you type the command and press Enter, press Y and hit Enter when asked if you want to continue. It will take a while to download all this stuff, so feel free to take a break while ROS downloads to your system.

4-Type:(sudo apt-get update) then type:(sudo apt install ros-melodic-desktop-full) Type Y and press Enter to complete the installation.

5-Set up the environment variables: (echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc) then (source ~/.bashrc) Note that anytime you want to see what environment variables ROS is using, you can type the following command: (export | grep ROS)

6-Install some other tools that you will work with in ROS. After you type the command below, press Y and Enter to complete the download process: (sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential) Press Y and hit
Enter.

7-Now initialize rosdep. This is a tool that is required before you can use ROS (sudo apt install python-rosdep) > (sudo rosdep init) > (rosdep update) The last stage of installation is presented here. Verify the ROS version you have installed. You have successfully installed ROS if you see your ROS version in the output: (rosversion -d)
