# Every Tool We Use

There are collection of scripts and packages for various use.

Path: src/narwhal_tool

## Teleop

Move the robot with keyboard 

```
ros2 run narwhal_teleop teleop
```

## Model Conversion - Yolo to Engine

```
python3 src/narwhal_tool/formatting_model/yolo_2_engine.py \
    --model src/narwhal_vision/<path>/best.pt \
    --half \
    --output_path src/narwhal_vision/<path>/best.engine
```

## Extract Raw Video from ROS2 Topic - Rosbag

Extract video from topic: /narwhal_cam/image_raw

Play rosbag by 

```
ros2 bag play <path to rosbag>
```

then

```
python3 src/narwhal_tool/extract_video_from_topic.py
```

