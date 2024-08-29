# Deploying-React-app-as-a-service-Linux-Ubuntu
## Project setup
```
npm install
```
## Create the vision.service file
```
nano /lib/systemd/system/vision.service
```
## Write the content for the vision.service file
```
[Service]
Type=simple
User=vision
Restart=on-failure
WorkingDirectory=/path/to/vision
ExecStart=npm run start -- --port=3000
```
## Update the service list
```
systemctl daemon-reload
```
## Start the service
```
systemctl start vision
```
## Check the service status
```
systemctl status vision
```
Open browser and check awesome React app.
