# UniversityAssignments
In this repo you'll find two different projects, both created in the context of assignemts. The first one is a bookstore using SQL, whilst the second is an elevator simulation using PDDL.


# Bookstore Using SQL

The project describes a bookstore.

The following ER-Diagram(P.P.Chen) shows the relations described in the code.
![image](https://github.com/angzosan/UniversityAssignments/assets/118728873/8fc152cb-5fd4-4d08-a8ab-c7325d3f1e4c)

The diagram above can be turned into a relational model ( following image ) . The one shown below uses a Crow's foot notation.
![image](https://github.com/angzosan/UniversityAssignments/assets/118728873/5b105b94-eb90-4d80-840e-e28d19d86f66)

# Elevator Simulation using PDDL

Full simulation of how an elavator would work, following specific conditions, using pddl.

Testing system : http://editor.planning.domains/
Output : 
![image](https://github.com/angzosan/UniversityAssignments/assets/118728873/2fedeff6-f953-411c-97f3-3bb5dc0900ed)

Status tree :
![image](https://github.com/angzosan/UniversityAssignments/assets/118728873/80c8d549-d95f-4640-ab9c-a875f619d9e1)

Solution length : 11 Possible statuses : 444

ANALYSIS 7 Levels 3 Elevators

Elevator A routes: All routes that include the levels : 2-4-6 ( B-D-F )

Elevator B routes: All routes that include the levels : 1-3-5-7 ( A-C-E-F )

Elevator C routes: All routes that include the levels : 1-2-3-4-5-6-7 ( A-B-C-D-E-F-G )

Entities : (level ?y), (elevator ?x), (transfer ?t) Relations : (is_at ?x ?y), (at ?t ?y), (can_go ?x ?y ?y) -> elevator x can go from level y to level y - different y's-

Transition Operands name : call variables : from, to, x, transfer prerequisetes : (level ?from) (level ?to) (elevator ?x) (transfer ?transfer) (at ?transfer ?from) -> already being in the level we want to start from (can_go ?x ?from ?to) -> the elevator being able to visit this level (not(is_at ?x ?from) ) Add list(statements we make 'true') : (is_at ?x ?from) -

name : move variables : from, to, x, transfer prerequisetes : (level ?from) (level ?to) (elevator ?x) (transfer ?transfer) (at ?transfer ?from) -> already being in the level we want to start from (can_go ?x ?from ?to) -> the elevator being able to visit this level (is_at ?x ?from) Add list(statements we make 'true') : (at ?transfer ?to) Remove list(statements we make 'false') : (not (at ?transfer ?from))
