###  Setup example in java dofn apache beam


[DoFn | Mingmin's Blog](https://mingminxu.com/tag/dofn/ "DoFn | Mingmin's Blog")


 

```java
public class MapBuyerSellerLkpFn extends DoFn<MapCheckout, MapCheckout> {
 
  /**
   * 
   */
  private static final long serialVersionUID = -451161312788562675L;  
 
  @Setup
  public void setup(){
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "setup");
  }
  @Teardown
  public void close(){
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "close");
  }
 
  @StartBundle
  public void startBundle(Context c){
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "startBundle");
  }
  @FinishBundle
  public void finishBundle(Context c){
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "finishBundle");
  }  
 
  @Override
  public void prepareForProcessing() {
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "prepareForProcessing");    
  }
 
  @ProcessElement
    public void processElement(ProcessContext c) {
    BeamComponentTracker.getInstance().reportUsage("MapBuyerSellerLkpFn", "processElement");
  }
}
```
