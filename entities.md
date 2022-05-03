
class Course {
	String name;
}


class Subject {
	String name;
}

class Exam {
	
	@ManyToOne
	Student student;
	
	Date examDate;
	
	Double marks;
	
	@ManyToOne
	Subject subject;

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
