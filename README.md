# ROS2 OLED SSD1306 for Waver

## Description

This ROS2 package made in C++ provides a way to drive an SSD1306 128x32 Oled display with I2C interface. Based on the work of Andrew Duncan, this package has been modified to work with ROS2 and includes a simple example of how to use the driver to display text and graphics on the OLED screen.

## Prerequisites
- A RapsberryPI or Embedded sistem connected with an SSD1306 128X32 OLED display connected via I2C.
- A ROS2 workspace set up and sourced.
- This `waver_oled_ssd1306` package cloned into the `src` directory of your ROS2 workspace.


## Configuration

Install the required dependencies:
```
sudo apt update
sudo apt install -y libi2c-dev iw
```

```
cd <ros2_workspace>/src
colcon build --packages-select waver_oled_ssd1306
```

## Usage

```
## run in a first terminal
ros2 run waver_oled_ssd1306 waver_oled_ssd1306_node

## run in a second terminal
ros2 topic pub /oled_text/first std_msgs/msg/String "{data: 'Hello Waver'}"
```
