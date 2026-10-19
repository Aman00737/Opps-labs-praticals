# PROJECT -1 Classes and Objects 
Create a Java class named Student with fields for roll number, name, and marks in three subjects. Add a constructor and methods to calculate total marks, percentage, and display the student details. Create at least three Student objects and display their details. Identify the class, objects, instance variables, constructor, and methods in your program.

class Student {
    // Instance variables
    int rollNo;
    String name;
    int marks1, marks2, marks3;

    // Constructor
    Student(int rollNo, String name, int marks1,
            int marks2, int marks3) {
        this.rollNo = rollNo;
        this.name = name;
        this.marks1 = marks1;
        this.marks2 = marks2;
        this.marks3 = marks3;
    }

    // Method to calculate total marks
    int calculateTotal() {
        return marks1 + marks2 + marks3;
    }

    // Method to calculate percentage
    double calculatePercentage() {
        return calculateTotal() / 3.0;
    }

    // Method to display student details
    void displayDetails() {
        System.out.println("Roll Number: " + rollNo);
        System.out.println("Name: " + name);
        System.out.println("Marks in Subject 1: " + marks1);
        System.out.println("Marks in Subject 2: " + marks2);
        System.out.println("Marks in Subject 3: " + marks3);
        System.out.println("Total Marks: " + calculateTotal());
        System.out.println("Percentage: "
                           + calculatePercentage() + "%");
        System.out.println("----------------------------");
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating three Student objects
        Student s1 = new Student(101, "Aman", 85, 90, 80);
        Student s2 = new Student(102, "Priya", 92, 88, 95);
        Student s3 = new Student(103, "Rahul", 75, 80, 85);

        // Displaying student details
        s1.displayDetails();
        s2.displayDetails();
        s3.displayDetails();
    }
}
