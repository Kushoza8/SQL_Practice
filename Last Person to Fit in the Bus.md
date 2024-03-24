#SQL COMMAND
select a.person_name
from Queue a Join Queue b
on a.turn>=b.turn
group by a.turn
having sum(b.weight)<=1000
order by a.turn desc
limit 1


# Explaination 
### We apply self join on the problem and sum up the value till that particular turn 
### Ex: if a.turn =2 then sum up the corresponding value of weights till a.turn>=b.turn
### Limit it sum()<=1000 and use limit 1 to find out the last person
