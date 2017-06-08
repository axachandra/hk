[![Build Status](https://jenkins.paas.axa-asia.com/buildStatus/icon?job=HK home FE - Master)](https://jenkins.paas.axa-asia.com/job/HK%20home%20FE%20-%20Master/) [![Coverage](https://sonarqube.paas.axa-asia.com/api/badges/measure?key=health-hk&metric=coverage)](https://sonarqube.paas.axa-asia.com/dashboard/index/health-hk)
[![Vulnerabilities](https://sonarqube.paas.axa-asia.com/api/badges/measure?key=health-hk&metric=vulnerabilities)](https://sonarqube.paas.axa-asia.com/dashboard/index/health-hk)
[![Bugs](https://sonarqube.paas.axa-asia.com/api/badges/measure?key=health-hk&metric=bugs)](https://sonarqube.paas.axa-asia.com/dashboard/index/health-hk)
[![code_smells](https://sonarqube.paas.axa-asia.com/api/badges/measure?key=health-hk&metric=code_smells)](https://sonarqube.paas.axa-asia.com/dashboard/index/health-hk)


# Home Frontend
Express + React

## Getting started
Install npm dependencies
`npm install`

Run with webpack in dev environment
`npm run dev`

Run with webpack in prod environment
`NODE_ENV=production npm start`

## Environment Variables
- PORT port the app runs on default - 3000
- LOG_LEVEL winston log levels ('error', 'warn', 'info') default - 'debug'
- LOG_FILE winston log file, if not specified then it wont create a file
- CONFIG environment of node ('local', 'uat', 'production')
- ENDPOINT the root url path the app is set at, default - 'health-insurance-advisor'
- NODE_TLS_REJECT_UNAUTHORIZED = 0 for local environment when testing UAT urls (salesforce/pricing)

### APIs
- PRICING_API pricing api url
- SALESFORCE_API salesforce api url

## Setup
- [x] Open Paas Compliant
- [x] React (Client/Server Side Rendering)
- [x] Redux
- [x] Redux-Saga
- [x] React-router
- [x] Webpack
- [x] scss
- [x] BEM (Block__Element--Modifier)
- [x] eslint
- [x] express (for server)
- [x] React Templates (for server rendering html)
- [x] babel (es6/es7)
- [x] Mocha - jsdom testing (fast and simple)
- [x] mocha test coverage
- [x] Enzyme Testing Framework
- [x] Winston Logging

## Local Tunnel
You can put your application online via localtunnel
```
lt --port 3000
```

## Docker Compose
Use docker compose to simulate the production environment

- Install Docker
https://docker.github.io/engine/installation/

- Install Docker-Compose

```
brew install docker-compose
```

- Start up docker on your computer

- Build Docker-Compose

```
NPM_TOKEN=<NPM TOKEN> docker-compose build
```

- Start Docker-Compose

```
NPM_TOKEN=<NPM TOKEN> docker-compose up
```

- Clean up docker

```
docker rmi $(docker images -f dangling=true -q)
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```
