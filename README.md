# Prolog MiniMaster
A short SWI-Prolog program, simulating a fictional university that offers a mini-master in Informatics, worth 30 credits.
This program checks if a student has completed all requirements for graduation.

We define two different tracks for the mini-master:
- Software Systems (ss) 
- Information Systems (is) 

We further define three faculties that offer courses: 
- Informatics (inf)
- Economics (eco)
- Law (law)

Graduation criteria are as follows:
- ss student: 20 credits from inf courses, 10 credits from eco courses
- is student (inclusive OR): 
  - 20 credits from inf, 5 credits from eco and 5 credits from law courses 
  - 20 credits from inf and 10 credits from eco courses

Courses offered by faculty (title,credits):
- inf faculty:
  - Practical Artificial Intelligence (pai), 10
  - Theoretical Artificial Intelligence (tai), 5
  - Data Science (ds), 5
  - Communication Systems (cs), 5
  - Big Data Analytics (bda), 5
  - IT Security (its), 5
- eco faculty:
  - Banking and Finance (bf), 5
  - Behavioral Economics (be), 5
  - Quantitative Finance (qf), 10
  - Organisation and Management (om), 5
  - Business Informatics (bi), 5
  - A primer in Entrepreneurship (pe), 5
- law faculty:
  - Democracy (d), 10
  - Financial Law (fl), 5
  - Public Procedural Law (ppl), 2.5
  - European Institutes (ei), 2.5

Students inserted were alice, bob, carlos, daniela, philip
To check if a student has completed all requirements, use 
```prolog
pass(student_name).
```
All the functions are listed in the soure file itself, prolog is very easy to read, so have a look at it.

An concrete example of a query with output 
```prolog
%! lists all courses from faculty inf taken by philip by title, faculty and credits.
coursesInf(philip,Y,H,Z).
Y = pai,
H = inf,
Z = 10 ;
Y = cs,
H = inf,
Z = 5 ;
Y = bda,
H = inf,
Z = 5 ;
Y = its,
H = inf,
Z = 5 ;
false.
```
This was one of the exercises in the Practical Artifical Intelligence Lecture at University of Zurich UZH
