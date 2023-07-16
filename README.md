# Mujoco_VR
This project uses the open source simulation engine mujoco for simulation and visualization, and realizes grasping and manipulation through real-time motion capture equipment.

This project can only run on **windows** at present, and the software and hardware involved are:
1. [mujoco200](https://www.roboti.us/index.html) For simulation and visualization.
2. [senseglove-nova](https://www.senseglove.com/product/nova/) Used to get the position of the finger joints.
3. [Htc HDM and tracker](https://www.vive.com/cn/product/vive-pro2-full-kit/overview/) Used to obtain stereo vision and the position and posture of the palm
   
### Usage
In the vive_tracker floder,\
run command.bat


## Nova_senseglove
Based on [SenseGlove-API](https://github.com/Adjuvo/SenseGlove-API)

### Usage
In the .\nova_glove\SGCoreCpp\examples\BasicCpp folder,Open x64 Native Tools Command Prompt for VS 2017,
*mkdir build* \
*cd build* \
*cmake ..* \
Then open the *SGCore_Example.sln* to run project

## Vive-Tracker
Based on [triad_openvr](https://github.com/TriadSemi/triad_openvr)
run python .\scripts\vive_tracke_win.py

## HTC-Mujoco
Based on [Mujoco-VR-htcvive](https://github.com/YujieLu10/Mujoco-VR-htcvive)
### Setup
Run makefile in src/ to build .exe files in the mujoco200/bin/ folder \
Open VS2015 x64 Native Tools Command Prompt \
Navigate to src/ directory in repo \
Run nmake -f makefile \
Run the code after making by navigating to mujoco200/bin/ and running mjvive.exe ..\\..\vive-mujoco\model\sawyer_rope.xml->mjvive.exe ..\\..\mujoco-htcvive\model\sawyer_rope.xml

### Notes

mjvive.py currently doesn't work \
minivive.cpp is mjvive.cpp without controllers
