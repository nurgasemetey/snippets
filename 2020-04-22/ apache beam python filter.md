###  apache beam python filter


[Filter](https://beam.apache.org/documentation/transforms/python/elementwise/filter/ "Filter")


 

```python
import apache_beam as beam

with beam.Pipeline() as pipeline:
  perennials = (
      pipeline
      | 'Gardening plants' >> beam.Create([
          {
              'icon': '🍓', 'name': 'Strawberry', 'duration': 'perennial'
          },
          {
              'icon': '🥕', 'name': 'Carrot', 'duration': 'biennial'
          },
          {
              'icon': '🍆', 'name': 'Eggplant', 'duration': 'perennial'
          },
          {
              'icon': '🍅', 'name': 'Tomato', 'duration': 'annual'
          },
          {
              'icon': '🥔', 'name': 'Potato', 'duration': 'perennial'
          },
      ])
      | 'Filter perennials' >>
      beam.Filter(lambda plant: plant['duration'] == 'perennial')
      | beam.Map(print))
```
