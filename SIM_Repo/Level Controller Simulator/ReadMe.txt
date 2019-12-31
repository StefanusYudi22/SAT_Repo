This repository containing ready to run code of Level Controller Simulator. 
Comprises of : 
   1. Ready to run FORTE
   2. Ready to run mosquitto with Websocket
   3. Ready to run node-red json file
   4. Ready to run Realtime Graph html file

In order to fully operate the simulator you have to follow these steps : 
1. Download binary installation file of mosquito from here (https://mosquitto.org/download/), install it and make sure that “Mosquitto Broker” is ready as the services inside computer by checking in Start==> Run ==> Services.
2. Install Node-Red by following these steps (https://nodered.org/docs/getting-started/windows) for windows user, for another user just google the steps, there is plently there and I assure you it won’t difficult. Enter your Node-RED using your browser and go to manage palette menu. Add this palette on your node red : 
    - node-red-dashboard
    - node-red-contrib-filter
    - node-red-contrib-influxdb
3. Download InfluxDB from here (https://portal.influxdata.com/downloads/), and unzip it on certain location. Run the influxd.exe and then run the influx.exe, write the query “create database  LevelDB” to create the database named “LevelDB”.
4. Download all file from here and extract it. This files contain LCS_FORTE, LCS_Mosquitto, LCS_Node-RED, and LCS_RTGraph. 
5. Copy the files inside LCS_Mosquitto to directory where you install mosquito before, overwrite the original installation files in your computer (C:\Program Files\mosquitto). Then run Mosquitto Broker as service in your computer, make sure that port 0.0.0.0:1883 and 0.0.0.0:9883 is open in your computer by typing “netstat –an” inside command prompt (for windows user).
6. Run forte.exe file inside LCS_FORTE.
7. Open your node-red and import the LCS.json file inside folder LCS_Node-Red using import menu, and then click Deploy. 
8. Open LCS_Graph.html inside folder LCS_Graph. If you want to deploy Graph into your localhost just follow this steps (https://stackoverflow.com/questions/38497334/how-to-run-html-file-on-localhost).
9. Access your node-red user interface using your browser, go to localhost:1880/ui by default.

Enjoy the Level Controller Simulator
