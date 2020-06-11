###  check tz pandas datetime


[python - Convert pandas timezone-aware DateTimeIndex to naive timestamp, but in certain timezone - Stack Overflow](https://stackoverflow.com/questions/16628819/convert-pandas-timezone-aware-datetimeindex-to-naive-timestamp-but-in-certain-t "python - Convert pandas timezone-aware DateTimeIndex to naive timestamp, but in certain timezone - Stack Overflow")


 

```
gps_data['time'] = pd.to_datetime(gps_data['tarih'], format="%Y%m%d%I%M%S")
gps_data['TIME2'] = pd.to_datetime(gps_data['TIME2'])
print(gps_data['TIME2'].dt.tz)
```
