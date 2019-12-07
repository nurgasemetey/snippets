###  Read csv in dataflow-beam


[Apache Beam: a python example - Bruno Ripa - Medium](https://medium.com/@brunoripa/apache-beam-a-python-example-5644ca4ed581 "Apache Beam: a python example - Bruno Ripa - Medium")




```python

with apache_beam.Pipeline(options=options) as p:

    rows = (
        p |
        ReadFromText(input_filename) |
        apache_beam.ParDo(Split())
    )
###
class Split(apache_beam.DoFn):

    def process(self, element):
        country, duration, user = element.split(",")

        return [{
            'country': country,
            'duration': float(duration),
            'user': user
        }]
```
