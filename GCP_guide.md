# Getting Started with Google Cloud Platform - Your own virtual machine.
If your account does not have a GCP project, you must create one to follow the steps. Only one project owned by you is needed for all tasks in this document.
- [ ] To create a project (if not automatically created) then click on the project list (above) and click New Project.
- [ ] The new project window appears. Enter a unique project name for your content. Your account is an individual one, so no organization will be set.
- [ ] Once created, select this project to continue.

## Run a GCP Virtual Machine to test ArcGIS Server
These instructions copy and launch a virtual machine image into your account. These steps only need to be done once to copy the VM into your account. After, you can stop/start your copy of the image to work with ArcGIS Server.

- [ ] Open google cloud console and enable CGP Compute Engine API (if not already enabled). This is what will be used to create the virtual machine (VM).
- [ ] Once enabled open the Compute Engine console to start creating the new virtual machine.
- [ ] Once in the compute engine console, initiate the Create Instance tool using the button (the button might be hidden in the ellipsis (... but vertical) depending on your screen width).
- [ ] Name the VM apropriately.
> First, name the virtual machine. The recommended name is arcgisserver-geom99, but this can be set to anything meeting GCP’s requirements without concern.
> The cloud is not a mythical place—it always has a location, and in this case we will be creating this virtual machine on a server in Iowa (take a look at the facility on google maps: https://goo.gl/maps/MQi2Hb1A18AqXZPA6)
- [ ]  For machine configuration we will use the defaults. This sets the “size” of the virtual machine: You can allocate more virtual CPUs, or more ram by changing the series or machine family (but will cost more). This can be changed with the VM not running if needed using the GCP console. The costs increase significantly with more CPUs and ram! For this task the e2-medium is enough, but in a business or production environment use Esri’s requirements (8gb RAM).
- [ ]  Google cloud provides different images to start from. Most are Linux-based, since the operating system is free. We will use Windows systems since that is what you are more familiar with (which premium charge is levied given Microsoft Windows Server is not free!). The image we will select was custom created with ArcGIS Server pre-installed and configured on a Windows Server. Click Change to find the instructors’ provided image.
- [ ]  The image provided is a custom one (select Custom Images). This custom image is not in your Google Cloud Project—it is stored in the instructor’s account. You must change the project to be the one indicated by your instructor (ArcGIS Server for 2023)
> Note: This step will not work if your google account has not been granted the necessary permissions. If you cannot see the ArcGIS Server project, then you must contact the instructor with your google account username to be given access.

- [ ]  Click All and click on Shawn’s ArcGIS Server project entry. (again, if you cannot see this contact the instructor and provide your google email address to be given access).
- [ ]  Once the project is selected, you will be able to see the custom images in the image dropdown list. There should only be one image listed, but if there are multiple pick the one with the latest version number/date.
- [ ]  Select the image
