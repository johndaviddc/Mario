# Pyramid Builder
This program builds a pyramid using the "#" character, based on user input for height between 1 and 8.

## How to Use
1. Compile the program using a C compiler
2. Run the program in your terminal
3. Enter a height between 1 and 8
4. The program will output a pyramid using "#" character

## Code Example
```sh
#include "cs50.h"
#include <stdio.h>

int main(void)
{
    int height;

    // Prompt the user for a height between 1 and 8
    do
    {
        height = get_int("Height: ");
    }
    while (height < 1 || height > 8);

    // Build the pyramid
    for (int i = 1; i <= height; i++)
    {
        // Print spaces
        for (int j = height - i; j > 0; j--)
        {
            printf(" ");
        }
        // Print hashes
        for (int j = 0; j < i; j++)
        {
            printf("#");
        }
        // Print gap
        printf("  ");
        // Print hashes
        for (int j = 0; j < i; j++)
        {
            printf("#");
        }
        // Go to the next line
        printf("\n");
    }

    return 0;
}
```

## Sample Output
```sh
Height: 4
   #  #
  ##  ##
 ###  ###
####  ####
```
