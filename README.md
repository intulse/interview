# Intulse Technical Interview

The purpose of this co-working project is to see how you work in a .NET Core (C#) environment and familiarize us with your personal development style.  This is a free-form project and there is not a specific expected solution. 

You are encouraged to:
1. Ask questions
2. Search the internet
3. Discuss technical choices

## Estimated Time
We expect the project to take anywhere between `30` to `60` minutes.

## Tools
- Visual Studio 2019+
- Postman (recommended)

## Required Technology
- [ASP.NET Core (C#)](https://docs.microsoft.com/en-us/aspnet/core/?view=aspnetcore-5.0)

## Objectives

- [ ] Create a new ASP.NET Core project in a new Solution using Visual Studio
- [ ] Create an API Controller with one endpoint which responds to a GET request to the route `/demo/call-summary`
  - [ ] The endpoint needs to retreive data from the following external data source (GET `https://dashboard.intulse.com/webservices/interview-test-data`)
  - [ ] Analyze the json returned from the data source and calculate the following:
    - [ ] Total call count
    - [ ] Total duration (seconds) of all calls
    - [ ] Average duration (seconds) of all calls in sec
    - [ ] Total count of calls in EACH hour between 8am-5pm on 2021-02-22
    - [ ] Total duration (seconds) of calls in EACH hour between 8am-5pm on 2021-02-22
    - [ ] Average duration (seconds) of calls in EACH hour between 8am-5pm on 2021-02-22
  - [ ] The endpoint should return a valid "application/json" response in the following format:
    ```json
    {
        "totalCalls": 0,
        "totalDurationInSeconds": 0,
        "avgDurationInSeconds": 0,
        "hours": [
            {
                "beginning": "08:00",
                "totalCalls": 0,
                "totalDurationInSeconds": 0,
                "avgDurationInSeconds": 0,
            },
            {
                "beginning": "09:00",
                "totalCalls": 0,
                "totalDurationInSeconds": 0,
                "avgDurationInSeconds": 0,
            },
            ....
        ]
    }
    ```
- [ ] Call your own endpoint using Postman and receive a valid json response.

## Bonus

- [ ] Implement proper use of `async`/`await` in your project
- [ ] Implement a Controller -> Service seperation of concerns pattern 
