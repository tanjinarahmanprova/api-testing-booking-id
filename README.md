
# API Testing


## Table of content
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation and Setup](#installation-and-setup)
    - [Postman](#postman)
    - [Node.js](#node.js)
    - [Newman](#newman)
- [Project Installation Steps](#project-installation-steps)
- [API Documentation](#api-documentation)
- [Description of API calls and tests](#description-of-api-calls-and-tests)
    - [Create booking](#create-booking)
    - [Get booking Info](#get-booking-info)
    - [Token generation](#token-generation)
    - [Update booking](#update-booking)
    - [Verify updated booking info](#verify-updated-booking-info)
    - [Delete booking](#delete-booking)
    - [Verify info after deleting](#verify-info-after-deleting)
- [Report Generation](#report-generation)
    - [Process of Report Generation](#process-of-report-generation)
    - [Report of the project](#report-of-the-project)
- [Contact](#contact)

## Overview
This repository demonstrates API testing using Postman and Newman. The tests cover a range of HTTP methods, including POST, GET, DELETE, and PUT, ensuring a thorough assessment of the API's capabilities.



## Prerequisites
- [Postman](https://www.postman.com/downloads/)
- [Node.js](https://nodejs.org/en/download/package-manager)
- Newman


## Installation and Setup
### Postman
- Download [Postman](https://www.postman.com/downloads/) from the official website
- Run the installer and complete set up.
- Launch Postman and sign in
### Node.js
- Download [Node.js](https://nodejs.org/en/download/package-manager) from the official website.
- Run the installer and complete set up.
- Verify Node.js installation by running node --version in a terminal.
### Newman
- Prerequisites: Node.js
- Install Newman globally by running the following npm command in terminal
```
npm install -g newman

```
- Verify Newman installation by running newman --version in a terminal.

## Project Installation Steps
Follow these steps to set up and start using the framework

- [Fork](https://github.com/tanjinarahmanprova/api-testing-booking-id.git) the repository.
- Clone
```
git clone https://github.com/tanjinarahmanprova/api-testing-booking-id.git
```
- Import the project into postman.
- Make any desired changes or additions to the project.

## API Documentation
- [API Documentation](https://restful-booker.herokuapp.com/apidoc/index.html)
- [Postman API Documentation](https://documenter.getpostman.com/view/32325704/2sA3QmDEV6)

## Description of API calls and tests
### Create booking
POST method is used to create booking. Dynamic data is generated using Pre-request script and these dynamic data is saved in environment variables.

![create1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/17c06c2f-9253-45b2-9504-137583f0a6e1)

![create2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/8eb3c10e-6b1e-4cb9-821d-1b1a224b6b42)

## Get booking info
GET method is used to fetch booking info that was created. Some tests are performed for status code and data validation.

![get0](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/a088ff01-82cb-4caa-b48b-5a7b604b8c8d)

![get1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/9ebc14ff-ff4a-495c-ae19-64a8d413a0cd)

### Token generation
POST method is used to generate a token which will be used as authentication for updating existing data as well as deleting. The token is saved in environment variable.

![auth1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/5d7dfa40-6708-43ac-b712-e09ff72da7b7)

![auth2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/31dd8b75-f23e-41cd-b052-3d7fc7315bd8)

### Update booking
PUT method is used to update the existing booking data with new data. For update access permission, token is entered in the header. Dynamic data is generated using Pre-request script and these dynamic data replaced previous data in environment variables. Some tests are performed to verify the update.

![update1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/2d876472-2e7b-4af8-8d11-708ebda742b9)

![update2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/4ff39615-9027-431d-ae6c-f09453666865)

![update3](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/dbf99b79-5a85-4830-a859-622f0a1b209a)

### Verify updated booking info
GET method is used to fetch updated booking info. Some tests are performed for status code and data validation.

![get2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/c645a2a0-d733-4ad8-9c4a-14b799d4f87c)

![get3](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/21363208-8a88-4e6e-b6ee-4404f7694885)

### Delete booking
DELETE method is used to delete booking. For delete access permission, the token is entered in the header.

![delete1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/85f38b2a-498c-4dbd-8dce-cd9cc4848575)


### Verify info after delete
GET method is used to verify that there is no data after deleting. Some tests are performed to verify the delete.

![delete3](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/699331b7-e5bf-495a-8ad7-c0e1e750c1f5)

![delete2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/49c1058a-f147-461e-b98e-87b53c0531a5)

## Report Generation
### Process of report generation
- Install the newman reporter packages by running the following commands in terminal.
```
npm install -g newman-reporter-html
npm install -g newman-reporter-htmlextra

```
- Export collection and environment from Postman in a folder.
- Open a terminal in that folder and run the following commands to generate reports.

```
newman run CollectionName.json -e EnvironmentName.json -r cli,html
newman run CollectionName.json -e EnvironmentName.json -r cli,htmlextra

```

### Report of the project
- To generate report for this project run the following command in terminal.
```
newman run Practice.postman_collection.json -e Practice.postman_environment.json -r cli,htmlextra
```
![report1](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/bf742912-a0b4-4e12-b2f6-f55d1e2d0ee9)
![report2](https://github.com/tanjinarahmanprova/api-testing-booking-id/assets/129376867/8cf745f2-c997-423f-b76e-5ca9323e3e0c)


## Contact
For questions or feedback, please feel free to reach out:
- **GitHub**: [Tanjina Rahman](https://github.com/tanjinarahmanprova)
- **Email**: [rahmantanjina983@gmail.com](mailto:rahmantanjina983@gmail.com)
- **LinkedIn**: [Tanjina Rahman](https://www.linkedin.com/in/tanjina-rahman-a53662191/)


