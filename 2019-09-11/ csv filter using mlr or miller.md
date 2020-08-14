###  csv filter using mlr or miller


[About Miller](http://johnkerl.org/miller/doc/)


 

```shell
mlr --csv --rs lf cut -f enlem,boylam,tarih_saat1 then filter '$tarih_saat1 <= "2018-10-30 08:15:08"' 657.csv

mlr --csv --rs lf cut -f STATUS then filter '$STATUS == 10' gps_points2019-11-18T08:30:00+00:00_tkczccw.txt.augmented.csv | wc
```
