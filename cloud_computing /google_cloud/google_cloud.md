# Google Cloud

## Google Cloud support:
### Compute:
  - **Google App Engine**: (A platform for building scalable web apps and mobile backends) - https://cloud.google.com/appengine
  - **Google Compute Engine**: (Run large-scale workloads on virtual machines hosted on Google's infrastructure) - https://cloud.google.com/compute

### Storage and Databases
  - **Google Cloud Storage**  - https://cloud.google.com/storage
  - **Google Cloud Datastore** (A managed, NoSQL, schemaless database for storing non-relational data)https://cloud.google.com/datastore
  - **Google Cloud SQL** Store and manage data using a fully-managed, relational MySQL database - https://cloud.google.com/sql
  
### ...................

## Google Cloud SDK
- https://cloud.google.com/sdk/docs/
- **Google Cloud SDK** is a set of tools that you can use to manage resources and applications hosted on Google Cloud Platform.
- These tools include:
  - **gcloud** command-line tool
  - **gsutil**
  - **bq**

## gcloud
- **gcloud** is a part of the **Google Cloud SDK**
- **gcloud** is a tool that provides the primary command-line interface to Google Cloud Platform
- For example, you can use gcloud to create and manage:
  - **Google Compute Engine** virtual machine instances and other resources
  - **Google Cloud SQL instances**
  - **Google Cloud Deployment manager deployments** (use gcloud to **deploy App Engine applications** and perform other tasks).
  
##Setup gcloud at first time.
  ```sh
    # Login in the Google Cloud Account
    gcloud auth login
    
    # Setup Account, Project
    gcloud init
  ```
  
- Choose the account.
- Pick cloud project.
  
## gcloud CLI
 - https://cloud.google.com/sdk/gcloud/reference/
 
 - **gcloud info** : Show all infimations of this Google Cloud
  ```
  Account: [minhtuan.techno@gmail.com]
  Project: [tuanminhle1992]
  
  Current Properties:
    [core]
      project: [tuanminhle1992]
      account: [minhtuan.techno@gmail.com]
      disable_usage_reporting: [False]
    [app]
      suppress_change_warning: [true]
    [compute]
      region: [asia-east1]
      zone: [asia-east1-a]
  ```

 - **gcloud config**
    ```sh
      # Show current account, project
      gcloud config list

      # Change current App engine project
      gcloud config set project [PROJECT_ID]
      
      # The file config is: /Users/leminhtuan/.config/gcloud/configurations/config_default
    ```
 
 - **gcloud app**: Manage your App Engine app. - Manager only 1 project GAE
    ```sh
      gcloud app versions list
    ```
 - **gcloud compute**: Read and manipulate Google Compute Engine resources.
    ```sh
      gcloud compute instances list
    ```
 
 - **gcloud projects**: Manage your projects. Manage all GAE of your Account
    ```sh
      gcloud projects list
    ```
 
 - **gcloud sql**: Manage Cloud SQL databases.

# Google Cloud SDK VS Google App Engine SDK (GAE)

##Google Cloud CLI:
  - gcloud
  - gsutil
  - bq
  
## Google App Engine CLI
  - dev_appserver.sh    //Run Jetty (Java Web Servlet Container ~ Tomcat) - run **war** folder
  - appcfg.sh           // Deploy **war** folder to **Google App Engile**
  - google_sql.sh
  - run_java
  - endpoints.sh

## gcloud VS appcfg.sh

### Get list of versions
- **appcfg.sh** list version of project
  ```sh
    cd path/to/GAE/project
    appcfg.sh -A [PROJECT_ID] list_versions war
    
    #=> return all version of this project
  ```
  
- **gcloud** list version of project
  ```sh
    gcloud app versions list
      
    #=>  return all version of curent project
  ```
  
### Change default version
- **appcfg.sh** change default version of a GAE project
  ```sh
      appcfg.sh -A [APP_ID] -V [VERSION] --enable_jar_splitting set_default_version war
  ```
  
- **gcloud** change default version of a GAE project
  ```sh
      gcloud preview app modules set-default default --version=[VERSION_NAME]
  ```
  
### Deploy app to GAE
  
- ***appcfg.sh* deploy war folder to GAE
  
  ```sh
      appcfg.sh -A [PROJECT_ID] -V [VERSION_NAME] --enable_jar_splitting set_default_version war
  ```
