# encryptix2
import java.util.Scanner;

public class Studentgradecalculator
{

    public static void main(String[] args) 
    {   

System.out.println("----------Check Student Grade Here!----------");
System.out.print("Enter the Number of Total Subjects you have : ");
        Scanner scanner = new Scanner(System.in);
        int Num_of_SUB = scanner.nextInt();

        if (Num_of_SUB<= 0)
        {
System.out.println("Invalid number of Subjects.");
            return;
        }

        double TotalMarks = 0;

        for (int i = 1; i<= Num_of_SUB; i++) 
        {
System.out.print("Enter the marks for subject "+i+" i.e (subject name) ");
            Scanner sc = new Scanner(System.in);
            String sub = sc.nextLine();
System.out.print("= ");
            double marks = scanner.nextDouble();

            while (marks < 0 || marks > 100) 
            {
System.out.println("Enter the marks between 0 and 100.");
System.out.print("Enter the marks for subject " + i + ": ");
                marks = scanner.nextDouble();
            }

TotalMarks += marks;
        }

       double AveragePercentage = TotalMarks / Num_of_SUB;
System.out.printf("The Average Percentage is = "+AveragePercentage+"\n");

       if (AveragePercentage>= 95) {
System.out.println("Grade Assign : A+");
        } 
        else if (AveragePercentage>= 90) {
System.out.println("Grade Assign : A");
        } 
        else if (AveragePercentage>= 85) {
System.out.println("Grade Assign : B+");
        } 
        else if (AveragePercentage>= 80) {
System.out.println("Grade Assign : B");
        } 
        else if (AveragePercentage>= 70) {
System.out.println("Grade Assign : C");
        }
        else if (AveragePercentage>=35 &&AveragePercentage<=69) {
System.out.println("Grade Assign : D");
        }
        else {
System.out.println("Grade Assign: Fail");
        }
scanner.close();
    }
}

