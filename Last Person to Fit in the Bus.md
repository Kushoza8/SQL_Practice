# SQL COMMAND

select a.person_name  <br>
from Queue a Join Queue b  <br>
on a.turn>=b.turn  <br>
group by a.turn  <br>
having sum(b.weight)<=1000  <br>
order by a.turn desc  <br>
limit 1  <br>


# Explaination 
#### We apply self join on the problem and sum up the value till that particular turn 
#### Ex: if a.turn =2 then sum up the corresponding value of weights till a.turn>=b.turn
#### Limit it sum()<=1000 and use limit 1 to find out the last person
