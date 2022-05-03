
class Course {
        
	Long id;
	String name;
	@manyToMany
	List<Subject> subject;
}


class Subject {
	
	Long id;
	String name;
}

class Examination {
	
	String name;
	Date examDate;
	
	@ManyToOne
	Subject subject;
	
	@ManyToOne
	Course course;
	
}

class ExamResult {
	
	@ManyToOne
	Student student;
	
	@ManyToOne
	Examination examinaion;
		
	Double marks;
	
	
}



class Student {

    //Other Attributes

	@ManyToOne
	Course courses;	

}


class Teacher {
	
	//Other Attributes
	@ManyToMany
	List<Course> courses;

	@ManyToMany
	List<Subject> subject;
}
