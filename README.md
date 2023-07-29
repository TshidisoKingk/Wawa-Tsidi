# Wawa-Tsidi 
These line import the necessary modules ( import random)
The producer must produce data that contains student information and store the data
in a ITstudents class.
The member variables of the ITstudent class must be generated using a random
generating algorithm. The variables include Student Name, Student ID (8 digits),
Programme, a list of Courses and the associated mark for each course.
The producer must wrap the student information into XML format. The names of the
XML files shall be captioned with numbers between 1-10. For example, student1.xml.
The producer will place the XML file in directory it shares with the buffer. Each time the
producer shares information with the buffer, it must insert an integer that corresponds
to the file name to the buffer/queue. For example, if the file added is student1.xml, 1
must be inserted to the buffer.
The Consumer
The consumer reads the content of the xml file it shares with the buffer.
The consumer must unwrap an XML file and gather the XML file student information
into a ITstudent class.
The consumer must clear the content of the xml file (or delete the file). Each time the
consumer removes/clears an XML file. The consumer must also remove the integer
from the buffer.
On the ITstudent class, the consumer must calculate the average mark based on the
marks allocated to the courses. The consumer must determine whether the student
passed or failed. The pass mark is 50%.
The consumer must print on the screen the following: the student’s name, Student ID,
Programme, Courses and the associated marks, the average, and the Pass/Fail
information.
The Buffer
The buffer is a shared common finite container with a maximum size of 10 elements.
The rules for access to the buffer are as follows:
1. The Producer process should not produce any data when the shared buffer is
full.
2. The Consumer process should not consume any data when the shared buffer
is empty.
3. The access to the shared buffer should be mutually exclusive i.e., at a time only
one process
