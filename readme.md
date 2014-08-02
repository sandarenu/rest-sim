### Writing Simple REST Simulators using WireMock

This is a simulator created for a REST service using WireMock. This mechanism can be used to test our client without availability of real server. 

#### How to Test

* Start the server using `start-sim.sh`
* Send sample request using *CURL*

* Request 1 
<pre>
curl -v -H "Content-Type: application/json" -X POST -d \
'{"trxId":"123456789",
"token":"onlinea98afd65d57961b21ef2114eafc5aa43",
"messageId":"101306191208080001"}' http://localhost:8482/charging-api/v1/authenticate
</pre>

* Request 2 
<pre>
curl -v -H "Content-Type: application/json" -X POST -d \
'{"trxId":"123456789",
"token":"offlinea98afd65d57961b21ef2114eafc5aa43",
"messageId":"101306191208080001"}' http://localhost:8482/charging-api/v1/authenticate
</pre>
