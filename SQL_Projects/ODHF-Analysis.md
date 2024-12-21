## What is the count of facilities by facility type?

```sql
SELECT odhf_facility_type, COUNT(odhf_facility_type)
FROM public.odhf
GROUP BY odhf_facility_type
order by COUNT(odhf_facility_type) DESC
```
## What is the percentage split for all facilities?
```sql
SELECT odhf_facility_type, COUNT(odhf_facility_type), COUNT(odhf_facility_type)/(select count(*) from public.odhf)*100
FROM public.odhf
GROUP BY odhf_facility_type
order by COUNT(odhf_facility_type) DESC
```
## Which city has the highest percentage of healthcare facilities?
```sql
SELECT city,count(facility_name),count(facility_name)/(select count(*) from public.odhf)*100
FROM public.odhf
GROUP BY city
ORDER BY count(facility_name) DESC
```
## Which province has the highest percentage of healthcare facilities?
```sql
SELECT province,count(facility_name),count(facility_name)/(select count(*) from public.odhf)*100
FROM public.odhf
GROUP BY province
ORDER BY count(facility_name) DESC
```
