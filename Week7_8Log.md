# ArcGIS Server on GCP: Creating an image and logging in on Google Cloud Platform
Objective: Set up a VM (Virtual Machine)
Feburary 22 2023
Time worked on: 45 minutes

> Requirements: A $50 credit in google cloud, on the account used. Or alternative method of payment. Work on this website https://console.cloud.google.com/getting-started

## Creating a VM for ArcGIS server that allows port access to an administrative port. [40 minutes]
### Setting up VM
- [ ] Enable the Compute Engine API, which can be located from your project overview (Use cntrl f to help locate it.) Except this process to take a few minutes.
- [ ] From the Compute Engine VM instances, interface click, create instance. (Take note of the status field which indicates if it is running, important to monitor considering it costs money.)
- [ ] Give it an appropriate name then, change the bootdisk, within the bootdisk select custom image, from here view all and change the source to Shawn's ArcGIS server, then select the image that is available from this source.
- [ ] Next change the firewall to allow HTTP and HTTPS acces (ports 6080 and 6443 respectively), note after this is created the VM has to be edited to allow traffic from port 444.

### Setting up Firewall Rules
- [ ] After the VM is created select "setup firewall rules" then click "create firewall rule", under "Target" use the dropdown menu and select "all instances in this network" then locate "Source IPv-4" ranges and input "0.0.0.0/0" then go to the "protocals and ports" section, under "specified protocols and ports" under TCP ports input "6443" finally click create to finish the firewall rule.


- [ ] Next we need to set login credentials. To do this, navigate back to the VM instances under Compute Engine. Click the arrow next to RDP, under the connect field and click set windows password. From here set the username to "student" and copy the password keeping it in a safe space.
- [ ] To connect to the VM naviagte to remote desktop connection in file explorer.
- [ ] Select the External IP which is located in the Compute Engine VM instances menu. Paste the IP into remote desktop connection adding port ":444" on the end.
- [ ] It will then prompt for credentials, select more choices, then use a different account, enter the user name "student" and the password you saved earlier.
- [ ] You will get a firewall warning but since you are the author you know you can accept it.
- [ ] After connecting you can close it by pressing the X on the top bar on the VM.
- [ ] Remember to stop the VM instance from the Computer Engine VM instances menu before leaving.
- [ ] Next Steps: Creating a server on the VM and uploading to it.


## Creating an ArcGIS server on the VM and uploading a shapefile to it from ArcGIS Pro. [30 minutes]
- [ ] Start the VM on Compute Engine.
- [ ] Setup a domain/url on DuckDNS. https://www.duckdns.org/
- [ ] Update the IP on the domain to the external IP from Compute Engine.
- [ ] Connect to the VM.
- [ ] On the VM create this file path C:\GISWorkspace and put the Canada.zip folder into it. Then extract.
- [ ] Open ArcGIS Pro, make a connection to the DuckDNS domain through ArcGIS Server. Use the logins from the text file on the VM.
- [ ] Login to ArcGIS server manager on the VM, using the logins from the text file, and make a folder for the file.
- [ ] Back on ArcGIS Pro upload the shapefile to the server being sure to refresh the server after the folder creation.
- [ ] After uploading shapefile navigate to its rest endpoint and use this as a reference to upload it on AGOL.
- [ ] Upload the rest endpoint url as the feature layer reference on AGOL, my navigating to new item from the contents page.
- [ ] Open the ArcGIS Server Rest API link on the VM desktop.
- [ ] Reference the url in AGOL map viewer, switching to domain to your DNS url but keeping the path to file.
- [ ] Save and Publish this item on AGOL.
