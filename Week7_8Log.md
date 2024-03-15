# ArcGIS Server on GCP: Creating an image and logging in on Google Cloud Platform
Objective: Set up a VM (Virtual Machine) for ArcGIS server

March 7 2024

Total Time worked on: 1 Hour 30 Minutes

> Requirements: A $50 credit in google cloud, on the account used. Or alternative method of payment. Work on this website https://console.cloud.google.com/getting-started

## Creating a VM for ArcGIS server that allows port access to an administrative port. [50 minutes]
### Setting up VM (20 minutes)
- [ ] Enable the Compute Engine API, which can be located from your project overview (Use cntrl f to help locate it.) Except this process to take a few minutes.
- [ ] From the Compute Engine VM instances, interface click, create instance. (Take note of the status field which indicates if it is running, important to monitor considering it costs money.)
- [ ] Give it an appropriate name then, change the bootdisk, within the bootdisk select custom image, from here view all and change the source to Shawn's ArcGIS server, then select the image that is available from this source.
- [ ] Next change the firewall to allow HTTP and HTTPS acces (ports 6080 and 6443 respectively), note after this is created the VM has to be edited to allow traffic from port 6443.

### Setting up Firewall Rules (10 minutes)
- [ ] After the VM is created select "setup firewall rules" then click "create firewall rule", under "Target" use the dropdown menu and select "all instances in this network" then locate "Source IPv-4" ranges and input "0.0.0.0/0" then go to the "protocals and ports" section, under "specified protocols and ports" under TCP ports input "6443" finally click create to finish the firewall rule.

### Accessing your VM (20 minutes)
- [ ] Next we need to set login credentials. To do this, navigate back to the VM instances under Compute Engine. Click the arrow next to RDP, under the connect field and click set windows password. From here set the username to "student" and copy the password keeping it in a safe space.
- [ ] To connect to the VM naviagte to remote desktop connection in file explorer.
- [ ] Select the External IP which is located in the Compute Engine VM instances menu. Paste the IP into remote desktop connection adding port ":6443" on the end.
- [ ] It will then prompt for credentials, select more choices, then use a different account, enter the user name "student" and the password you saved earlier.
- [ ] You will get a firewall warning but since you are the author you know you can accept it.
- [ ] After connecting you can close it by pressing the X on the top bar on the VM.
- [ ] Remember to stop the VM instance from the Computer Engine VM instances menu before leaving.

## Publishing Image Map to AGOL (10 minutes)
- [ ] Start the VM on Compute Engine.
- [ ] Connect to the VM.
- [ ] Open ArcGIS Pro, make a connection to the ArcGIS Server. Use the logins from the text file on the VM.
- [ ] On ArcGIS, the map has the image shared prior by Shawn.
- [ ] Publish this map item on AGOL.

## Creating an ArcGIS server on the VM and uploading a shapefile to it from ArcGIS Pro. [30 minutes]
- [ ] Start the VM on Compute Engine.
- [ ] Connect to the VM.
- [ ] On VM create this file path C:\GISWorkspace\Canada
> For our exercise we already have this folder path.
- [ ] On the local machine create this file path C:\GISWorkspace\Canada and put the Canada.zip folder into it. Then extract.
- [ ] Login to ArcGIS server manager on the VM, using the logins from the text file, and make a folder for the file.
- [ ] Open ArcGIS Pro, make a connection to the ArcGIS Server. Use the logins from the text file.
- [ ] Back on ArcGIS Pro add the shapefile to the project connected to the ArcGIS server on VM.
- [ ] On the server, right click on the server and publish the feature layer on ArcGIS server.
      


