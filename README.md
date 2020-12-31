# Twitter-with-Frontend
Twitter Clone with Front End


## Table of Contents
• Table of Contents • Build Process
• What is Working • API Details
– Open Endpoints
– Endpoints that require Authentication – User
– UserProfile
– Websocket APIs
• Screenshots – Index – Login
– Signup
– Subscribe
– User Profile
– Query Page
– User Feed Page
• Video Link
Build Process
• Unzip file unzip NegiYadav.zip
• dotnet build src/FsTweet.Web/FsTweet.Web.fsproj to build project
• Since this project makes use of Postgres Databae, you’d need to load the
dump using psql -U postgres database < dump_file to load all the
schema necessary for this project
• dotnet run --project src/FsTweet.Web/FsTweet.Web.fsproj to run
the project
• Visit localhost:5000 to view this project
What is Working
• Register account
• Send a tweet. Tweets can have hashtags (e.g. #COP5615isgreat) and
mentions (@bestuser)
• Subscribe to user’s tweets
• Re-tweets (so that your subscribers get an interesting tweet you got by
other means)
• Allow querying tweets subscribed to, tweets with specific hashtags, tweets
in which the user is mentioned (my mentions)
• If the user is connected, deliver the above types of tweets live (without
querying)
