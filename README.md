# Intelligent-task-offloading-in-private-5g-networks
![image](https://github.com/user-attachments/assets/5fc29adb-279f-4535-a6e1-33bd8c4c17db)

Follow This repository for Multinode 5G setup using Open5gs, srsRAN and USRP B210 base station. After that we have used opencells 5G sims to overwrite sim and connect a 5G mobile phone to our 5G network

*https://github.com/ManojPandekamat/Private-5g-setup-with-Open5gs-and-srsRAN-and-B210*

Follow The [Steps](./Steps/) folder for setup steps 

***********************************************************************************************************************************************************************
**Total Work Flow**
***********************************************************************************************************************************************************************
1. User connects Private 5G network
2. User request to `schedular 10.45.0.1:5001/predict` endpoint
3. Schedular forword request to one of the selected node
    - Schedular for every 30 seconds requests the metrics such as CPU,MEMORY Utilization from the edge nodes
    - It predicts the future load of each node and select a best node that is below threshold value we had set during deployment.
    - If no edge node is availble below threshold value it forwards the request to backup node deployed in docker in remote server.
4. The Edge Node or cloud Node process the image and return the results to the user and send the processed data to the storage node  in openstack for future use.

***********************************************************************************************************************************************************************
**Note**
You can build all the Docker images mentioned in this project from scrach using [Build](./Build/) or we have already mentioned the images built during setup in the configuration files
