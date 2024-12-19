## What is the count of facilities by facility type?

```sql
SELECT odhf_facility_type, COUNT(odhf_facility_type)
FROM public.odhf
GROUP BY odhf_facility_type
order by COUNT(odhf_facility_type) DESC
```
