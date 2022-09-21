# u_protocol

describes the protocol unify uses to communicate with other unify services
<br>

# protocol

<br>
the syntax is defined by json<br>
<br>

# job system

many protocol subsets should rely on a job system to enable seamless way of two way communication
on request the server sends a job id to client: <br>
id "j234n0djn"
this id will be send back from the client if the client wants to send something thorough the pipeline

<br>

# client services

a client might offer multiple services / communication methods so every request should have a <br>
_service_ "ble" <br>
attribute <br>

the core should be accessible through the "core" value. the core services is responsible for things like "list services" etc but this will be explained in the core service section.

a typical request might look like this: 

Request:

```json
{
      "service": "ble",
      "id": "vkjh4poi89",
      "data": {
            "export": "connect",
            "arguments": ["22:FA:9F:3F:EB:16"],
      }
}
```

Response:

```json
{
      "id": "vkjh4poi89",
      "result": true
}
```

# core protocol subset
the argument "export" specifies the function that sould execute.
the argument "argument" specifies the arguments provided for that function

export: "services" no arguments
returns a list of service names

# bluetooth low energy protocol subset
_this section will be removed and put into its own repository_

<br>

exports: etc etc etc coming soon look rust repo


