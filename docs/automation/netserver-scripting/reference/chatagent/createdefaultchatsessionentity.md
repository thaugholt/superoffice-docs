---
uid: chatagent-createdefaultchatsessionentity
title: ChatAgent.CreateDefaultChatSessionEntity event method
description: Scripting events called on the CreateDefaultChatSessionEntity method on the ChatAgent service agent.
so.generated: true
keywords:
  - "netserver"
  - "scripting"
so.date: 08.26.2022
so.topic: reference
so.envir:
  - "onsite"
---
# ChatAgent.CreateDefaultChatSessionEntity

Scripting events called on the <see cref='M:SuperOffice.CRM.Services.IChatAgent.CreateDefaultChatSessionEntity'>CreateDefaultChatSessionEntity</see> method on the <see cref='IChatAgent'>IChatAgent</see>  service agent.

## BeforeCreateDefaultChatSessionEntity

```cs
    static void BeforeCreateDefaultChatSessionEntity(
       ref object  eventState
      );
```

Executes before the service method is invoked.
The return value is not calculated yet, so this method can't affect the result.
It can store some state in the *eventState* parameter, that is passed to the **After** and **AfterAsync** methods in this service call.
Event state is not preserved between different service calls. It is set to null at the start of each service call.

## AfterCreateDefaultChatSessionEntity

```cs
    static void AfterCreateDefaultChatSessionEntity(
       ref ChatSessionEntity  returnValue,
       ref object  eventState
      );
```

Executes after the service method has been invoked. The service waits for this method to complete before returning the result to the caller.
The return value has been set. The script may modify the return value by altering the **returnValue** parameter.
Any state you set in the **Before** method is passed in through the *eventState* parameter.

## AfterCreateDefaultChatSessionEntityAsync

```cs
    static void AfterCreateDefaultChatSessionEntityAsync(
       ref ChatSessionEntity  returnValue,
       ref object  eventState
      );
```

Executes after the service method is invoked, without waiting for the call to return.
The service call is not blocked waiting for this method to complete.
The async event handler cannot modify the return value of the service call.
Any state you set in the **Before** method is passed in through the *eventState* parameter.