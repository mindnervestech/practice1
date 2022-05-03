**//practice1/csv/Student Data.csv
POST /api/upload/studentdata**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV 

	- Check is the class exits in the Course table or not
	- If class does not exists in the Course table create new Course
	- Save student entity along with the Course

=================================================

**//practice1/csv/Teacher Data.csv
POST /api/upload/teacherdata**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV 
	- Save teacher entity	`


=================================================
**//practice1/csv/Subject Teacher Data.csv
POST /api/upload/teacherSubjectData**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV 
	- Check is the subject exits in the Subject table or not
	- If subject does not exists in the Subject table create new Subject
	- Get the Teacher by id (teacherRepository.findById)
	- If Teacher is found add subject to List<Subject> subject

=================================================	
**//practice1/csv/Class Teacher Mapping.csv
POST /api/upload/teacher_subject_data**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV 
	- Get the Teacher by id (teacherRepository.findById)
	- Get the Course by id (courseRepository.findById)
	- If Teacher is found AND Course is found then add course to List<Course> course

=================================================

**//practice1/csv/subject_course	
POST /api/upload/course_subject_data**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV 
	- Get the Subject by id 
	- Get the Course by id 
	- If Course is found AND Subject is found then add subject to List<Subject> subject in Course entity

==================================================	

**//practice1/csv/Exam Data.csv	
POST /api/upload/exam_data**

- Parse CSV file
- User some libary like opencsv to read the csv file. 
- For each record of the CSV
	- Find in the Examination by Subject and Exam_date
		- If does not exits then create new Examination record with name = Concat (Subject , exam_date)
		- get the referance of examination object
		- Get the student object by id.
		- Save the record in ExamResult by saving student, examination and marks

==================================================
