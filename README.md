# Jenkins CI/CD Pipeline Project Architecture (Java Web Application)
![CompleteCICDProject!](https://lucid.app/publicSegments/view/a6ef3233-7dda-483a-a662-d8ec90395ba3/image.png)

6)  #### Configure system:    

         1) - Click on Manage Jenkins --> Global Tool Configuration
            - Go to section SonarQube servers --> **Add SonarQube **
            - Name: **SonarQube**
            - Server URL: http://REPLACE-WITH-SONARQUBE-SERVER-PRIVATE-IP:9000  (replace SonarQube with private IP here)
            - Server authentication token: select 'sonarqube-token'
            - Click on Save    

         2) - Click on Manage Jenkins --> Configure System
            - Go to section Prometheus
            - Collecting metrics period in seconds: **15**
            - Click on Save

         3) - Click on Manage Jenkins --> Configure System
            - Go to section Slack
            - Use new team subdomain & integration token credentials created in the above slack joining step
            - Workspace: **Replace with Team Subdomain value** (created above)
            - Credentials: select 'slack-token' credentials (created above) 
            - Default channel / member id: #general
            - Click on Save  

