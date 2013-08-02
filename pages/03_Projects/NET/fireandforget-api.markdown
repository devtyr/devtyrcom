Title: FireAndForget - API - DevTyr
Description: Easy to configure, lightweight and asynchronous message bus
Keywords: FireAndForget, Message, Service, Bus, Lightweight, Asynchronous
Author: DevTyr / Norbert Eder
Menu: FireAndForget
MenuTitle: API
Sidebar: FireAndForget
Template: page_sidebar
Directory: projects/fireandforget
-----

## API

This page contains everything you need to know about messages and the API provided by the message bus.

### Message

This is how a JSON message looks like needed by the message bus:

<pre>
  {
     "Data":{
        "MessageType":"DefaultTask",
        "Data":"This is some data for the default handler0"
     }
  }
</pre>

Very important is `MessageType`. This has to match with an executor that handles this kind of messages. `Data` includes the serialized data for the executor. 

To define a delayed message use this notation:

<pre>
  {
    "Data": {
        "MessageType": "TestTask",
        "ExecuteAt": null,
        "Data": "Data for the test handler0",
        "IsBulk": false
    }
  }
</pre>

`ExecuteAt` is a date value indicating when to execute the task (delayed). Finally, `IsBulk` defines that this task should be combined with the same task (this is only for delayed tasks).

> `ExecuteAt` and `IsBulk` are *optional*.

### API in detail

These are the possible requests for controlling FireAndForget:

*Add a message*

    POST http://localhost:2900/api/v1/enqueue HTTP/1.1
    Host: localhost:2900
    content-type: application/json
    content-length: 72

    {
      "Data": {
        "MessageType": "Default",
        "Data": "Muh"
      }
    }

*Add a delayed message which is bulk enabled*

    POST http://localhost:2900/api/v1/enqueue HTTP/1.1
    Host: localhost:2900
    content-type: application/json
    content-length: 197

    {
      "Data": {
        "MessageType": "TestTask",
        "ExecuteAt": "2013-05-28T12:18:15.4027698+02:00",
        "Data": "THIS TASK IS DELAYED!!!!",
        "IsBulk": true
      }
    }

*Requeue all erroneous tasks*

    POST http://localhost:2900/api/v1/retry HTTP/1.1
    Host: localhost:2900
    content-type: application/json
    content-length: 0

*Requeue all erroneous tasks of a specific queue*

    POST http://localhost:2900/api/v1/retry/default HTTP/1.1
    Host: localhost:2900
    content-type: application/json
    content-length: 0

There is a test client in the solution to show how it works. It's really simple!