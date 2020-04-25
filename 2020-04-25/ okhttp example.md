###  okhttp example

[A Guide to OkHttp | Baeldung](https://www.baeldung.com/guide-to-okhttp "A Guide to OkHttp | Baeldung")

[tutorials/OkHttpPostingLiveTest.java at master · eugenp/tutorials](https://github.com/eugenp/tutorials/blob/master/libraries-http/src/test/java/com/baeldung/okhttp/post/OkHttpPostingLiveTest.java "tutorials/OkHttpPostingLiveTest.java at master · eugenp/tutorials")




```java
this.client = new OkHttpClient.Builder()
                                .connectTimeout(100, TimeUnit.MILLISECONDS)
                                .readTimeout(500, TimeUnit.MILLISECONDS)
                                .build();
String json = objectMapper.writeValueAsString(map);

                            RequestBody body = RequestBody.create(
                                    MediaType.parse("application/json"), json);

                            Request request = new Request.Builder()
                                    .url("http://34.102.164.28/osrm-map-matcher/match")
                                    .post(body)
                                    .build();

                            Call call = client.newCall(request);
                            Response response = call.execute();
                            requestTimeDistribution.update(response.receivedResponseAtMillis()-response.sentRequestAtMillis());
```
