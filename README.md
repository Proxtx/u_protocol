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
job_id "j234n0djn"
this job_id will be send back from the client if the client wants to send something thorough the pipeline

<br>

# client services

a client might offer multiple services / communication methods so every request should have a <br>
_service_ "ble" <br>
attribute <br>

the core should be accessible through the "core" value. the core services is responsible for things like "list services" etc but this will be explained in the core service section.

# bluetooth low energy protocol subset
_this section will be removed and put into its own repository_

<br>

bluetooth low energy workflow:

1. search
2. find / don't find
3. connect
4. submit data / listen
5. result

these steps should be controlled via the protocol
