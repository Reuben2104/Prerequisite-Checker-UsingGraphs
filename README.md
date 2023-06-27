# Prerequisite-Checker

**Overview**
Imagine (just for the sake of this assignment) that you are a student interested in the Rutgers Computer Science program. There are tons of courses available, many with prerequisites that need to be satisfied before they can be taken. It can get confusing to navigate what courses you need to take before other courses, and what courses are available to you given the courses you have already taken.
Luckily, you recognize that mapping out all the courses along with their prerequisites forms a DAG (Directed Acyclic Graph), or a graph with directed edges and no cycles.

**Tasks**

1. AdjList
This Java class will take two command line arguments in the following order: an adjacency list input file name and an output file name.
The input file will be formatted as follows:
An integer a (the number of courses)
a lines, each with a course ID (a string)
An integer b (the number of prereq connections)
b lines, each with a course ID, then one of its direct prerequisites (space separated)
Every course ID is guaranteed to NOT contain spaces or newlines
You will use this list of prereq connections to construct an adjacency list, then output it to the output file.
The output file will be formatted as follows:
a lines, where each line starts with a course ID and a space, then lists all the course’s immediate prerequisites (space separated)
The order in which you output the lines, as well as the order in which you output the courses in each line after the first DOES NOT MATTER for grading.

2. ValidPrereq
This Java class will take three command line arguments in the following order: an adjacency list input file, a prereq input file and an output file.
The adjacency list input file will be formatted exactly as the one from AdjList.
The prereq input file will be formatted as follows:
1 line containing the ID for course 1
1 line containing the ID for course 2
You will use the graph described by the adjacency list input file to answer the following question about the courses: If course 2 was an immediate prerequisite for course 1, would all courses still be possible to take? (Remember, a course can only be taken once all its immediate prerequisites have been met). For example, adding cs111 as a prerequisite to cs211 is redundant, but doesn’t cause any problems and all courses are still possible to take. Adding cs211 as a prerequisite to cs111 creates a situation where you cannot take cs111 OR cs211 OR anything in between, so all courses are no longer possible to take.
The output file will be formatted as follows:
One line, containing either “YES” or “NO”. “YES” if all courses are still possible to take for a new student, and “NO” otherwise.

3. Eligible
This Java class will take three command line arguments: an adjacency list input file, an eligible input file, and an output file.
The adjacency list input file will be formatted exactly as the one from AdjList.
The eligible input file will be formatted as follows:
An integer c (the number of courses)
c lines, each with one course ID
Assume you have completed these c courses, all their prerequisites (both direct and indirect) and nothing else. What are all the courses that you are eligible to take now (and haven’t taken yet)?
The output file will be formatted as follows:
For each course you are now eligible to take, output its course ID on its own line.
The order in which you output the course IDs DOES NOT MATTER for grading.

4. NeedToTake
This Java class will take three command line arguments in the following order: an adjacency list input file, a need to take input file, and an output file.
The adjacency list input file will be formatted exactly as the one from AdjList.
The need to take input file will be formatted as follows:
One line containing a course ID (target course)
An integer d (the number of taken courses)
d lines, each with one course ID (taken course)
Assume you have taken these d courses, all their prerequisites (both direct and indirect), and nothing else. What are all the courses that you have NOT taken yet, which are required in order to take the target course? In other words, what direct and indirect prerequisites of the target course have you not taken yet?
The output file will be formatted as follows:
For each course you need to take, output its course ID on its own line.
The order in which you output the course IDs DOES NOT MATTER for grading.

5. CHALLENGE PROBLEM: SchedulePlan (25 points extra credit!)
This Java class will take three command line arguments in the following order: an adjacency list input file, a schedule plan input file, and an output file.
The adjacency list input file will be formatted exactly as the one from AdjList.
The schedule plan input file will be formatted as follows:
One line containing a course ID (target course)
An integer e (the number of taken courses)
e lines, each with one course ID (taken course)
Assume you have taken these e courses, all their prerequisites (both direct and indirect), and nothing else. Plan out a schedule such that you are eligible to take the target course in the FEWEST POSSIBLE number of semesters. Remember that you can’t actually include a course in a semester until all its direct prerequisites were satisfied in previous semesters.
The output file will be formatted as follows:
An integer f (the number of semesters)
f lines, each with some number of space separated course ID’s
ANY VALID SCHEDULE which ends with you being able to take the target course will be accepted by the grader, as long as you utilize the minimum possible number of semesters.




