###  window apache beam example



[Beam Programming Guide](https://beam.apache.org/documentation/programming-guide/#windowing-basics "Beam Programming Guide")


 

```python
class AddTimestampDoFn(beam.DoFn):
  def process(self, element):
    # Extract the numeric Unix seconds-since-epoch timestamp to be
    # associated with the current log entry.
    unix_timestamp = extract_timestamp_from_log_entry(element)
    # Wrap and emit the current entry and new timestamp in a
    # TimestampedValue.
    yield beam.window.TimestampedValue(element, unix_timestamp)

timestamped_items = items | 'timestamp' >> beam.ParDo(AddTimestampDoFn())


```
