---
title: "Proposal"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference only. Please **do not copy it verbatim** for your report, including this warning.
{{% /notice %}}

In this section, you need to summarize the contents of the workshop that you **intend** to conduct.

# Cloud Racket Platform

### 1. Executive Summary  
The Badminton Court Finder Platform is designed to help badminton players in Ho Chi Minh City easily search for courts, book them, and manage schedules in real-time. The application is built entirely on a serverless AWS architecture, integrating technologies such as personalized AI recommendations, sentiment analysis of user reviews, and mapping of nearby courts via Google API, while also supporting monthly revenue statistics for court owners.

### 2. Problem Statement  
*Current Problem*  
Currently, finding and booking badminton courts mainly relies on manual contact (phone or social media). Court schedules are not updated in real-time and court coverage is limited, making it difficult to estimate travel distance. Court owners also face challenges managing the number of courts and revenue reporting inefficiently.

*Solution*  
This website provides an automated process for searching, booking, and efficient management for business owners. Users can search for courts near their location via Amazon Location Service, view real-time court availability in Amazon DynamoDB, and receive personalized court recommendations through Amazon Personalize. Court owners can register and update court information, receive booking confirmation emails via Amazon SES, and view revenue statistics through a Custom Dashboard built with AWS Amplify, Lambda, and Chart.js using data from DynamoDB/S3. The web interface is deployed via AWS Amplify, and user management is handled through Amazon Cognito.

*Benefits and ROI*  
  * **For players:** Easily find and book suitable courts within seconds, receive personalized recommendations based on behavior and location, and automatically receive confirmation emails. Search time is reduced by 90% (from 30 minutes to 3 minutes), and booking confirmation time is shortened from 2–24 hours to only 5 minutes.  
  * **For court owners:** Automatically manage courts, schedules, and bookings via a central dashboard, reducing manual operations by 80%. The system provides visual reports of revenue, bookings, and average ratings to support data-driven decision making.  
  * **For the development team:** Fully serverless system, extremely low operating cost (<$1/month in the initial phase, estimated $8–15/month after Free Tier). The system is both a practical solution and a valuable learning environment providing real data for AI, Vietnamese NLP, and recommendation model research.

### 3. Solution Architecture  
The platform uses a serverless AWS architecture for stable operation, easy scalability, and cost efficiency. Data about users, courts, and bookings is stored in Amazon DynamoDB. Components communicate via Amazon API Gateway and AWS Lambda functions. The web and mobile interface is deployed via AWS Amplify, while Amazon Cognito ensures secure access control. Amazon Personalize recommends courts based on user history and Amazon Comprehend considers reviews and ratings, while the Custom Dashboard visualizes activity data for court owners and users. All operations are monitored via Amazon CloudWatch and automated with Amazon EventBridge.  

![Cloud Racket Platform Architecture](/images/2-Proposal/proposal_badminton.jpg)

*AWS Services Used*  
- *AWS Amplify Hosting*: Host and deploy web/mobile applications.  
- *Amazon API Gateway*: Communication between client and backend.  
- *AWS Lambda*: Handle business logic and connect AWS services.  
- *Amazon DynamoDB*: Store user, court, and booking information.  
- *Amazon Cognito*: Authenticate and authorize users.  
- *Amazon SES*: Send confirmation emails and notifications automatically.  
- *Amazon S3*: Store court images and analytical data.  
- *Amazon Personalize*: Provide personalized court recommendations.  
- *Amazon Comprehend* (Optional): Analyze sentiment in Vietnamese reviews to supplement overall ratings.  
- *Amazon Location Service + DynamoDB GeoLib*: Find courts near the user’s location.  
- *Custom Dashboard*: Visualize data and analyze reports via a custom dashboard built with AWS Amplify, AWS Lambda, and Chart.js from data stored in DynamoDB or S3.  
- *Amplify Admin UI (Admin Portal)*: Manage CRUD operations for courts, moderate reviews, and monitor logs.  
- *Amplify CI/CD*: Automatically deploy and update the system.  
- *Amazon CloudWatch*: Monitor logs, performance, and alerts.  
- *Amazon EventBridge (Scheduler)*: Automate notifications and clean up data.  
- *AWS IAM + WAF*: Manage security, encrypt data, and prevent web attacks.  
- *User Module*: Amazon Cognito manages registration, login, and user profiles; player data, booking history, and favorite courts are stored in DynamoDB.  
- *Court Module*: Court owners add or edit court information and images; court data is stored in DynamoDB, images in S3; status updates handled via API Gateway + Lambda.  
- *Booking Flow*: API Gateway → Lambda → DynamoDB → SES handles bookings, checks for conflicts, and sends automatic confirmation emails.  
- *Recommendation System*: Amazon Personalize analyzes user behavior and ratings to provide court recommendations; Lambda queries results based on 70% behavior + 30% rating model.  
- *Geo Search*: DynamoDB Geo Library or Amazon Location Service finds courts near the player; integrates Google Maps for navigation.  
- *Admin Dashboard*: Custom dashboard shows revenue, bookings, and ratings, built with AWS Amplify and Chart.js using aggregated data from DynamoDB or S3 via AWS Lambda.  
- *Automation Layer*: EventBridge triggers Lambda periodically to send reminders, retrain Personalize, and clean up old data.  

