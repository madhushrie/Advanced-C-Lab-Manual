EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:

//type your code here
```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    if (n == 1) {
        printf("one\n");
    } else if (n == 2) {
        printf("two\n");
    } else if (n == 3) {
        printf("three\n");
    } else if (n == 4) {
        printf("four\n");
    } else if (n == 5) {
        printf("five\n");
    } else if (n == 6) {
        printf("six\n");
    } else if (n == 7) {
        printf("seven\n");
    } else if (n == 8) {
        printf("eight\n");
    } else if (n == 9) {
        printf("nine\n");
    } else {
        printf("Greater than 9\n");
    }

    return 0;
}
```




Output:
<img width="863" height="361" alt="image" src="https://github.com/user-attachments/assets/697d5292-932a-44c8-a106-4989a00be3bf" />

//paste your output here






Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

//type your code here
```
#include <stdio.h>

int main() {
    char a[50];
    int i, h, c;

    printf("Enter a string containing digits: ");
    scanf("%s", a);

    
    for (h = 0; h <= 3; h++) {
        c = 0; 
        for (i = 0; a[i] != '\0'; i++) {
            if (a[i] == ('0' + h)) {
                c++;
            }
        }
        printf("%d ", c); 
    }

   
    for (h = 4; h <= 9; h++) {
        printf("0 ");
    }

    printf("\n");  
    return 0;
}
```




Output:


//paste your output here

<img width="640" height="182" alt="image" src="https://github.com/user-attachments/assets/349f8e30-4408-48f2-a121-bdb65142d7b0" />





Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

//type your code here
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>


void swap(char **x, char **y) {
    char *temp = *x;
    *x = *y;
    *y = temp;
}

// Function to compare two strings (used for qsort)
int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}
void permute(char **s, int l, int r) {
    int i;
    if (l == r) {
        for (i = 0; i <= r; i++) {
            printf("%s ", s[i]);
        }
        printf("\n");
    } else {
        for (i = l; i <= r; i++) {
            swap(&s[l], &s[i]);
            permute(s, l + 1, r);
            swap(&s[l], &s[i]); 
        }
    }
}

int main() {
    char **s;   
    int n, i;

    // Step 4: Input number of strings
    printf("Enter number of strings: ");
    scanf("%d", &n);

    
    s = (char **)malloc(n * sizeof(char *));
    if (s == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    
    for (i = 0; i < n; i++) {
        s[i] = (char *)malloc(50 * sizeof(char));  
        if (s[i] == NULL) {
            printf("Memory allocation failed!\n");
            return 1;
        }
        printf("Enter string %d: ", i + 1);
        scanf("%s", s[i]);
    }

    
    qsort(s, n, sizeof(char *), compare);

    printf("\nAll permutations in lexicographical order:\n");
    permute(s, 0, n - 1);

    
    for (i = 0; i < n; i++) {
        free(s[i]);
    }
    free(s);

    
    return 0;
}
```




Output:


//paste your output here

<img width="921" height="444" alt="image" src="https://github.com/user-attachments/assets/e0192cbf-08ce-4bda-9c0b-a74ceea69c90" />





Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

//type your code here
```
#include <stdio.h>

int main() {
    int n, i, j, min;
    
    
    printf("Enter value of n: ");
    scanf("%d", &n);
    
    
    int len = n * 2 - 1;

    
    for (i = 0; i < len; i++) {
        for (j = 0; j < len; j++) {
            
            int top = i;
            int left = j;
            int right = len - 1 - j;
            int bottom = len - 1 - i;
            min = top;
            if (left < min) min = left;
            if (right < min) min = right;
            if (bottom < min) min = bottom;

            
            printf("%d ", n - min);
        }
        printf("\n");
    }

    
    return 0;
}
```




Output:


//paste your output here
<img width="677" height="538" alt="image" src="https://github.com/user-attachments/assets/9973d884-3c2e-4ad6-99c6-a8bb3b8ca3f1" />






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

//type your code here
```
#include <stdio.h>
int square() {
    int num, sq;
    printf("Enter a number: ");
    scanf("%d", &num);

    // Calculate square
    sq = num * num;
    return sq;
}

int main() {
    int result;
    result = square();
    printf("Square of the given number is: %d\n", result);

    
    return 0;
}
```




Output:


//paste your output here

<img width="460" height="190" alt="image" src="https://github.com/user-attachments/assets/685abd65-a6dc-4555-a30a-facc64bf91c9" />





Result:
Thus, the program is verified successfully



























