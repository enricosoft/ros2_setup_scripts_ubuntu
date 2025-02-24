# ros2_setup_scripts_ubuntu

unofficial ROS2 install script for Ubuntu

Access https://docs.ros.org/en/jazzy/Installation.html to get the updated information.

## QuickStart

After downloading this repository, just run the following command.

```sh
./run.sh
```

If you modify any .sh script on windows, before run it on WSL run the command:
dos2unix run.sh
and
dos2unix ros2-jazzy-desktop-main.sh

## Usage

By default, `run.sh` will install `ros-jazzy-desktop`.   
If you need to install another package, use indivitual installers listed bellow.

### Individual installers

ROS 2 Jazzy (LTS)

* To install `ros-jazzy-ros-base`, use [`ros2-jazzy-ros-base-main.sh`](./ros2-jazzy-ros-base-main.sh) instead of `run.sh`.
* To install `ros-jazzy-desktop`, use [`ros2-jazzy-desktop-main.sh`](./ros2-jazzy-desktop-main.sh) instead of `run.sh`.


## Supported LTS Versions

Reference: [REP-0003](https://ros.org/reps/rep-0003.html), [REP-2000](https://ros.org/reps/rep-2000.html)

| Ubuntu | ROS 1 | ROS 2 |
| ------ | ----- | ----- |
| Ubuntu 24.04<br>EOL: June 2029[^5] | - | Jazzy<br>EOL: May 2029 |

* Note: Here, EOL for Ubuntu refers to the end of normal support, which is not Ubuntu Pro.

[^2]: https://ubuntu.com//blog/18-04-end-of-standard-support
[^3]: https://wiki.ubuntu.com/FocalFossa/ReleaseNotes
[^4]: https://discourse.ubuntu.com/t/jammy-jellyfish-release-notes/24668
[^5]: https://discourse.ubuntu.com/t/noble-numbat-release-notes/39890

## LICENSE

```

### Acknowledgements

`run.sh` is based on [https://index.ros.org/doc/ros2/Installation/Crystal/Linux-Install-Debians/](https://web.archive.org/web/20190618134850/https://index.ros.org//doc/ros2/Installation/Crystal/Linux-Install-Debians/)
by Open Robotics, licensed under CC-BY-4.0.  

`tutorial.sh` is based on [https://index.ros.org/doc/ros2/Tutorials/Colcon-Tutorial/](https://web.archive.org/web/20190618134901/https://index.ros.org/doc/ros2/Tutorials/Colcon-Tutorial/)
by Open Robotics, licensed under CC-BY-4.0.  

source: https://github.com/ros2/ros2_documentation

Access https://docs.ros.org/en/jazzy/Installation.html to get the updated information.
