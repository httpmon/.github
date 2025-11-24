# HTTP Monitoring (httpmon)

## Introduction

Well, well, well, I have the same project in my repository named [HTTP_monitoring](https://github.com/elahe-dastan/HTTP_monitoring) which does exactly the same thing,
that project started to become larger and larger which was really hard to maintain that was when my friend and teacher
[Parham Alvani](https://github.com/1995parham) suggested to change the project to smaller microservices that were much
easier to maintain, here is how I want to break the project to smaller projects.

<p align="center">
  <img alt="architecture" src="../microservice.png" />
</p>

## User repository

This repository is only responsible for creating and running the endpoints Register, Login and add

## Saver repository

In the begging saver should make the tables in the database

## Server repository

This repository get the url table periodically and publishes each URL which should be checked to the nats.

## Checker repository

This repository gets the URLs which should be checked from nats, checks their status and publishes the status to nats
again, we have more than one instance if this project running
