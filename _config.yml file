package project;

import java.util.ArrayList;
import java.util.Scanner;

// Student class to hold application details
class Student {
    private String name;
    private int age;
    private String course;

    public Student(String name, int age, String course) {
        this.name = name;
        this.age = age;
        this.course = course;
    }

    public void display() {
        System.out.println("Name: " + name + ", Age: " + age + ", Course: " + course);
    }
}

// Main application class
public class college-application{
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<Student> applications = new ArrayList<>();

        System.out.println("=== College Application System ===");

        while (true) {
            System.out.println("\n1. New Application");
            System.out.println("2. View All Applications");
            System.out.println("3. Exit");
            System.out.print("Enter your choice: ");
            int choice = 0;
            try {
                choice = Integer.parseInt(scanner.nextLine());
            } catch (Exception e) {
                System.out.println("Invalid input. Please enter a number.");
                continue;
            }

            switch (choice) {
                case 1:
                    // New Application
                    System.out.print("Enter student name: ");
                    String name = scanner.nextLine();
                    System.out.print("Enter age: ");
                    int age = 0;
                    try {
                        age = Integer.parseInt(scanner.nextLine());
                    } catch (Exception e) {
                        System.out.println("Invalid age. Application cancelled.");
                        break;
                    }
                    System.out.print("Enter course applied for: ");
                    String course = scanner.nextLine();
                    Student student = new Student(name, age, course);
                    applications.add(student);
                    System.out.println("Application submitted successfully!");
                    break;
                case 2:
                    // View All Applications
                    if (applications.isEmpty()) {
                        System.out.println("No applications found.");
                    } else {
                        System.out.println("\nList of Applications:");
                        for (Student s : applications) {
                            s.display();
                        }
                    }
                    break;
                case 3:
                    // Exit
                    System.out.println("Thank you for using the College Application System!");
                    scanner.close();
                    return;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
    }
}
