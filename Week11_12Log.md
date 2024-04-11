# Web 4 Indoor Navigation (Solution not Recommended)
Objective: Explore solution related to Indoor Floor Navigation Problem

March 17 - 30, 2024

Total Time worked on: aprox. 5 hours

> These two weeks were quite exploratory. While other team members were working on ESRI side of the solution, I found an exciting repository on GitHub which was employing QGIS and Leaflet to solce Indoor floor related problems. Also, this solution didn't work for me because later I realized the data we have, we didn't have the full right to create 3D surface on it and also, the site that was suppose to processon the geojson files went down. So, these to items are very much mandatory to froceed with this approach.

WRLD Indoor Mapping Solution : https://github.com/wrld3d/wrld-indoor-maps-api

## Connecting ArcGIS REST end to QGIS [20 minutes]
- [ ] On the browser pane on the left side of QGIS project, Right click on ArcGIS Rest Server and add new server using REST ennd link.
- [ ] After making connection with the ArcGIS server, add layers to the project.

## Digitizing floor plans, 3D views and network path [3.2 hours]
> This process was quite a lessonful session I had in all of this solution finding journey. It is awakward how we spend hours in stuff that doesn't work and finally know the reason why it didn't work. Even though the procedures were straight and doable there was something (what I thought at first) which was not allowing me to do 3D development in QGIS using Advance Editing Option. I spent quite a time on this, finding the reasons and issue to my problem.
### Problem Identification
> The prooblem was on the data we have. Because we have no privilege to edit UDOT floor plan, a new floor plan layer had to be created in QGIS to accomplish Advance Editing Option.
- [ ] Create new feature {Polygon - Floor Plans, Line - Navigation and routing} Create Feature tool. 
- [ ] Activate toggle edit option and start digitizing the required plan and path.


### Exporting layers into geojson and further (1.2 hours)
- [ ] After the layers are ready, export each layers to geojson file format using Export tool.
> Another issue again. A late realization, of how these geojson files are to be sent to Wrld-indoor-maps using an account in the domain https://wrld3d.com/, I'm stucked here because the site is not functional and I haven't been able to access it.


> With whatever I went through, I have a sense that QGIS can solve this problem along with Leaflet without using any commercial APIs so, my next learning will be focused on digitizing my own floor plan(small scale) and generating 3D perspective and using Leaflet for mapping solution. 


