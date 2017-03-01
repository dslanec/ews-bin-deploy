# New Relic - Openshift v3 Java Proof of Concept
An Assemble script for Openshift v3 (Source 2 image) which deploys a sample java application on JBoss EWS 8 and instruments the application with the latest version of the New Relic Java agent.  More details on Source 2 image (S2I) and other Openshift deployment strategies can be found [here](https://blog.openshift.com/binary-deployments-openshift-3/).

## Installation Instructions
1. [Ensure the OC command is installed on your machine](https://docs.openshift.com/enterprise/3.1/cli_reference/get_started_cli.html)
2. Clone this repository with ```git clone https://github.com/dslanec/ews-bin-deploy.git```
3. In the assemble script on line 86 replace "LICENSE_KEY" with your New Relic License Key
4. On line 87 replace APPLICATION_NAME with the name the application should report to New Relic with
5. Add the .sti directory to the root of a new git repository and perform a commit
6. run ``` oc new-app jboss-webserver30-tomcat8-openshift~https://github.com/<USERNAME>/<REPOSITORY>.git --name=petstore ``` to deploy the application (replace USERNAME and REPOSITORY with your relevant details).