### 4. Technical Implementation  
*Project Phases*  
The project is divided into 4 main phases:  
1. *Research & Architecture*: Draw AWS Serverless system diagram, define booking workflow and data flow (Week 1).  
2. *Development & Testing*: Build API Gateway + Lambda, integrate DynamoDB and Cognito, perform functional testing (Weeks 2–3).  
3. *Analysis*: Add recommendations from Personalize, display data via Dashboard (Week 4).  
4. *Deployment & Optimization*: Use Amplify CI/CD for automated deployment, set up CloudWatch and EventBridge for monitoring (Week 5).  

*Technical Requirements*  
- *Frontend*: ReactJS / Next.js (AWS Amplify Hosting)  
- *Backend*: AWS Lambda (Node.js or Python) + Amazon API Gateway  
- *Database*: Amazon DynamoDB (store users, courts, bookings, ratings; supports Geo queries via DynamoDB Geo Library or AWS Location Service)  
- *AI Integration*: Amazon Personalize (analyze behavior and ratings to recommend courts)  
- *Auth & Security*: Amazon Cognito (login/authentication), AWS IAM (permissions), AWS WAF (web attack protection)  
- *Email*: Amazon SES (booking confirmation, notifications, automatic reminders)  
- *Analytics*: Custom Dashboard (visualize revenue, bookings, ratings from DynamoDB or S3 via AWS Amplify + Lambda + Chart.js)  
- *Automation*: Amazon EventBridge (Scheduler) automates reminders, updates recommendations, cleans old data  
- *Maps API*: AWS Location Service or Google Maps / Places / Distance Matrix (find nearby courts, show maps and directions)  

### 5. Timeline & Milestones  
- *Project Duration*: 3 months (internship phase)  

- **Month 1 – Research & Preparation**  
  - Research AWS services (Amplify, Lambda, DynamoDB, Personalize, SES, Location Service)  
  - Set up development environment and hardware  

- **Month 2 – System Design & Architecture**  
  - Design overall architecture and define main modules  
  - Develop API schemas, user roles (Cognito), and CI/CD pipeline  
  - Prepare sample datasets for Personalize and DynamoDB  

- **Month 3 – Implementation & Deployment**  
  - Week 1: Finalize architecture, define DynamoDB schema, deploy API Gateway + Lambda  
  - Week 2: Develop backend and frontend (ReactJS/Next.js + Amplify Hosting)  
  - Week 3: Integrate Amazon Personalize, SES, and Location Service  
  - Week 4: Test, optimize performance, and fully deploy on AWS Amplify  

### 6. Budget Estimation  

*Infrastructure Costs*  
- AWS Amplify Hosting: Free Tier: 500 build minutes, 5 GB hosting. After Free Tier: ~$0.01/min × 500 = $5.00/month  
- AWS Lambda: $0.00/month (20,000 requests/day, 128 MB, avg 200 ms)  
- Amazon API Gateway: $0.00/month (600,000 requests/month within Free Tier)  
- Amazon DynamoDB: $0.00/month (5 GB data, 100K read/write per day)  
- Amazon S3 (Images): $0.12/month (10 GB storage, 5,000 GET/PUT requests)  
- Amazon SES (Email): $0.00/month (2,000 emails/month Free Tier)  
- Amazon Personalize: Free 2 months (20 GB data, 5M interactions). After that: ~$8/month for batch inference (small data + weekly retraining)  
- Custom Dashboard (Amplify + Chart.js): $0.00/month  
- Amazon Location Service: $0.00/month (10,000 map requests, 1,000 location requests)  
- Amazon EventBridge (Scheduler): $0.00/month (10 rules triggers/day/hour)  
- AWS IAM + WAF: $0.00/month (basic auth, encryption, security)  

*Total*: $0.7/month, $8.40/12 months  
- Month 1: $0.12/month (all within Free Tier)  
- Month 2: $5.12/month (Personalize still Free Tier, Amplify starts charging)  
- After Free Tier: $13.12/month ≈ $157.44/year  

### 7. Risk Assessment  
*Risk Matrix*  
- Internet outage: Medium impact, medium probability  
- Unauthorized access: High impact, low probability  
- Budget overrun: Low impact, low probability  
- AI recommendation errors: Medium impact, low probability  

*Mitigation Strategies*  
- Network: Auto retry when connection lost  
- Security: MFA via Cognito, WAF blocks attacks  
- Costs: Alerts via AWS Budgets, optimize query frequency  
- AI: Monitor and periodically retrain Personalize model  

*Contingency Plan*  
- Allow temporary offline bookings and sync when network is available  
- Rollback CodePipeline if deployment fails or costs exceed estimates  

### 8. Expected Outcomes  
*Technical Improvement*: The application provides real-time court search and booking, personalized recommendations, and visual reports to optimize operations for players and court owners.  
*Long-term Value*: The platform can expand to other sports (tennis, basketball, gyms) and serve as a blueprint for smart sports solutions using AWS Serverless and AI. It is also an ideal practical project for students or research teams applying AWS to develop intelligent systems.