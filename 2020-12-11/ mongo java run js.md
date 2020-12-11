###  mongo java run js





 

```
    private void archivePhaseData(String scriptText, String junctionId, String archivedJunctionId, String dateString) {
        logger.info("Archiving phase data for junction id: {}, archived id: {}, datestring: {}", junctionId, archivedJunctionId, dateString);
        ScriptOperations scriptOperations = mongoTemplate.scriptOps();
        ExecutableMongoScript echoScript = new ExecutableMongoScript(scriptText.toString());
        scriptOperations.register(new NamedMongoScript("moveDocuments", echoScript));
        Object object = scriptOperations.call("moveDocuments", junctionId, archivedJunctionId, dateString);
    }
```
