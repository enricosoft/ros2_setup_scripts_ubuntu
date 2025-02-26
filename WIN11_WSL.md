## INSTALL ROS2 \ GAZEBO ON WINDOWS 11 USING WSL

```
wsl.exe --update
wsl --install -d Ubuntu-24.04
```

```
wsl --list --verbose
```
# If the wsl versione of our ubuntu distro row is 1, run the following command:
```
wsl --set-version Ubuntu-24.04 2
```

# Then set this distro as default:
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
echo "source /opt/ros/jazzy/setup.bash" >> ~/.bashrc && source ~/.bashrc
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
