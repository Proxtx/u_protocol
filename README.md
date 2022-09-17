# u_protocol

describes the protocol unify uses to communicate with other unify services
<br>

# protocol

<br>
basically property value. except nested properties exist however they can be handled differently in different implementations of the protocol<br>
<br>
syntax: attribute name + " " + value in quotes<br>
example: test "hello test 1234"<br>
can be chained<br>
example: test "hello test 1234" another_test "another test 1234"<br>
nested is indicated via a dot<br>
example: test.first "hello test 1234" test.second "another test 1234"<br>
<br>
this protocol is simple to make implementing it in different programming languages easy.<br>
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

<br>

bluetooth low energy workflow:

1. search
2. find / don't find
3. connect
4. submit data / listen
5. result

these steps should be controlled via the protocol
