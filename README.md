\# ReqRes API Testing Project



!\[API Tests](https://github.com/coder-ankii/reqres-api-testing/actions/workflows/api-tests.yml/badge.svg)



\## 📌 About the Project

A complete API testing project built using \*\*Postman\*\* and \*\*Newman\*\* with a fully automated \*\*CI/CD pipeline\*\* using GitHub Actions.



The project tests the \[ReqRes REST API](https://reqres.in/) covering all CRUD operations with assertions on every request.



\---



\## 🛠️ Tools \& Technologies

\- \*\*Postman\*\* — API test creation and manual execution

\- \*\*Newman\*\* — Command line collection runner

\- \*\*Newman HTML Extra\*\* — Beautiful HTML test reports

\- \*\*GitHub Actions\*\* — CI/CD pipeline for automated test execution



\---



\## 📁 Project Structure

reqres-api-testing/

├── collections/

│   └── ReqRes API Tests.postman\_collection.json

├── environments/

│   └── ReqRes Dev.postman\_environment.json

├── reports/

│   └── report.html

└── .github/

└── workflows/

└── api-tests.yml

\---



\## 🧪 Test Coverage



| Request | Method | Status Code | Assertions |

|---|---|---|---|

| Get All Users | GET | 200 | 3 |

| Get Single User | GET | 200 | 3 |

| Create User | POST | 201 | 3 |

| Update User | PUT | 200 | 3 |

| Delete User | DELETE | 204 | 2 |



\*\*Total: 5 requests | 14 assertions\*\*



\---



\## ▶️ How to Run Locally



\### Prerequisites

\- \[Node.js](https://nodejs.org/) installed

\- Newman installed globally



\### Install Newman

```bash

npm install -g newman

npm install -g newman-reporter-htmlextra



\### Run Tests

newman run collections/"ReqRes API Tests.postman\_collection.json" \\

\-e environments/"ReqRes Dev.postman\_environment.json" \\

\-r htmlextra \\

\--reporter-htmlextra-export reports/report.html



\## ⚙️ CI/CD Pipeline

This project uses GitHub Actions to automatically run the test suite on every push to the master branch.

The pipeline:

1\. Sets up Node.js environment

2\. Installs Newman and HTML reporter

3\. Runs the full Postman collection

4\. Uploads HTML report as an artifact



\## 📊 Sample Test Results

\- ✅ 5 requests executed

\- ✅ 14 assertions passed

\- ✅ 0 failures

