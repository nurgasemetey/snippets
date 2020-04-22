### apache beam python write file 


[google cloud storage - Writing to text files in Apache Beam / Dataflow Python streaming - Stack Overflow](https://stackoverflow.com/questions/53379585/writing-to-text-files-in-apache-beam-dataflow-python-streaming "google cloud storage - Writing to text files in Apache Beam / Dataflow Python streaming - Stack Overflow")


 

```python
my_pcollection = (p | ReadFromPubSub(....)
                    |  WindowInto(FixedWindows(10*60))
                    |  fileio.WriteToFiles(path=known_args.output))
```
