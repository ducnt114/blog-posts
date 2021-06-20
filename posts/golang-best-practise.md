---
title: "Golang best practise"
date: 2021-06-20T22:30:46+07:00
categories: [coding]
tags: [coding, golang]
---

# Project structure for API service

Follow the MVC design pattern, there are 3 main folders:

- **controllers**:

  - each group router will be devided as 1 file, ex: `/user` -> `user_controller.go`, `/log` -> `log_controller.go`

  - only parsing request parameters/request body, then pass to `services` layer. Don't doing business logic at this layer.

- **services**:

  - Doing business logic with input from controller layer

- **repositories**:

  - Provide function to access database, normally expose basic CRUD operations.

Note: `[Controller] calls [Service(s)] who calls [repository(ies)]`

Remaining folders:

- **models**:

  - define data model

  - each table will be stored as 1 file

- **routers**:

  - define routing path

- **dtos**:

  - short form of `data transfer objects`, this folder containing request and response struct for each api route

- **mappers**:

  - convert request struct (defined in dtos) to model object and vice versa

- **conf**:

  - listing of variables which loaded from environment

# Naming convention
