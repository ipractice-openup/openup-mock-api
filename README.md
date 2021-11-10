# OpenUp Mock Server

This json-server project can be used to mock the rest API. The db.json file is filled with some dummy data corresponding to the wireframes in the assessment. You can use the rest api endpoints to modify the data.

Feel free to use another mock service if you are more familiar with it.

```
npm install
npm start
```

A few examples of possible requests:
```
Getting data
GET http://localhost:3000/psychologists
GET http://localhost:3000/psychologists/1
GET http://localhost:3000/psychologists/1?_embed=timeslots
GET http://localhost:3000/clients
GET http://localhost:3000/clients/1
GET http://localhost:3000/clients/1?_embed=timeslots
GET http://localhost:3000/timeslots
GET http://localhost:3000/timeslots?_expand=psychologist

Creating a timeslot
POST http://localhost:3000/timeslots 
{
    "psychologistId": 1,
    "clientId": "",
    "startDateTime": "2021-04-11T09:00:00.0000000Z",
    "endDateTime":  "2021-04-11T09:30:00.0000000Z"
}

Booking a timeslot
PATCH http://localhost:3000/timeslots/0
{
    "clientId": 1
}


```
More information on json-server can be found on [github](https://github.com/typicode/json-server).
