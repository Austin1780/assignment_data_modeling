# assignment_data_modeling
Mmmmm.... dataaaaa....
Jeffrey Dederick
*Include your ERM modeling "pseudocode" in the space below*


Goals: Users need to be able to access all courses
       Each course needs to be able to access all lessons.

1)  Entities: courses
            lessons

  Attributes: course id (integer)
              course title (string 12-36)
              course description (string 100max)

              lesson id (integer)
              lesson title (string 12-36)
              lesson body (string 10,000max)

  Relationships: 1 course to many lessons

2)
