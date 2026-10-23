# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```

#include <stdio.h>
#include <string.h>
#include <ctype.h>

void main()
{
    char plain1[10], cipher1[10];
    char plain2[10], cipher2[10];
    int key, i, length;

    printf("\n Enter the first plain text: ");
    scanf("%9s", plain1);

    printf("\n Enter the second plain text: ");
    scanf("%9s", plain2);

    printf("\n Enter the key value: ");
    scanf("%d", &key);

    printf("\n\t PLAIN TEXT 1: %s", plain1);
    printf("\n\t ENCRYPTED TEXT 1: ");

    length = strlen(plain1);

    for (i = 0; i < length; i++)
    {
        cipher1[i] = plain1[i] + key;

        if (isupper(plain1[i]) && cipher1[i] > 'Z')
            cipher1[i] -= 26;

        if (islower(plain1[i]) && cipher1[i] > 'z')
            cipher1[i] -= 26;

        printf("%c", cipher1[i]);
    }
    cipher1[length] = '\0';

    printf("\n\t AFTER DECRYPTION 1: ");

    for (i = 0; i < length; i++)
        printf("%c", cipher1[i] - key);

    printf("\n\n\t PLAIN TEXT 2: %s", plain2);
    printf("\n\t ENCRYPTED TEXT 2: ");

    length = strlen(plain2);

    for (i = 0; i < length; i++)
    {
        cipher2[i] = plain2[i] + key;

        if (isupper(plain2[i]) && cipher2[i] > 'Z')
            cipher2[i] -= 26;

        if (islower(plain2[i]) && cipher2[i] > 'z')
            cipher2[i] -= 26;

        printf("%c", cipher2[i]);
    }
    cipher2[length] = '\0';

    printf("\n\t AFTER DECRYPTION 2: ");

    for (i = 0; i < length; i++)
        printf("%c", cipher2[i] - key);

    printf("\n");
}

```

## OUTPUT:

<img width="1895" height="890" alt="image" src="https://github.com/user-attachments/assets/233453c5-3433-49c9-b541-a708f4616519" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
