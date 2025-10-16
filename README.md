## Objective

We have created a SAPUI5 application and want to deploy it to the Application FrontEnd.

## Required files for AppFront Deployment

At a minimum, manifest.json, index.html and xs-app.json should be present to prepare an application for deployment to App FrontEnd. Please see detailed instructions here https://community.sap.com/t5/technology-blog-posts-by-sap/simple-ui-applications-with-application-frontend-service/ba-p/14096009.
Though we have a simple SAPUI5 application with no data from the backend, we have the configuration required to extend this application to enable data binding, so you may see more than necessary configuration in the mta.yaml, ui5-deploy.yaml and xs-app.json files.

## Run locally

```
    ui5 serve -o index.html

```

http://localhost:8080/index.html

## Deploy to Cloud Foundry

1. Add mta.yaml with app-frontend service configuration
2. create ui5-deploy.yaml file
3. Run `mbt build`
4. cf deploy mta_archives/<mtarfile>
5. The application is deployed and available under BTP Cockpit -> HTML5 -> Application Frontend
