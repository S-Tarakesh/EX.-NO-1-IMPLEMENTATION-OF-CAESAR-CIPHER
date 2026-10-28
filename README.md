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
 
int main() { 
	char input[1000]; 
	int key; 
	char temp[1000]; 
 
	printf("Enter plain text: "); 
	fgets(input,sizeof(input),stdin); 
 
	printf("Enter key: "); 
	scanf("%d", &key); 
 
	strcpy(temp, input); 
 
	key = ((key % 26) + 26) % 26; 
 
	for (int i = 0; temp[i] != '\0'; i++) { 
    	if (isupper((unsigned char)input[i])) { 
        	input[i] = (char)('A' + (input[i] - 'A' + key) % 26); 
    	} 
    	else if (islower((unsigned char)input[i])) { 
        	input[i] = (char)('a' + (input[i] - 'a' + key) % 26); 
    	} 
	} 
	printf("Cipher is %s\n", input); 
	for (int i = 0; temp[i] != '\0'; i++) { 
    	if (isupper((unsigned char)input[i])) { 
        	input[i] = (char)('A' + (input[i] - 'A' - key) % 26); 
    	} 
    	else if (islower((unsigned char)input[i])) { 
        	input[i] = (char)('a' + (input[i] - 'a' - key) % 26); 
    	} 
	} 
	printf("Plain Text is %s\n",input); 
	return 0; 
}
```
## OUTPUT:
<img width="1266" height="711" alt="image" src="https://github.com/user-attachments/assets/55e9ea25-0ed1-4b85-887e-81aba91f62b9" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
