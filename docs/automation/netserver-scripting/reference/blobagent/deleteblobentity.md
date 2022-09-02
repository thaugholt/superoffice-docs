---
uid: blobagent-deleteblobentity
title: BLOBAgent.DeleteBlobEntity event method
description: Scripting events called on the DeleteBlobEntity method on the BLOBAgent service agent.
so.generated: true
keywords:
  - "netserver"
  - "scripting"
so.date: 08.26.2022
so.topic: reference
so.envir:
  - "onsite"
---
# BLOBAgent.DeleteBlobEntity

Scripting events called on the <see cref='M:SuperOffice.CRM.Services.IBLOBAgent.DeleteBlobEntity'>DeleteBlobEntity</see> method on the <see cref='IBLOBAgent'>IBLOBAgent</see>  service agent.

## BeforeDeleteBlobEntity
```cs
    static void BeforeDeleteBlobEntity(
       Int32  blobEntityId,
       ref object  eventState
      );
```
Executes before the service method is invoked.
It can store some state in the *eventState* parameter, that is passed to the **After** and **AfterAsync** methods in this service call.
Event state is not preserved between different service calls. It is set to null at the start of each service call.
## AfterDeleteBlobEntity
```cs
    static void AfterDeleteBlobEntity(
       Int32  blobEntityId,
       ref object  eventState
      );
```
Executes after the service method has been invoked. The service waits for this method to complete before returning the result to the caller.
This service call has no return value, so there is no **returnValue** parameter
Any state you set in the **Before** method is passed in through the *eventState* parameter.
## AfterDeleteBlobEntityAsync
```cs
    static void AfterDeleteBlobEntityAsync(
       Int32  blobEntityId,
       ref object  eventState
      );
```
Executes after the service method is invoked, without waiting for the call to return.
The service call is not blocked waiting for this method to complete.
Any state you set in the **Before** method is passed in through the *eventState* parameter.
