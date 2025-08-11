```
  select
  	c.company_name,
  	avg(p.carbon_footprint_pcf) avg_cfp
  from product_emissions p
  Join companies c on c.id = p.company_id 
  group by 1
  order by 2 desc
  limit 1
```  
caau 2
```
  select
  	year,
  	sum(carbon_footprint_pcf) total_over_year
  from product_emissions 
  group by 1
  order by 1 desc
```
