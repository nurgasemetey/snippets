### Autowire in kotlin


[How to use spring annotations like @Autowired in kotlin? - Stack Overflow](https://stackoverflow.com/questions/35479631/how-to-use-spring-annotations-like-autowired-in-kotlin)




```kotline
@Component
class YourBean {

    @Autowired
    lateinit var mongoTemplate: MongoTemplate

    @Autowired
    lateinit var solrClient: SolrClient
}
```
