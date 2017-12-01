FROM ros:kinetic-ros-base
MAINTAINER Jihoon Lee <jihoonlee.in@gmail.com>

# Install system dependencies
RUN apt-get update && apt-get install -y --force-yes tmux wget
RUN apt-get install -y --force-yes ros-kinetic-turtlebot ros-kinetic-rosbridge-suite ros-kinetic-tf2-web-republisher
RUN apt-get install -y --force-yes ros-kinetic-joint-state-publisher ros-kinetic-visualization-marker-tutorials ros-kinetic-interactive-marker-tutorials ros-kinetic-interactive-marker-proxy
RUN apt-get install -y --force-yes vim git python-wstool

# Create userid for building and running ROS applications
RUN useradd -m ros
RUN adduser ros root

# Install turtlebot webview launcher
RUN cd /tmp; wget https://raw.githubusercontent.com/jihoonl/rwt_dockers/master/demos/files/rwt_demos.launch
RUN mv /tmp/rwt_demos.launch /home/ros/

# Install turtlebot webview start script
RUN cd /tmp; wget https://raw.githubusercontent.com/jihoonl/rwt_dockers/master/demos/files/start.sh
RUN mv /tmp/start.sh /home/ros/
RUN chmod +x /home/ros/start.sh

EXPOSE 9090

CMD ["/bin/bash", "/home/ros/start.sh"]
