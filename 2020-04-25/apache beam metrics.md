### apache beam metrics


[Metrics](https://beam.apache.org/releases/javadoc/2.4.0/org/apache/beam/sdk/metrics/Metrics.html "Metrics")




```java
 private Counter successMatchCounter;
                    private Counter failedMatchCounter;
                    private Counter timeoutMatchCounter;
                    private Distribution vehicleObservationDistribution;
                    private Distribution requestTimeDistribution;

                    @Setup
                    public void setup(){

                        successMatchCounter = Metrics.counter("TEST", "successMatchCounter");
                        failedMatchCounter = Metrics.counter("TEST", "failedMatchCounter");
                        timeoutMatchCounter = Metrics.counter("TEST", "timeoutMatchCounter");
                        vehicleObservationDistribution = Metrics.distribution("TEST", "vehicleObservationDistribution");
                        requestTimeDistribution = Metrics.distribution("TEST", "requstTimeDistribution");
```
