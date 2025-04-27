# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
~~~c
#include <stdio.h>
#include <math.h> 
void calculateEMI(float principal, float rate, int time) {
    float monthlyRate, emi;
    int months;
    monthlyRate = rate / (12 * 100); 
    months = time * 12;              
    emi = (principal * monthlyRate * pow(1 + monthlyRate, months)) / (pow(1 + monthlyRate, months) - 1);
    printf("Monthly EMI = %.2f\n", emi);
}
int main() {
    float principal, rate;
    int time;
    printf("Enter loan amount (principal): ");
    scanf("%f", &principal);
    printf("Enter annual interest rate (in %%): ");
    scanf("%f", &rate);
    printf("Enter loan period (in years): ");
    scanf("%d", &time);
    calculateEMI(principal, rate, time);
    return 0;
}
~~~

## OUTPUT

![Screenshot 2025-04-27 112320](https://github.com/user-attachments/assets/af405990-b6da-4f30-9010-9b41401ae374)




## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
~~~c
#include <stdio.h>
int main() {
    int n = 6; 
    int first = 0, second = 1, next, i;
    printf("Fibonacci Series up to %d terms:\n", n);
    for(i = 0; i < n; i++) {
        if(i == 0) {
            printf("%d ", first);
        } else if(i == 1) {
            printf("%d ", second);
        } else {
            next = first + second;
            printf("%d ", next);
            first = second;
            second = next;
        }
    }
    printf("\n");
    return 0;
}
~~~


## OUTPUT


![Screenshot 2025-04-27 112559](https://github.com/user-attachments/assets/9c9ddea1-df89-4a43-a535-acb6445d32fd)






## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
~~~c
#include <stdio.h>
int main() {
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    printf("The last element of the array is: %d\n", arr[n-1]);
    return 0;
}
~~~

## OUTPUT

![Screenshot 2025-04-27 112903](https://github.com/user-attachments/assets/513c5eb8-6cdc-4325-abaf-46d62e11a6e3)








## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
~~~c
#include <stdio.h>
int main() {
    int n, count = 0;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    for(int i = 0; i < n; i++) {
        if(arr[i] > 0) {
            count++;
        }
    }
    printf("Total number of positive elements: %d\n", count);
    return 0;
}
~~~

## OUTPUT

![Screenshot 2025-04-27 113205](https://github.com/user-attachments/assets/0dfcb9bc-4ec4-42ce-87c3-59ee5bcc050e)




## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
~~~c
#include <stdio.h>

int main() {
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n]; 
    printf("Enter %d elements:\n", n);
    for(int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    for(int i = 0; i < n; i++) {
        if(arr[i] % 2 == 0) {
            arr[i] = 'E'; 
        }
    }
    printf("Modified array:\n");
    for(int i = 0; i < n; i++) {
        if(arr[i] == 'E') {
            printf("E ");
        } else {
            printf("%d ", arr[i]); 
        }
    }
    printf("\n");
    return 0;
}
~~~
## Output:
 
![Screenshot 2025-04-27 113413](https://github.com/user-attachments/assets/c526cffe-55f0-4c1b-9228-bf5535524228)


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



