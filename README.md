# CSS 342 Data Structures, Algorithms, and Discrete Mathematics I

<img src="https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/images/repo_cover.png"
     alt="schedule icon"
     width="90%" />
     
## Official Course Info ([link](https://www.washington.edu/students/crscatb/css.html))
Integrating mathematical principles with detailed instruction in computer programming. Explores mathematical reasoning and discrete structures through object-oriented programming. Includes algorithm analysis, basic abstract data types, and data structures. May not be repeated. 

## Prerequisites ([link](https://www.washington.edu/students/crscatb/css.html))
A minimum grade of 2.8 in either CSS 133, CSS 143, CSE 143, or CSS 162; and minimum grade of 2.5 in either STMATH 125 or MATH 125.

## Course Info

| Key Info             |                                                              |
| -------------------- | ------------------------------------------------------------ |
| Date & Time          | WF 5:45pm - 7:45pm                                           |
| Lecture Location     | Hybrid: UW1 building room 021 / [Zoom](https://washington.zoom.us/j/91844203771)  |
| Lecturer             | [Peng Du](https://www.linkedin.com/in/peng-du-ph-d-14b0a11b)  |
| Grader/TA            | Maranatha Chiu                            |
| Email                | pengdu@uw.edu ([CSS342] MUST show on subject)                |
| Office Hours         | Discord ([use this invite to join](https://discord.gg/etC5bR8nJb)) |

## Communication
- **Canvas** for assigning tasks (homework, quizzes, and exams) and scores.
- **Discord** for announcements, discussion forums, assignment posting, and individual grades. Choose this if in doubt.
- **Email** barely use but will reply probably asking you to use the above two methods

### Coursework Distribution
| Course Work | Grading % |
|-------------|-----------|
| Homeworks | 35        |
| Quiz & in-class exercises      | 5   |
| Midterm exam       | 20       |
| Final projects | 20 |
| Final exam      | 20        |
| Total | 100 |

### Grading Rubric
All grades will be listed as percentages in the Canvas LMS. The conversion table below will help you determine your final grade. For example, if you earn 950 points (or 95%) you will get a 4.0. If you earn 750 points (or 75%) you will earn a 2.0.

<img src="https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/images/gradingrubric.png"
     alt="schedule icon"
     width="70%" />


## Exams (quiz, midterms and final)

- Possibly in-class or "take-home" style depending on Covid situation. Each will be 1.5 hr to 2 hrs.
- Problems such as single-choice question, discussion, and coding
- Midterms are incremental (covering material up to the exam date), and final exam is comprehensive (covering everything).
- There will be reviews and examples given before midterms and final.
- Quiz is similarly to homework except no question and discussion will be given by instructor on solution before submission. 
- There might be in-class quiz during lecture.

## Lecture Recording
All lecture will be recorded to the best effort. The playlist is [here](https://www.youtube.com/playlist?list=PLmZYijop2pDbcQOvKJQumZpJGyIetIQz0).

## Textbook
- Data Abstraction & Problem Solving With C++: Walls & Mirrors, Sixth or Seventh Edition, Frank M. Carrano, Addison Wesley, 2013, ISBN-10: 0132923726, ISBN-13: 978-0132923729
- (Free PDF) [An Active Introduction to Discrete Mathematics and Algorithms, Charles Cusack, David Santos, GNU Free Software, 2014](https://cusack.hope.edu/Notes/Notes/Books/Active%20Introduction%20to%20Discrete%20Mathematics%20and%20Algorithms/ActiveIntroToDiscreteMathAndAlgorithms.2.6.3.pdf)

Here's the [full list](https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/books.md) of books including optional and recommended.

## Class Goal
The goals of this course are for students to: 

- Be comfortable with OOP programming and debugging in C++.
- Excise and reinforce the knowledge about fundamental data structures and algorithms, and as a result improve problem solving skills.
- Adopt the "clean code" (e.g. [this](https://youtu.be/AeWbJ5LIFNg) and [this too](https://youtu.be/4F72VULWFvc)) mindset via the practice of TDD ([Test Driven Development](https://youtu.be/d1EAyR_NCOA)).
- Practice and adopt the use of source control system.
- Be exposed to IT-industry popular development tools such as CMake, CLion, Git/Github/CICD, Vim, cloud computing and virtual machine, CICD.

## Lecture
- Read the relevant textbook chapters before each class.
- There will be live "code-along" in lecutre. Have a running dev environment ready for each lecture.
- Lecture will be recorded to the best effort. Lecture recording, PPT slides and demo code from class will be available shortly after each lecture.
- PPT Slides are for reference only and tentative to change even after lecture.
- Take notes. Write down your questions in class and follow up later.

## Tentative Schedule

<img src="https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/images/schedule.png"
     alt="schedule icon"
     width="30%" />
     
- The following class schedule is an approximate, high-level ordering of topics.
- Schedule is tentative and subject to change. Changes will be announced in class and/or Discrod channels.
     
|  Date | Week | Topics | Chapters | Course Work |
| --- | --- | --- | :--- | --- |
| 3/30, 4/1 | 1 | Course intro, dev setup<br/>C++ basics (function, loop, ifs, pointer, reference)<br/>TDD basics, (watch [this](https://www.youtube.com/watch?v=iUD55KscxsA) before class 2)<br/>Homework submission walthrough | C++ ch {1}<br/>ch interlue {2}<br/>apendx A & B | [homework 1](https://github.com/a-teaching-goose/CSS342A-2022-Spring/tree/main/homeworks/homework-1) |
| 4/6, 8 | 2 | C++ (OOP) <br/>Makefile, CMake<br/>Debugging<br/>Unit Testing<br/>  | C++ ch interlude {1, 5, 6}<br/>ch {3, 4 & 11} | [quiz-1](https://github.com/a-teaching-goose/CSS342A-2022-Spring/blob/main/exam/quiz/quiz-1.md) |
| 4/13, 15 | 3 | OOP, ADT (array, array list) | C++ ch {8, 9, 12} | [homework2](https://github.com/a-teaching-goose/CSS342A-2022-Spring/tree/main/homeworks/homework-2) |
| 4/20, 22 | 4 | OOP, ADT (linked list, iterator)<br/>STL intro | C++ ch interlude {8}<br/>ch {6, 7, 13, 14} |  |
| 4/27, 29 | 5 | ADT (map)<br/>Recursion<br/>Dependency Injection<br/> | C++ ch {18} | [quiz-2](https://github.com/a-teaching-goose/2022-342a-quiz-2) </br> [homework3](https://github.com/a-teaching-goose/CSS342A-2022-Spring/tree/main/homeworks/homework-3) |
| 5/4, ***6*** | 6 | ***Midterm on 5/6***<br>ADT (map)<br/>Recursion<br/>Dependency Injection<br/> | C++ ch {2, 5.3, 6, 13} | [homework4](https://github.com/a-teaching-goose/CSS342A-2022-Spring/tree/main/homeworks/homework-4) |
| 5/11, 13 | 7 | Special topic: A tale of two linkedlist reversals<br>Recursion (back tracking)<br/>ADT(binary trees) | C++ ch {15} |   |
| 5/18, 20 | 8 | ADT(binary trees, cont)</br>Sorting & complexity analysis | C++ ch {15.5} |  |
| 5/25, 27 | 9 | ADT(graph, topology sort)<br/>Math induction & Propositional logic | Math {4, 8.1}, C++ {20} |   |
| 6/1, 3 | 10 | Final review |  |  |
| ***6/8*** | 11 | ***Final exam on 6/8, Wednesday, no lecture*** |  |  |

[Registration deadlines for class add, drop, withdraw...](https://www.uwb.edu/academic-calendar/2021-2022-academic-calendar/registration-2021-2022)

## Policy (IMPORTANT)
All the materials are either in class or online. In-class only materials will be unavailable unless you attend class. The only exceptions are: you are terribly sick, family emergency, or academic event. In such cases, you should provide evidence (e.g., medical doctor’s note). 

- Assignments: All assignments should be done **independently** and any cheating or collaboration work will be returned without points, and will be reported as academic misconduct to the university. All assignments are required to submit online (Canvas), unless otherwise noted. Please note that **late assignments will not be accepted** under any circumstances.
- Discussions, Exercises, and Labs: Short programming works or short questions will be given in class. You are required to finish the work in class and submit online (most cases). The works won’t be repeated outside of the class, therefore it is your responsibility to be in class to claim your points.  
- Exams: Exams cover the contents you have learned in class by the time of the exam, none of them are cumulative. There will be **no make-up exams**, either earlier or later. Exceptions might be granted, very rarely though, and only under extenuating circumstances.
- (In-person quarter only) Quizzes: Quizzes will be given during the first 20 minutes of the class throughout the quarter.

## Code of Conduct and Behaviour
Work is to be done independently unless directed otherwise; collaborative work is NOT acceptable. You may discuss the problem statement with each other and help debug, but all designing and coding are to be done independently. Any pair programming must be approved by me. This class is run by honor code.
- By taking this class, you agree that you will **not** collaborate inappropriately on any work. In some cultures, family relationships, and loyalty are considered above all others.
- In this course, we are an academic family and you betray the instructor’s and the university’s trust should you violate the honor code. This violation will be taken seriously. (See [Academic Conduct](http://www.uwb.edu/academic/policies/Academic_Conduct.xhtml)).
- The purpose of the assignments is to help you understand deeply technical material. You may discuss the problem statement with each other and help debug, but do your own design and coding. See the student [honor code](https://www.uwb.edu/academic/policies/academic-conduct).
- Live lectures are inherently interactive. Questions during class are encouraged. Please raise your hand to get the instructor's attention. At the instructor's discretion, answers may be tabled until the end of class if they are too far off-topic.
- Computer (or handheld devices) use during the lecture is limited to taking notes and lab/exercise programming. 
- Displaying any images or videos on your screen during the lecture is not allowed as it is distracting and disrespectful.
- Silence your mobile phones and limited your mobile device usage. If you need to take a call or you have an emergency, step out of the classroom.
- Please, no whispering, chitchatting, giggling, etc., this is very distracting and disrespectful. Disruptive students will be asked to leave and you will be responsible for missing lectures.
- If you arrive late or have to leave in the middle of class, do so quietly without causing disruption.
- Flash photography is not permitted. Non-flash photography to capture the white-board is permitted as long as it is not disruptive or distracting.

## Disability Accommodations 
To request academic accommodations due to a disability, please contact Disabled Student Services (DSS) at 425.352.5307, 425.352.5303 TDD, 425.352.5455 FAX, or at dss@uwb.edu. You will need to provide documentation of your disability as part of the review process prior to receiving any accommodations (by the third week of the quarter). 

## Religious Accommodations
Washington state law requires that UW develop a policy for accommodation of student absences or significant hardship due to reasons of faith or conscience, or for organized religious activities. The UW’s policy, including more information about how to request an accommodation, is available at Religious Accommodations Policy (https://registrar.washington.edu/staffandfaculty/religious-accommodations-policy/). Accommodations must be requested within the first two weeks of this course using the Religious Accommodations Request form (https://registrar.washington.edu/students/religious-accommodations-request/).

## Inclement Weather Policy 
Call (206)-547-4636 (206-547-INFO) to see if University of Washington, Seattle, Bothell, and Tacoma campuses are open and operating. 

## Classroom Emergency Preparedness 
Please see http://www.uwb.edu/safety/are-you-ready for detailed information on the following topics: active shooter, inclement weather, bomb threat, crime or violence, earthquake, fire, hazardous material spill, identity theft, lockdown, medical emergency, online safety, power outage, sexual assault, student in distress, suspicious mail, theft, pandemic flu, and extreme heat. 

## For our Veterans 
If you are a student who has served in our nation’s military forces, thank you for your service. We hope that you feel comfortable enough to confidentially self-identify yourself to your instructor so s/he can help you make a successful transition from the military to higher education.

## Respect for Diversity 
- Diverse backgrounds, embodiments and experiences are essential to the critical thinking endeavor at the heart of university education. In STEM and at UW Bothell, students are expected to: 
- Respect individual differences which may include, but are not limited to: age, cultural background, disability, ethnicity, family status, gender presentation, immigration status, national origin, race, religion, sex, sexual orientation, socioeconomic status, and veteran status. 
- Engage respectfully in discussion of diverse worldviews and ideologies embedded in course readings, presentations, and artifacts, including those course materials that are at odds with personal beliefs and values.

Students seeking support around these issues can find more information and resources at http://www.uwb.edu/diversity.

## Student Support Services 
- Career Services: http://www.uwb.edu/careers, 425-352-3706 
- CSS Tutoring: http://www.uwb.edu/css/advising 
- IT Helpdesk: http://uwbit@uw.edu, 425-352-3456 
- Library: http://library.uwb.edu, 425-352-5340 
- Quantitative Skills Center: http://www.uwb.edu/qsc, 425-352-3170 
- School of STEM Advising: stemadv@uw.edu, 425-352-3746 
- Student Counseling Services: http://www.uwb.edu/studentservices/counseling, 425-352-3183 
- Student Success and Career Services: http://www.uwb.edu/studentservices/successservices, 425-352-3427 
- Writing and Communication Center: http://www.uwb.edu/wacc, 425-352-5253 

