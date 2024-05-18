# Intulse Technical Interview (Part 1)

The purpose of this co-working project is to see how you work in a .NET Core (C#) environment and familiarize us with your personal development style.  This is a free-form project and there is not a specific expected solution. 

You are encouraged to:
1. Ask questions
2. Search the internet
3. Discuss technical choices

## Estimated Time
We expect the project to take anywhere between `30` to `60` minutes.

## Tools
- Visual Studio 2022+
- Postman (recommended)

## Required Technology
- [ASP.NET Core (C#)](https://docs.microsoft.com/en-us/aspnet/core/)

## Objectives

- [ ] Create a new ASP.NET Core Web API project in a new Solution using Visual Studio
- [ ] Create an API Controller with one endpoint which responds to a GET request to the route `/demo/call-summary?date=2021-02-22`
  - [ ] The endpoint needs to retreive data from the following external data source (GET `https://raw.githubusercontent.com/intulse/interview/main/interview-test-data.json`)
  - [ ] Analyze the json returned from the data source and calculate the following for the specified input `date`:
    - [ ] Total call count
    - [ ] Total duration (seconds) of all calls
    - [ ] Average duration (seconds) of all calls
    - [ ] Total count of calls in EACH hour between 8am-5pm on 2021-02-22
    - [ ] Total duration (seconds) of calls in EACH hour between 8am-5pm on 2021-02-22
    - [ ] Average duration (seconds) of calls in EACH hour between 8am-5pm on 2021-02-22
  - [ ] The endpoint should return a valid "application/json" response in the following format:
    ```json
    {
        "summaryDate": "2021-02-22"
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
- [ ] Use dependency injection to inject the service into the controller


# Intulse Technical Interview (Part 2)

The purpose of this co-working project is to see how you work in a Angular environment and familiarize us with your personal development style.  This is a free-form project and there is not a specific expected solution. 

You are encouraged to:
1. Ask questions
2. Search the internet
3. Discuss technical choices

## Estimated Time
We expect the project to take anywhere between `30` to `60` minutes.

## Tools
- Visual Studio Code
- NPM ("Nodejs package manager" is a part of [NodeJS](https://nodejs.org))

## Required Technology
- [Angular 16+](https://angular.dev)

## Objectives

- [ ] Create a new Angular project using NPM, Angular CLI, and Visual Studio
- [ ] Create a single page application that allows the user to input a date and click a button to get a call summary for that day.
- [ ] When the button is clicked display a loading indicator while making an API call to the endpoint you developed in part 1 of this technical interview
- [ ] When the data is loaded hide the loading indicator and display that data in pleasing manor
- [ ] Use a `for of` structural directive to display each of the "hours" data points
