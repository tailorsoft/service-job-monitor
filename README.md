# Tailorsoft Service Monitor 

add data folder with service monitor specifications

example
-

```xml
<moqui.service.job.ServiceJob jobId="poll_temperature" jobName="poll_temperature"
                                  description="get temperature salt lake city"
                                  serviceName="tailorsoft.demo.TemperatureServices.get#Temperature"
                                  cronExpression="* 0/5 * ? * * *"
                                  paused="N">
</moqui.service.job.ServiceJob>
```

### Service monitoring
monitoring services requires two entities (`Monitor`, `MonitorBounds`), these will control which service to listen to, and when to launch alerts based on their bounds.

#### tailorsoft.servicejobmonitor.Monitor
```xml
<tailorsoft.servicejobmonitor.Monitor jobName="poll_temperature" title="Temperature"
                                   valuePath="value.temp" indexName="temperature"/>
```

#### tailorsoft.servicejobmonitor.MonitorBounds

 ```xml
 <tailorsoft.servicejobmonitor.MonitorBounds
             jobName="poll_SftpCountFiles_MuckCA"
             lower="0"
             upper="10"
             count="3"
     />
 ```


