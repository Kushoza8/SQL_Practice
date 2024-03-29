### Highest_Salary_In_EachBranch

#### A new concept learned here is rank

with cte as(
    select name as Employee,salary as Salary,departmentId,
    RANK() over(partition by departmentId order by salary desc) as employee_rank
    from Employee
)
select e1.name as Department,e2.Employee,e2.Salary
from cte e2 
inner join Department e1
on e1.id=e2.departmentId
where employee_rank=1

