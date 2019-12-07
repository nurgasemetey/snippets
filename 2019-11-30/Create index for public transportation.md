### Create index for public transportation







```sql
CREATE INDEX timestamp_ind ON public.ulasim_veri ("TIMESTAMP" DESC);
SELECT * FROM public.ulasim_veri WHERE "TIMESTAMP" >= '2018-11-06 05:00:00' AND "TIMESTAMP" <= '2018-11-07 00:00:00'
```
