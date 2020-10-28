# AndroidDM-VM-Cloud
AndroidDM Server for cloud VM, such as aliyun VM, azure VM

# git clone https://github.com/EdgeSolution/AndroidDM-VM-Cloud.git

# run application
  - The virtual machine needs to expose ports: 8080, 30001, 30002, 1883, 5432, 5500, 5901, 9191, 9000
  - Run start.sh

# Run the Debian slim docker image for AndroidDM

# v1.0.0 version
 - New features
 - docker images version
  - localhost/harbor/androiddm-javaenv-admin:v1.0.0
  - localhost/harbor/androiddm-astore-slim-admin:v1.0.0
  - localhost/harbor/androiddm-mosquitto-admin:v1.0
  - localhost/harbor/androiddm-novnc-admin:v1.0
  - postgres:9.4
  - portainer/portainer
