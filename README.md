# Class-7.5-Assignments

## Steps to create a VM in Google Cloud
1. Open Console and select VM Instances
2. Click on Creare Instance
3. Under Machine Configuration, fill in the Name field for the name of your instance
4. Select Machine type (E2 is ok)
5. On left pane, ***ignore*** OS and storage and click on Data Protection.
6. To avoid charges later, click on No backups.
7. On left pane, click on Networking and select Allow HTTP traffic.
8. On the left pane, ***ignore*** Observability and Security tabs and select Advanced.
9. Copy your user_data.sh script (this may be called something else depending on what version you choose.) and paste it inside the Automation-startup script box.
10. Ignore all other settings and click on Create.
11. Wait a few moments until your instance status shows green check mark. This indicates your instance has been initialized and is ready to access. 
12. Hover you mouse cursor over the link in External IP until the double-box icon shows up. This is used to copy the external IP of the instance. 
13. Copy external IP of your instance and paste it into a browser address bar using the following format: `http://<external- IP> `
14. This should load the web page of your instance. 