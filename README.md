# c-program-assignment

1. Write a C program to find the maximum of three numbers without using logical operators.
 
    #include <stdio.h>
   
    int main()
   
    {
    
    int a, b, c, max;
   
    printf("Enter three numbers: ");
   
    scanf("%d %d %d", &a, &b, &c);

    max = a;

    if (b > max)
        max = b;

    if (c > max)
        max = c;

    printf("Maximum = %d", max);

    return 0;
   
}

3.  Write a  C program to check whether the given year is leap year or not by adding century leap year or non-century leap year in the output (Eg: 2000 is a century leap year, 2024 is a non-century leap year)

    #include <stdio.h>

    int main()
    
    {
    int year;
    

    printf("Enter year: ");
    scanf("%d", &year);

    if (year % 400 == 0)
        printf("%d is a century leap year", year);

    else if (year % 100 == 0)
        printf("%d is not a leap year", year);

    else if (year % 4 == 0)
        printf("%d is a non-century leap year", year);

    else
        printf("%d is not a leap year", year);

    return 0;
    
}
