# Task completed in Week 13
## Create a GitHub repository for web hosting (20 Minutes)
With all four group member's agreement, I created a Github repository https://github.com/georajesh/geom99-project for hosting our Project Website.
- [ ] With Create new option, create a new repository.
- [ ] Inside repository settings, under Pages option, activate the build and deployment settings. 

## Getting started with Web Designing (120 Minutes)
Applying the skills developed from GEOM 101 and implementing the ideas from assignments and project completed in GEOM 101 from last term, landing page for our project is created.
- [ ] Application of ArcGIS Maps SDK for JavaScript
'javascript'
        require(["esri/config", "esri/Map", "esri/views/MapView"], function(esriConfig, Map, MapView) {
        esriConfig.apiKey = "API Key";
      
        const webmap = new WebMap({
          portalItem: {
            // autocasts as new PortalItem()
            id: "App ID"
          }
        });
        const view = new MapView({
          map: Map,
          center: [X,Y], // Longitude, latitude
          zoom: 13, // Zoom level
          container: "viewDiv" // Div element
        });
      });

> API for our Application is used for Dashboard however, we found it is not working and we still have it to figure out whether we use ArcGIS Maps SDK or just <iframe> to display our AGOL solution.
