## INSTALL ROS2 \ GAZEBO ON WINDOWS 11 USING WSL
[NOTE: you need windows 11 because it has better support to wslG, the wsl gui]

```
wsl --install -d Ubuntu-24.04
```

```
wsl --list --verbose
```
# If the wsl versione of our ubuntu distro row is 1, run the following command:
```
wsl --set-version Ubuntu-24.04 2
```

```
wsl --set-default Ubuntu-24.04
```

```
wsl
```
# Start the default distro and the first time it will ask you to set the user and pwd

```
sudo apt update
sudo apt upgrade
cd /home/{youUsername}
```

# Install Ros2-jazzy desktop as default
```
git clone https://github.com/enricosoft/ros2_setup_scripts_ubuntu
sudo ./run.sh
source /opt/ros/jazzy/setup.bash
```
# Test it
```
ros2
rviz2
```

# Now we should install gazebo because it's not included in ros2-desktop (Rviz it is)
```
sudo apt-get install -y lsb-release gnupg curl

sudo curl -sSL https://packages.osrfoundation.org/gazebo.gpg -o /usr/share/keyrings/pkgs-osrf-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/pkgs-osrf-archive-keyring.gpg] http://packages.osrfoundation.org/gazebo/ubuntu-stable $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/gazebo-stable.list > /dev/null

sudo apt-get update
sudo apt-get install gz-harmonic
sudo apt-get install ros-jazzy-ros-gz
```

# Test it
```
gz sim
```
