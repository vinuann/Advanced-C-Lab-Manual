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
#include <stdio.h>

int greatest(int a, int b, int c)
{
    int max = a;

    if (b > max)
        max = b;

    if (c > max)
        max = c;

    return max;
}

int main()
{
    int a, b, c, result;

    scanf("%d %d %d", &a, &b, &c);

    result = greatest(a, b, c);

    printf("Greatest number = %d", result);

    return 0;
}

Output:
<img width="153" height="37" alt="image" src="https://github.com/user-attachments/assets/a4d67838-9bd6-4a1c-8ab1-70b4b38015ae" />
<img width="220" height="27" alt="image" src="https://github.com/user-attachments/assets/c6baba56-0595-4902-8427-11607ef42936" />



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
#include <stdio.h>

int main()
{
    int n, k;
    int i, j;
    int and_max = 0, or_max = 0, xor_max = 0;
    int and_val, or_val, xor_val;

    scanf("%d %d", &n, &k);

    for (i = 1; i <= n; i++)
    {
        for (j = i + 1; j <= n; j++)
        {
            and_val = i & j;
            or_val = i | j;
            xor_val = i ^ j;

            if (and_val < k && and_val > and_max)
                and_max = and_val;

            if (or_val < k && or_val > or_max)
                or_max = or_val;

            if (xor_val < k && xor_val > xor_max)
                xor_max = xor_val;
        }
    }

    printf("%d\n", and_max);
    printf("%d\n", or_max);
    printf("%d\n", xor_max);

    return 0;
}

Output:
<img width="62" height="77" alt="image" src="https://github.com/user-attachments/assets/0c028e82-dffb-49d3-8546-3d18278bd7f0" />


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
#include <stdio.h>

int main()
{
    int noshel, noque;
    int shelarr[100][100];
    int nobookarr[100];
    int k, c;

    scanf("%d %d", &noshel, &noque);

    for (k = 0; k < noshel; k++)
    {
        scanf("%d", &nobookarr[k]);

        for (c = 0; c < nobookarr[k]; c++)
        {
            scanf("%d", &shelarr[k][c]);
        }
    }

    for (k = 0; k < noque; k++)
    {
        int shelf, book;

        scanf("%d %d", &shelf, &book);

        printf("%d\n", shelarr[shelf][book]);
    }

    return 0;
}

Output:
<img width="180" height="272" alt="image" src="https://github.com/user-attachments/assets/4a8068e6-0985-4683-9051-9b5672d40710" />
<img width="76" height="131" alt="image" src="https://github.com/user-attachments/assets/22371a5e-2e0d-4da4-89b3-6746c5a185f6" />




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
#include <stdio.h>

int main()
{
    int n, i, sum = 0;
    int arr[100];

    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
        sum = sum + arr[i];
    }

    printf("%d", sum);

    return 0;
}


Output:
<img width="162" height="65" alt="image" src="https://github.com/user-attachments/assets/7f78b406-ce7d-4664-a66f-f076b0598391" />
<img width="86" height="41" alt="image" src="https://github.com/user-attachments/assets/1b445c0b-99a4-47cb-be3f-f394457ab4b0" />



 


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
#include <stdio.h>

int main()
{
    char str[200];
    int i, count = 0;

    fgets(str, sizeof(str), stdin);

    for (i = 0; str[i] != '\0'; i++)
    {
        if (str[i] == ' ' && str[i + 1] != ' ')
            count++;
    }

    if (str[0] != '\n')
        count++;

    printf("%d", count);

    return 0;
}
Output:
<img width="197" height="33" alt="image" src="https://github.com/user-attachments/assets/35de7e81-a91e-4be2-9166-4a9921a8ca76" />
<img width="65" height="40" alt="image" src="https://github.com/user-attachments/assets/668adf98-ef0d-468d-b9b0-724320f00c0c" />





Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
