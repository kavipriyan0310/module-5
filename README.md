# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    float length, width, area;
    float *ptr_length, *ptr_width;
    ptr_length = &length;
    ptr_width = &width;
    printf("Enter length of the rectangle: ");
    scanf("%f", ptr_length);
    printf("Enter width of the rectangle: ");
    scanf("%f", ptr_width);
    area = (*ptr_length) * (*ptr_width);
    printf("The area of the rectangle is: %.2f\n", area);
    return 0;
}
```

## OUTPUT
		       	
<img width="806" height="327" alt="image" src="https://github.com/user-attachments/assets/edb53218-f6d1-46ef-aed9-5bb07297ef22" />


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
       char *str;
       str = (char *)malloc(8 * sizeof(char)); 
if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1; 
    }
    strcpy(str, "WELCOME");
    printf("%s\n", str);
    free(str);
    return 0;
}
```
## OUTPUT
<img width="798" height="298" alt="image" src="https://github.com/user-attachments/assets/41e67058-5e3f-4ad7-b77e-511703099126" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct student {
    char name[50];
    int roll_number;
    float marks;
};

int main() {
    struct student s;  
    printf("Enter student's name: ");
    fgets(s.name, sizeof(s.name), stdin); 
    printf("Enter student's roll number: ");
    scanf("%d", &s.roll_number);
    printf("Enter student's marks: ");
    scanf("%f", &s.marks);
    printf("\nStudent Information:\n");
    printf("Name: %s", s.name);
    printf("Roll Number: %d\n", s.roll_number);
    printf("Marks: %.2f\n", s.marks);
    return 0;
}
```


## OUTPUT

<img width="797" height="447" alt="image" src="https://github.com/user-attachments/assets/c3dcc548-4738-4a82-bf60-f0e112c99db1" />

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct employee {
    char name[50];
    int id;
    float basic_salary;
    float hra;      
    float da;        
    float gross_salary;
};
void calculate_gross_salary(struct employee *e) {
    e->hra = 0.20 * e->basic_salary;
    e->da = 0.10 * e->basic_salary;
    e->gross_salary = e->basic_salary + e->hra + e->da;
}

int main()
{
    struct employee emp[3]; 
    int i;
    for(i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d\n", i + 1);
        printf("Enter name: ");
        getchar(); 
        fgets(emp[i].name, sizeof(emp[i].name), stdin);
        printf("Enter ID: ");
        scanf("%d", &emp[i].id);
        printf("Enter basic salary: ");
        scanf("%f", &emp[i].basic_salary);
        calculate_gross_salary(&emp[i]);
    }
    printf("\nEmployee Details and Gross Salary:\n");
    for(i = 0; i < 3; i++) {
        printf("\nEmployee %d\n", i + 1);
        printf("Name: %s", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("HRA: %.2f\n", emp[i].hra);
        printf("DA: %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

    return 0;
}
```


## OUTPUT
<img width="554" height="750" alt="image" src="https://github.com/user-attachments/assets/b7d34d99-c1e6-44be-a4e7-a81e7371c552" />
<img width="758" height="349" alt="image" src="https://github.com/user-attachments/assets/a7318ed2-8dbc-4c81-a47e-9b4a7ca1e43b" />
<img width="549" height="764" alt="image" src="https://github.com/user-attachments/assets/2a9839b2-f813-4e4a-8041-c2afbaa97383" />

<img width="737" height="263" alt="image" src="https://github.com/user-attachments/assets/049aeb99-2110-4d76-8267-eb8d9fdab889" />


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


