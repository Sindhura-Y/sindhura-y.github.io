# Career Progression Assessment Portfolio - Sindhura Yalamanchili

**```About me```**

---

**```ISMs i resonate with the most```**


---

**```Next steps```**

Currently being mentored by Jeffrey Pryciak on Architecting new systems and solving existing problems in our systems.

---

## Project 1 - Rocket Mortgage Servicing API


<br/>

**```Description:```**
    
<i>A backend-for-frontend for client facing servicing systems.</i>
  
  - [Apphub](https://applications.apphub.rockettech.tools/application/201864#code)
  - [Git Repository](https://git.rockfin.com/myql-servicing/servicing-api)
  - Technologies Used: .Net core 3.1, API Gateway, Lambda, ECS, RDS Aurora, S3, Redis Cache


<br/>

**```Highlights:```**

<br/>

<details>
        <summary><b>Survey Widget</b></summary>
        <i>This is a module on the RMS dashboard that aids in gathering client’s financial intentions.</i>

  - <b>My Contributions:</b>
      -  Proposed and engineered the solution with an RDS Aurora, Lambda and an S3 bucket.
      -  Trained engineers on connecting to an AWS database using SSH since this is the first database RMS owned.
      - <p align="left">
            <a>
                <img src="./screenshots/surveywidget.png" style="width:400px;"/>
            </a>
        </p>
  
    - Business Outcomes:
      - Provided an increased quality of lead, closed loan volume and improve our retention Rate. Business estimated this will result in 225 Million in closed loan volume per yearly and the quality of the leads generated close at 78% or better.

   - Relevant Documentation and Pull Requests:
      - <b>[Survey Widget Analysis](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/MQLS/docs/LEGACY%20Feature_Story%20Documentation/2019%20Features/RMS%20Survey%20Widget%20Analysis%20(Draft).md)</b>
      - <b>[Survey Widget Database](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/MQLS/docs/LEGACY%20Feature_Story%20Documentation/2019%20Features/RMS%20Survey%20Widget%20-%20Database%20Schema/index.md)</b>
      - <b>[Quget Package](https://git.rockfin.com/Servicing/data-access-layer)</b>
      - <b>[RMS API PR](https://git.rockfin.com/myql-servicing/servicing-api/pull/1136)</b>
</details>

<br/>

<details>
        <summary><b>Cache Utility</b></summary>
    <i>RMS calls Viper API, that has a shared database for every single read & write for payment information. With the steady increase in volume, Viper Database is becoming overloaded, and in sudden bursts of volume we started to experience issues and time outs. We stabilized payments by adding caching, migrating parts of the loan data collection to Servicing Data Mart API (SDM), and optimizing the SDM calls. Fixing this in RMS API, also helped reduce the calls to all of our downstream legacy systems.</i>

  - <b>My Contributions:</b>
      - Contributed to Quget package owned by Midware to fix a cache availability bug.
      - Made respective changes to Quget packages and services owned by RMS.
        - <p align="left">
            <a>
                <img src="./screenshots/amaze_cacheutilityfix.png" style="width:400px;"/>
            </a>
        </p>

  - Business Outcomes:
      - Reduced our chances of taking Viper down that helped better client experience with scheduling and managing payments.

  - Relevant Pull Requests:
      - <b>[Quget Package](https://git.rockfin.com/Rocket-Mortgage-Midware/CacheUtility/pull/7)</b>
      - <b>[Quget Package](https://git.rockfin.com/myql-servicing/RMSCommon/pull/25)</b>
      - <b>[RMS API](https://git.rockfin.com/myql-servicing/servicing-api/pull/1305)</b>
</details>

<br/>
  
<details>
        <summary><b>RMS API Breakdown</b></summary>
  <i>In Its current state RMS is a monolith with layers that mix their purposes. In order to get to our desired state a phased approach of preparing RMS API to be seperated must be taken before moving on to eventually breaking up the API. The end state must result in isolated API's, using small subset of shared code from a singular shared package, running on a K8 cluster</i>
    
  - <b>My Contributions:</b>
    - Technical Lead
    - Working with Product owners to create work items to account for the breakdown.

  - Relevant Pull Requests:
        - <b>[Feature Documentation](https://git.rockfin.com/Servicing/SP-Documentation/blob/master/docs/Engineering/Features/RMS%20API%20Breakout/FeatureSpecs.md)</b>
        - <b>[RMS API PR](https://git.rockfin.com/myql-servicing/servicing-api/pull/1855)</b> 
</details>

<br/>
  
<details>
    <summary><b>Rocket Homes:</b></summary>
    <i>This is a module on the dashboard that provides clients with their neighbourhood trend report.</i>
  
   - <b>My Contributions:</b>
       -  Acted as a lead in driving the conversations with Product Owners in RMS, Rocket Homes' Team Leader and Engineers on Data Contract alignment.
       - Worked extensively with Quality Engineers for integration testing.
 
   -  Business Value:
       - Rocket Home Location Trend Data in RMS for our Serviced Clients will achieve an increase in client engagement on the website, increase client satisfaction and provide valuable insights for future Servicing retention opportunities.
       - <b>[Design](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/MQLS/docs/LEGACY%20Feature_Story%20Documentation/2019%20Features/Rocket%20Homes%20-%20Home%20Page%20Module/Content%20and%20Design%20for%20Rocket%20Homes.md)</b>
    
   - Relevant Documentation and Pull Requests:
      - <b>[Data Contract](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/MQLS/docs/LEGACY%20Feature_Story%20Documentation/2019%20Features/Rocket%20Homes%20-%20Home%20Page%20Module/Data%20Contract%20-%20Rocket%20Homes%20(deprecated)%20-%20RMS%20API.md)</b>

</details>   
  <br/> 

---

## Project 2 - Rocket Mortgage Servicing Web

<br/>

**```Description:```**

<i>A frontend for rocket mortgage servicing clients.</i>
  
  - [Apphub](https://applications.apphub.rockettech.tools/application/203001#code)
  - [Git Repository](https://git.rockfin.com/myql-servicing/servicing-web)
  - Technologies Used: Angular, Express.js Proxy, Spark Design, Jasmine
</details>

<br/>

**```Highlights:```**

<br/>

<details>
    <summary><b>Proxy Modernization</b></summary>
<i>The existing node proxy that is in RMS was never intended to be a long lived solution. It was assumed/theorized that the proxy was not even needed. Thus no attention was ever really given to the structure or ease of use. Time has proven to us that the proxy is needed and in its current statement is untenable. It is convoluted and not engineered for growth or development teams or support. In order for RMS to move into the future, the proxy must be reimagined.</i>

  - <b>My Contributions:</b>
    -  Collaborated with Train SRE to re-write the proxy to reduce the complexity of integrating with multiple back-end services. 
    - <p align="left">
        <a>
            <img src="./screenshots/amaze_proxy.png" style="width:400px;"/>
        </a>
        </p>
  
  - Business Outcomes:
      - Reduce the complexity of adding new resources to all RMS API suites, thus reducing time to implement while increasing the ability to troubleshoot problems.

   - Relevant Documentation and Pull Requests:
        - <b>[Readme](https://git.rockfin.com/myql-servicing/servicing-web/blob/master/express-server/README.md)</b>
        - <b>[Pull Request](https://git.rockfin.com/myql-servicing/servicing-web/pull/2401)</b>
 </details>

<br/>

<details>
    <summary><b>Refinance calculator</b></summary>
  <i>A runtime injectable microfront end.</i>
  
  - <b>MyContributions</b>
      - Created a landing page for calculators.
      - <p align="left">
        <a>
        <img src="./screenshots/amaze_mfeweb.png" style="width:400px;"/>
        </a>
      </p>
  
  - Business Outcomes
      - To provide clients with additional details around their home financing. Additionally, this is a source of understanding what the clients goals are in terms of refinancing or purchasing when they enter go to start an application by passing along all the information from the calculator into the application process to streamline it for both client and banker

      - <p align="left">
            <a>
                <img src="./screenshots/refinancecalculator.png" style="width:400px;"/>
            </a>
        </p>

   - Relevant Documentation and Pull Requests
        - <b>[Documentation](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/ITServicingArchitecture/docs/R5%202020%20Solution%20Architecture/RMS%20Features%20for%20R5/1823776%20-%20Refinance%20Calculator%20and%20Calculator%20Page_%20RMS.md)</b>
        - <b>[Pull Request](https://git.rockfin.com/myql-servicing/servicing-web/pull/2096)</b>
</details> 
<br/>

<details>
    <summary><b>Spark design upgrades in accordance with business needs</b></summary>
<i>Spark design system upgrades to improve accessibility for our special clients.</i>
  
  - <b>My Contributions:</b>
      - Collaborated with Spark Design System team to update the package and write custom CSS to mees business requirements for better client experience. 

  - Business Outcomes:
      - Improves accessibility, design and development efficiencies and overall Rocket brand health.
  
 - Relevant Documentation and Pull Requests:
      - <b>[EPIC](https://tfs.rockfin.com/QL/IT/_workitems/edit/2228945)</b>
      - <b>[Pull Request](https://git.rockfin.com/myql-servicing/servicing-web/pull/2330)</b>
</details>  
<br/>

<details>
    <summary><b>Adobe target - Banners</b></summary>
<i>Banners to notify clients </i>
  
  - <b>My Contributions:</b>
      - Created banners to inject into RMS UI through adobe target to notify clients about maintenance, natural disaster support and loan acquisition details. 
      - <p align="left">
            <a>
            <img src="./screenshots/amaze_adobebanner.png" style="width:400px;"/>
            </a>
        </p>

  - Business Outcomes:
      - Better client experience and less calls to Client Relations for acquisition loans from Mr.Cooper. 

 - Relevant Documentation and Pull Requests:
      - <b>[ADS Story](https://tfs.rockfin.com/QL/IT/_workitems/edit/2776486)</b>
      - <b>[API Pull Request](https://git.rockfin.com/myql-servicing/servicing-api/pull/1769)</b>
      - <b>[Web Pull request](https://git.rockfin.com/myql-servicing/servicing-web/pull/3015)</b>
</details>

<br/>

---

## Project 3 - Viper

<br/>

**```Description:```**

<i>A backend for payments that integrates with our vendor MSP (Mortgage Servicing Platforms).</i>

  - [Apphub](https://applications.apphub.rockettech.tools/application/201336#code)
  - [API, Listener Git Repository](https://git.rockfin.com/Servicing/viper)
  - [Database Git Repository](https://git.rockfin.com/Servicing/ViperDB)
  - Technologies Used: .Net Framework, ADO.Net, SQL Server, UM Queues 

<br/>

**```Highlights:```**

<br/>

<details>
    <summary><b>Privacy By Design</b></summary>
<i>Automate the process of right to delete to comply with new CCPA(California Consumer Privacy Act) law. </i>

  - <b>My Contributions:</b>
      - Collaborated with multiple teams on architecting the solution and implementing it.
      - Collaborated with Nexus for UM Queue creation and troubleshooting issues. 
  
  - Business Outcomes:
      - Log, track and enforce consumer consent for data sharing and to protect client data and comply with regulations. 
      - <i>solution screenshot</i>

 - Relevant Documentation and Pull Requests:
      - <b>[ADS Feature](https://tfs.rockfin.com/QL/IT/_workitems/edit/1772949)</b>
      - <b>[API PR](https://git.rockfin.com/Servicing/viper/pull/835)</b>

</details>

<br/>

---

## Project 4 - Loan Client Settings Service

<br/>

**```Description:```**

<i>Tech enablement to decouple from MyQL Midware and move to cloud-based services.</i>

  - [Apphub](https://applications.apphub.rockettech.tools/application/208453)
  - [API Git Repository](https://git.rockfin.com/Servicing/208453-loan-client-settings-service)
  - [Lambda Git Repository](https://git.rockfin.com/Servicing/208501-loan-client-settings-sender-lambda)
  - Technologies Used: .Net Core 3.1, DynamoDB, AWS SQS, Lambda, ECS Fargate 

<br/>

**```Highlights:```**

<br/>

<details>
    <summary><b>Contributions</b></summary>

- Technical Lead
- Paired up with Train Architect to solution the decouple
- Led the conversations with multiple teams (Current Loan Services for Welcome Experience 2.0, SIP team for the flow of qtweets to downstream systems like Panorama).
- Collaborated with Database Engineers from Servicing and RMO to backfill the new database with the data from Midware.
- <p align="left">
    <a>
    <img src="./screenshots/amaze_lcss2.png" style="width:400px;"/>
    </a>
  </p>

    - Business Outcomes:
      - Eliminate the risk in a single point of failure between RMO and RMS for servicing related client information. 
      - <p align="left">
            <a>
            <img src="./screenshots/loanclientsettingsservice.png" style="width:400px;"/>
            </a>
        </p>

   - Relevant Documentation and Pull Requests
        - <b>[AD Feature](https://tfs.rockfin.com/QL/IT/_workitems/edit/2351845)</b>
        - <b>[Architecture](https://editor.signavio.com/p/hub-preview#/model/e8e01b2b080f4620927c640565a64e4a)</b>
        - <b>[Overview](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/main/MQLS/docs/RMS%20Teams/Pandapool/Loan%20Client%20Settings%20Service/index.md)</b>
        - <b>[Database IAC Pull Request](https://git.rockfin.com/Servicing/208453-loan-client-settings-service/pull/3)</b>
        - <b>[API Pull Request](https://git.rockfin.com/Servicing/208453-loan-client-settings-service/pull/16)</b>

</details>

<br/>

---

## Project 5 - Client Data Service

<br/>

**```Description:```**

<i>placeholder</i>

  - [Service Apphub](https://applications.apphub.rockettech.tools/application/208815)</b>
  - [Lambda Apphub](https://applications.apphub.rockettech.tools/application/207989)</b>
  - [API Git Repository](https://git.rockfin.com/Servicing/208453-loan-client-settings-service)</b>
  - [Lambda Git Repository](https://git.rockfin.com/Servicing/ViperDB)</b>
  - Technologies Used: .Net Core 3.1, AWS RDS, AWS SQS, Lambda, ECS Fargate

<br/>


**```Highlights:```**

<br/>

<details>
    <summary><b>Contributions</b></summary>

- Company Wide Initiative:
    -  <i>Talk to Andrea</i>
  
    - Business Outcomes 
      - <i>Talk to Andrea</i>

   - Relevant Documentation and Pull Requests
        - <b>[Architecture Diagram](https://editor.signavio.com/p/editor?id=27b2524ac41344a2940fb4d46f41580c)</b>
        - <b>[Service PR](https://git.rockfin.com/Servicing/Client-Data-Service/pull/242)</b>
        - <b>[Lambda PR](https://git.rockfin.com/Servicing/208815-client-identifier-processor-lambda/pull/38)</b>

</details>

<br/>

---

## Project 6 - Rocket Credit API
<br/>

**```Description:```**

<i>Credit monitoring for Rocket Mortgage Servicing Clients.</i>

  - [API Apphub](https://applications.apphub.rockettech.tools/application/209456)</b>
  - [Database Apphub](https://applications.apphub.rockettech.tools/application/209523)</b>
  - [API Git Repository](https://git.rockfin.com/myql-servicing/Rocket-Credit-Consumer-API)</b>
  - [Database Git Repository](https://git.rockfin.com/myql-servicing/rocket-credit-consumer-db)</b>
  - Technologies Used: .Net Core 3.1, AWS RDS, AWS SQS, Lambda, ECS Fargate

<br/>


**```Highlights:```**

<br/>

<details>
    <summary><b>Contributions</b></summary>

- Acted as a Technical Lead on the Epic
- Paired up with our train architect and Staff engineer to help design the technical work.
- Collaborated with Train SRE team to deploy the application to EKS.
  
    - Business Outcomes 
      - <i>Keeping clients engaged in Rocket products by allowing credit monitoring</i>

   - Relevant Documentation and Pull Requests
        - <b>[Architecture Diagrams](https://editor.signavio.com/p/explorer#/directory/479c91b4fa3744fe89e3e5ea171e8fac)</b>
        - <b>[EKS Pull Request](https://git.rockfin.com/myql-servicing/Rocket-Credit-Consumer-API/pull/10)</b>

</details>

<br/>

---

## Project 7 - Product Monitoring Lambdas

<br/>

**```Description:```**

<i>Automates the check-in process for forbearance clients.</i>

  - [Apphub](https://applications.apphub.rockettech.tools/application/206845)</b>
  - [API Git Repository](https://git.rockfin.com/default-loan-services/product-monitoring-audit)</b>
  - Technologies Used: .Net Core 3.1, AWS SNS, AWS SQS, Lambda, RDS Aurora

<br/>

**```Highlights:```**

<br/>

<details>
    <summary><b>Contributions</b></summary>

- Led the conversations with Senior engineer from Default Loan Services and multiple teams on RMS to help design the work.
- Collaborated with Database team to backfill the database, troubleshoot and fix the issues after GoLive.
- <p align="left">
    <a>
        <img src="./screenshots/amaze_dlscovid.png" style="width:400px;"/>
    </a>
    </p>
  
    - Business Outcomes 
      - Reduced calls to Client Relations
      - Improved RMS experience for forbearance clients during COVID-19.

   - Relevant Documentation and Pull Requests
        - <b>[Architecture Diagrams](https://git.rockfin.com/Servicing/SPLegacyConfluenceDocs/blob/5b43f09356b1dc45c9cddf3fbe3bed690826d44b/ITServicingArchitecture/docs/R2%202020%20Solution%20Architecture/Solution%20Architecture%20Documents%20R2%202020/DLS%20Features/Product%20Monitoring.md)</b>
        - <b>[Pull Request](https://git.rockfin.com/default-loan-services/product-monitoring-audit/pull/4)</b>

</details>

<br/>

---

## Technical Achievements

<br/>

**```Sev-1 Auth0 cert issue```**

[Blameless Incident Report](https://git.rockfin.com/RockCentral-Post-Incident-Process/Blameless-Incident-Reports/blob/8de5c8f23b16015dcd6da8ae32a8038235246d08/36852_201864_-_PROD_-_Rocket_Mortgage_Servicing_API_Multiple_Applications_Having_C_09302021.md)

[PagerDuty Incident](https://rockcentraldetroit.pagerduty.com/incidents/P0EF57N)

The root certificate authority expired and caused a widespread outage across Rocket Mortgage Technology. This took down Rocket Mortgage Servicing and impacted client experience. All the other backend services except Loan Client Settings Service(LCSS) and Client Data Service(CDS) were behind ping and these two were the only two services utilizing auth0 for authentication. When we built these systems and integrated them with our UI, we put them behind a feature flag in Split.IO. By turning these flags off, we were able to bring the site back up for clients with all the functionality except for the settings page. This was a huge win considering the Tech Incident(TI) went on for almost about two days.

<p align="left">
    <a>
        <img src="./screenshots/amaze_sev1.png" style="width:400px;"/>
    </a>
</p>

<br/>

**```Cache Availability Fix```**

During the pandemic, we were seeing increased traffic to RMS. This was causing issues to some of our legacy downstream applications. I was approached by my team leader to look into Caching some of the response so we reduce the calls to these systems. We were using a quget package to write to redis cache. I found a bug in the package that caused failed writes to the cache when it's unavailable and reached out to the team that owned the package and contributed to the bug fix. I collaborated with my Senior engineer to make the changes in the services we owned to properly log the writes to the cache. This helped us reduce the down time for our downstream legacy systems during high traffic.

<br/>

**```COVID-19: Forbearance Auto-Extension```** 

A few months into the pandemic, Client relations was overloaded with calls from clients regarding forbearance. Our partner, Default Loan Services(DLS) reached out to RMS to build some products to automate the forbearance check-in for clients. RMS went all in. We were provided with business requirements and i led the conversations between multiple teams both on RMS, DLS and the database team to design a robust solution. Even after we went live with the solution, i kept workign with DLS and a couple of database engineers from servicing to fix the data issues by creating sql scripts.


<br/>

**```Loan Client Settings Service and Rocket Credit```**

After the proxy modernization, my team was approached by our Train Architect to build a new service as a part of the decouple from origination. Rocket Mortgage Origination aka Midware owns all the data Rocket Mortgage Servicing clients for settings. We had to decouple and unblock them from moving to cloud. I reached out to my Architect requesting to assist in architect the solution and lead the project. As a part of this, i had the opportunity to work with multiple teams on the train and was able to successfully deliver the project.

<br/>

**```FOC Initiative```**
- There is a company-wide initiative which is very critical and cannot be disclosed - 
    Architected the solution and implemented it

---

## Non-Technical Achievements

**```Train Standards and Process Improvements```**
[Production Push Process](https://git.rockfin.com/Servicing/SP-Documentation/tree/STORY-12345-ProdPushProcess/docs/Production%20Pushes/Docs)
[Git training]()

**```Mentorship```**

Intern: Darryl Brooks 
Associate Software Engineer: Benjamin Eckert
Knowledge Share Sessions for new Seniors on the train: Suman Saurav, KrishnaChaitanya Sanagapally

**```OnCall```**

Troubleshoot issues requested through Cherwell/Product Owners
Work with Engineers from various teams to resolve Technology Incidents
Assist various OnCall engineers debug OnCall issues

<p align="left">
    <a>
        <img src="./screenshots/amaze_oncall.png" style="width:400px;"/>
    </a>
</p>

**```Production Pushes```**

Actively helping current and new team members with production builds, git issues and deployments


**```Public-speaking```**

ISM of the Month presentation at RIS

Representing Rocket Innovation Studio and promoting FOC ISMs through mediums like [WeTech Alliance](https://www.wetech-alliance.com/2022/03/09/women-in-tech-spotlight-sindhura-yalamanchili/)
