## Execution
### Build simulatorwrapper image

Run command

`dts devel build -f`

### Start docker containers

Run command `docker-compose up` from the directory where the file *docker-compose.yaml* resides.

### Monitor and publish rostopic

Run command

`dts start_gui_tools fakebot`

or

`docker run -it --net host duckietown/dt-ros-commons:daffy-amd64 /bin/bash`

To monitor image publisher, run command `rqt_image_view` and select topic */fakebot/camera_node/image/compressed* .

// Doesn't seem to be working
To change wheel velocity, run command `rostopic pub /fakebot/wheels_driver_node/wheels_cmd /fakebot/kinematics_node 'auto','X','Y'`. Replace *X* and *Y* with desired velocity of left and right wheel, respectively. 
