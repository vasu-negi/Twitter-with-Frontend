# Twitter-with-Frontend
Twitter Clone with Front End


## Table of Contents
- [Table of Contents](#table-of-contents)
- [Build Process](#build-process)
- [What is Working](#what-is-working)
- [API Details](#api)
  - [Open Endpoints](#open-endpoints)
  - [Endpoints that require Authentication – User](#endpoints-that-require-authentication)
  - [User](#user)
  - [UserProfile](#user-profile)
  - [Websockets APIs](#websockets-apis)
- [Screenshots](#screenshots)
  - [Index](#index)
  - [Login](#login)
  - [Signup](#signup)
  - [Subscribe](#subscribe)
  - [User Profile](#user-profile)
  - [Query Page](#query-page)
  - [User Feed Page](#user-feed-page)


## Build Process

- Git Clone or Download the project.
- dotnet build src/FsTweet.Web/FsTweet.Web.fsproj to build project
- Since this project makes use of Postgres Databae, you’d need to load the
dump using psql -U postgres database < dump_file to load all the
schema necessary for this project
- dotnet run --project src/FsTweet.Web/FsTweet.Web.fsproj to run
the project
- Visit localhost:5000 to view this project

## What is Working

## Register account
- Send a tweet. Tweets can have hashtags (e.g. #COP5615isgreat) and
mentions (@bestuser)
- Subscribe to user’s tweets
- Re-tweets (so that your subscribers get an interesting tweet you got by
other means)
- Allow querying tweets subscribed to, tweets with specific hashtags, tweets
in which the user is mentioned (my mentions)
- If the user is connected, deliver the above types of tweets live (without
querying)

## API Details

### Open Endpoints

- Open endpoints require no Authentication.
  - Login : POST /login/
  
### Endpoints that require Authentication
- Closed endpoints require a valid Token to be included in the header of the request. A Token can be acquired from the Login view above.

### User

Each endpoint manipulates or displays information related to the User whose Token is provided with the request:
  - Show signup page : GET /signup
  - Create User for login : POST /user/
  - Signup success: GET /signup/success/%s
  - Logout: GET /logout

### UserProfile

%s means it accepts a username of type string
  - Show user profile page : GET /%s
  - Get timeline view : GET /wall/
  - Get all the followers : GET /followers/
  - Get all the user that it follows : GET /followees/ • Create Tweet/Retweet : POST /tweets/
  - Fetch all the tweets in system : GET /all/
  - To follow a user: POST /follow

### Websockets APIs
 - Get live tweets: GET /websocket

## Screenshots

### Index Page 
![Index](./docs/index.png)

### Login Page
![Login](./docs/signup.png)

### Signup Page
![Signup](./docs/signup.png)

### Follow  
![Subscribe](./docs/follow.png)

### Follow  
![Subscribe](./docs/follow.png)

### User Profile  
![User Profile](./docs/userprofile.png)

### Query Page
![Query Page](./docs/query.png)
 
### User Feed Page
![User Feed Page](./docs/feed.png)





