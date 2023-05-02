# TaskTrain Client 
TaskTrain is a simple task tracker built with Ruby on Rails and React

## REQUIREMENTS
### Prerequisites
* node v14.17.4 and above
* npm 6.14.14 and above
* React 18.2.0

## Setup Instructions

This section will guide you through setting up and running this repository on your local machine.

### Project

* Clone the repository
    ```
    git clone https://github.com/sinatra-pod/moringa-library.git 
    ```

    or

    ```
    git clone git@github.com:sinatra-pod/moringa-library.git 
    ```
* Navigate to the project folder using the following command
    ```
    cd TaskTrain
    ```
* To interact with the front-end part of the application, navigate to the `client` folder
    ```
    cd client
* To run the front-end part first ensure that you run 
  ```
  npm install 
* To start the application run
  ```
  npm run dev
  ```

Screens
-------

Have a look at what I have been working on.

| Login | Register |
| ----- | -------- |
| ![login](../screens/login.png) | ![register](../screens/register.png) |


Meta
----
Authors:
* [Ian Okumu](https://github.com/otsembo)
* [please add you author creds here]

**Status**: `maintained, and is currently in development`

**Version**: `v0.1.0`

**React Version**: `18.2.+`


Usage
-----


## License
This project is licensed under the MIT License

Documentation
-------------
You can see the documentation over at **Read the Docs**

Resources
-------------

* https://react-typescript-cheatsheet.netlify.app/





# TASKTRAIN API
This API provides powers our application, [TaskTrain](https://task-train.netlify.app/). The API is built using Ruby on Rails.

## Technologies Used
This application has been built with the following tools:

![ruby](https://img.shields.io/badge/Ruby-CC342D?style=for-the-badge&logo=ruby&logoColor=white)


- **Ruby `v2.7.+`**
- **Rails `v7.0.+`**
- **activeRecord `v7.0.4`**
- **rake `v13.0.6`**
- **rerun `v0.14`**
- **require_all ` 3.0`**
- **faker`v3.0`**
- **rspec `v3.12`**
- **sqlite3 `v3.0`**


## Project Setup
You can set up this repository by following this manual

1. Clone the repository
    ```{shell}
   git clone https://github.com/otsembo/TaskTrain.git
   ```
2. Ensure the ruby gems are set up in your machine
    ```{shell}
   bundle install
   ```
3. Perform any pending database migrations
   ```{shell}
   rails db:migrate
   ```
4. Run the application
    ```{shell}
    rails server
    ```
5. Open the application from your browser
    ```
   http://localhost:3000
   ```

## Application

### Folder Structure


    .
    ├── ...
    ├── api                   
    │   ├── app              
    │   ├── config            
    │   ├── db            
    │   ├── spec          
    │   └── ...                 
    └── ...



### MODELS
This section will describe the schema definitions for our database.

#### 1. todos
- All the tasks that have been added.

| COLUMN           | DATA TYPE                                         | DESCRIPTION                                      | 
|------------------|---------------------------------------------------|--------------------------------------------------|
| id               | Integer                                           | Unique identifier.                               |
| title            | String                                            | The name of the task.                            |
| status           | ENUM `[CREATED, IN_PROGRESS, COMPLETE, CANCELLED]`| The status of the task.                          |
| description      | String                                            | A short description about the submission.        | 
| priority         | ENUM `[HIGH, MEDIUM, LOW]`                        | How urgent is the task                           |
| createdAt        | Date                                              | The date the submission was created.             |


#### 2. users

- All the registered user accounts

| COLUMN          | DATA TYPE | DESCRIPTION                           | 
|-----------------|-----------|---------------------------------------|
| id              | Integer   | Unique identifier.                    |
| email           | String    | User's email addrress.                |
| password_digest | String    | User's password hashed with `BCrypt`. |
| updated_at      | Date      | The date the user was updated.        |
| createdAt       | Date      | The date the user was created.        |



| Column Name | Data Type | Description |
| --- | --- | --- |
| name | string | Name of the drop |
| user_id | bigint | Unique ID of the user associated with the drop |
| folder_id | bigint | Unique ID of the folder associated with the drop |
| created_at | datetime | Timestamp of when the drop was created |
| updated_at | datetime | Timestamp of when the drop was last updated |