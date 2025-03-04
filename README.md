# Student_grade_tracker
import java.util.Scanner;

public class StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Ask how many subjects
        System.out.print("Enter the number of subjects: ");
        int numSubjects = scanner.nextInt();

        // Array to store the grades
        double[] grades = new double[numSubjects];

        // Input grades from the user
        for (int i = 0; i < numSubjects; i++) {
            System.out.print("Enter grade for subject " + (i + 1) + ": ");
            grades[i] = scanner.nextDouble();
        }

        // Calculate the average grade
        double sum = 0;
        double highest = grades[0];
        double lowest = grades[0];

        for (int i = 0; i < numSubjects; i++) {
            sum += grades[i];
            if (grades[i] > highest) {
                highest = grades[i];
            }
            if (grades[i] < lowest) {
                lowest = grades[i];
            }
        }

        double average = sum / numSubjects;

        // Output the results
        System.out.println("\nResults:");
        System.out.println("Average grade: " + average);
        System.out.println("Highest grade: " + highest);
        System.out.println("Lowest grade: " + lowest);

        scanner.close();
    }
}
