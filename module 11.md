

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
//type your code here
```
#include<stdio.h>
int main(){
    int a,b,c,d;
    scanf("%d %d %d %d",&a,&b,&c,&d);
    if(a>b&&a>c&&a>d){
        printf("%d",a);
        
    }
    else if(b>a&&b>c&&b>d){
        printf("%d",b);
    }
    else if(c>a&&c>b&&c>d){
        printf("%d",c);
        
    }
    else if(d>a&&d>b&&d>c){
        printf("%d",d);
    }
}

```
Output:
//paste your output here
<img width="694" height="421" alt="image" src="https://github.com/user-attachments/assets/4864b211-a776-48af-ac4a-9cae22c363a6" />


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
//type your code here
```
#include<stdio.h>
void cal_max(int n, int k){

    int max_and=0,max_or=0,max_xor=0;
    for(int a=1;a<=n;a++){
        for(int b=a+1;b<=n;b++){
            int and_val=a&b;
            int or_val=a|b;
            int xor_val=a^b;
            if(and_val<k&&and_val>max_and)max_and=and_val;
            if (or_val < k && or_val > max_or)   max_or = or_val;
            if (xor_val < k && xor_val > max_xor) max_xor = xor_val;
        }
    }
    printf("%d\n%d\n%d\n",max_and,max_or,max_xor);
}



int main(){
    int n,k;
    scanf("%d %d",&n,&k);
    cal_max(n,k);
    return 0;
}
```

Output:
//paste your output here
<img width="709" height="471" alt="image" src="https://github.com/user-attachments/assets/0bd8f366-5d8d-469d-b164-23fa4f3bbf93" />


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
//type your code here
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);

    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);

    int *total_number_of_books = calloc(total_number_of_shelves, sizeof(int));

    int **total_number_of_pages = malloc(total_number_of_shelves * sizeof(int*));

    for (int i = 0; i < total_number_of_shelves; i++) {
        total_number_of_pages[i] = NULL;  // initially no books
    }

    for (int q = 0; q < total_number_of_queries; q++) {
        int type;
        scanf("%d", &type);

        if (type == 1) {
            int x, y;
            scanf("%d %d", &x, &y);

            int books = total_number_of_books[x];
            total_number_of_pages[x] = realloc(total_number_of_pages[x], (books + 1) * sizeof(int));
            total_number_of_pages[x][books] = y;
            total_number_of_books[x]++;

        } else if (type == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", total_number_of_pages[x][y]);

        } else if (type == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", total_number_of_books[x]);
        }
    }

    for (int i = 0; i < total_number_of_shelves; i++) {
        free(total_number_of_pages[i]);
    }
    free(total_number_of_books);
    free(total_number_of_pages);

    return 0;
}
```
Output:
//paste your output here
<img width="764" height="452" alt="image" src="https://github.com/user-attachments/assets/049a99d7-93ef-46da-8ccc-3a60bf125f39" />


Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
//type your code here
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, i;
    int *arr;   
    int sum = 0;

    scanf("%d", &n);

    arr = (int *)malloc(n * sizeof(int));

    
    if (arr == NULL) {
        printf("Memory allocation failed!");
        return 1;
    }

    // Read n integers from input
    for (i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

   
    for (i = 0; i < n; i++) {
        sum += arr[i];
    }

    printf("%d", sum);

    
    free(arr);

    return 0;
}

```

Output:
//paste your output here
<img width="728" height="372" alt="image" src="https://github.com/user-attachments/assets/2ff15c71-07fd-448b-a8c8-94607968cca8" />


 


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A      SENTENCE



Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
//type your code here
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char sentence[200];
    int i, count = 0;
    int inWord = 0; // Flag to track if currently inside a word

    // Step 1: Input the sentence
    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin); // safer than gets()

    // Step 3: Process each character
    for (i = 0; sentence[i] != '\0'; i++) {
        // Check if the character is a letter or digit (part of a word)
        if (!isspace(sentence[i]) && sentence[i] != '.' && sentence[i] != ',' && sentence[i] != '!' && sentence[i] != '?') {
            if (inWord == 0) {  // first character of a new word
                count++;
                inWord = 1;
            }
        } else {
            inWord = 0;  // space or punctuation ends a word
        }
    }

    // Step 5: Display result
    printf("Number of words in the given sentence: %d\n", count);

    return 0;
}
```

Output:
//paste your output here

<img width="503" height="223" alt="image" src="https://github.com/user-attachments/assets/a506b762-5dac-4ee9-acc9-45196dd9fe87" />


Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
