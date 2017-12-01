# Robot Web Tools Demo Docker 


## Installation

```
  sudo apt-get install docker.io
  sudo docker.io pull robotwebtools/demos
```

## Execution

* Starts Docker Container. Rsbridge port will be exposed as localhost:8888
```
 > sudo docker.io run -d -p 8888:9090 robotwebtools/demos
```

* Open demo page. (Turtlebot2 URDF, Marker, Interactive Marker demo are supported)

<img src="turtlebot_webview.png" alt="alt text" width=400px></img>


## Customise 

1. Edit [Dockerfile](Dockerfile) and image name in [build_environment.sh](build_environment.sh)

2. Create image 

```
  ./build_environment.sh
```
