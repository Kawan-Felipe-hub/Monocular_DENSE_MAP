# Manual - NUVEM_DE_PONTOS_DENSA versão 1.0

## NÓ - CÂMERA

```python
ros2 run usb_cam usb_cam_node_exe --ros-args     -p video_device:=/dev/video0     -p pixel_format:="mjpeg2rgb"     -p camera_info_url:="file:///home/roboime/dev/rtab/camera.yaml"     -p frame_id:=default_cam
```
Obs: verifique o caminho do .yaml e se a câmera está configurada como video0!

## NÓ - Midas

```python
python3 midas_ros2.py
```
Obs: verifique se está na pasta do projeto!


## NÓ - RTAB

```python
ros2 launch rtabmap_launch rtabmap.launch.py     rtabmap_args:="--delete_db_on_start --Vis/MinInliers 10 --Mem/IncrementalMemory true"     rgb_topic:=/image_raw     depth_topic:=/camera/depth_registered     camera_info_topic:=/camera_info     frame_id:=default_cam     approx_sync:=true     approx_sync_max_interval:=0.7     wait_imu_to_init:=false     qos:=1    visual_odometry:=true
```
