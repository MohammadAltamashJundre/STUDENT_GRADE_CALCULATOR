# STUDENT_GRADE_CALCULATOR
STUDENT GRADE CALCULATOR
import java.util.Scanner;
public class task2 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String[] subjects = {"Math", "Science", "English", "History","Hindi","Marathi"};
        int[] marks = new int[subjects.length];
        int totalMarks = 0;
        for (int i = 0; i < subjects.length; i++) {
            System.out.print("Enter marks obtained in " + subjects[i] + ": ");
            marks[i] = scanner.nextInt();
            totalMarks += marks[i];
        }
        double averagePercentage = (double) totalMarks / subjects.length;
        String grade;
        if (averagePercentage >= 90) {
            grade = "A+";
        } else if (averagePercentage >= 80) {
            grade = "A";
        } else if (averagePercentage >= 70) {
            grade = "B";
        } else if (averagePercentage >= 60) {
            grade = "C";
        } else {
            grade = "D";
        }

        // Display Results
        System.out.println("Total Marks: " + totalMarks);
        System.out.println("Average Percentage: " + averagePercentage + "%");
        System.out.println("Grade: " + grade);

        scanner.close();
    }
}
