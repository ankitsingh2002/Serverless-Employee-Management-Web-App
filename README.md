# 🚀 Serverless Employee Management Web App

A scalable, cost-effective, and 100% serverless full-stack web application built on **Amazon Web Services (AWS)**. This system enables users to seamlessly add, retrieve, and manage employee records without provisioning or managing any backend servers.

---

## 🏗️ Architecture & Workflow

1. **Frontend Hosting (Amazon S3):** Static web files (`index.html`, `script.js`, CSS) are hosted on a public Amazon S3 bucket for high availability and low-latency delivery.
2. **REST API Layer (Amazon API Gateway):** Exposes secure `GET` and `POST` RESTful endpoints with CORS enabled to handle frontend HTTP requests.
3. **Serverless Compute (AWS Lambda):**
   - `insertEmployeeData`: Processes incoming `POST` requests to validate and store new employee details.
   - `getEmployee`: Handles `GET` requests to fetch employee records from the database.
4. **NoSQL Database (Amazon DynamoDB):** Stores employee records in the `employeeData` table using `employeeid` as the Partition Key for fast, single-digit millisecond performance.
5. **Security & Monitoring (IAM & CloudWatch):** Configured least-privilege IAM execution roles for Lambda functions and integrated CloudWatch Logs for real-time debugging and execution tracking.

---

## 🛠️ Tech Stack & AWS Services Used

- **Compute:** AWS Lambda (Python / Node.js)
- **API Management:** Amazon API Gateway (REST API, CORS)
- **Database:** Amazon DynamoDB
- **Storage & Hosting:** Amazon S3 (Static Website Hosting)
- **Security:** AWS IAM (Least-Privilege Roles & Policies)
- **Monitoring:** Amazon CloudWatch Logs
- **Frontend:** HTML5, CSS3, JavaScript (Fetch API)

---

## ✨ Key Features

- **Zero Server Management:** Fully event-driven architecture that scales automatically based on incoming traffic.
- **Pay-Per-Use Cost Model:** Eliminates idle server costs by charging only for actual API requests and Lambda execution time.
- **Secure Access Control:** Granular IAM permissions ensure Lambda functions can only access the designated DynamoDB table.
- **Real-Time Data Operations:** Instant insertion and retrieval of employee profiles via RESTful API calls.
