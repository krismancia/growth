# growth
growth of each city project 2
ELECT 
    YEAR(joined) AS year_joined,
    COUNT(YEAR(joined)) AS members_joined
FROM
    grp_member
GROUP BY YEAR(joined);

update grp_member set city = "chicago"
where city in ("EAST CHICAGO","WEST CHICAGO", "NORTH CHICAGO","CHICAGO HEIGHTS","CHICAGO RIDGE", "CHICAGO");

update grp_member set city = "SAN FRANCISCO"
WHERE CITY IN ("SAN FRANCISCO","SOUTH SAN FRANCISCO");

update grp_member set city ="NEW YORK"
WHERE CITY IN ("NEW YORK, WEST NEW YORK");

select
city,
year(joined) as year,
count(*) as members
from grp_member
group by city,
 year(joined) order by city,
YEAR
 where city= 'CHICAGO';

select
city,
year(joined) as year,
count(*) as members
from grp_member
group by city,
 year(joined) order by city,
YEAR
 where city= 'SAN FRANCISCO';
 
 select
city,
year(joined) as year,
count(*) as members
from grp_member 
group by city,
 year(joined) order by city,
YEAR
 where city= 'NEW YORK';
 
SELECT 
    MONTH(joined) AS month, COUNT(*) AS members
FROM
    grp_member
WHERE
    YEAR(joined) = 2017
GROUP BY MONTH(joined)
ORDER BY month;
