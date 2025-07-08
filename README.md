# Group: CECS-savages
# CS50 Summer 2025, Activities 3-4

## Activity 3

![Visualizing Git](./VisualizingGit.png)

## Activity 4 Part 1
```
#include <stdio.h>
#include <math.h>

int main(int argc, char *argv[])
{
  int width=24,
  		length=11;

  
  // print out the area of the box defined by width and length
  // it should look like 
  // 		A box of width #### and length #### has an area of ####.
  int area = width * length;
  
  printf("A box of width %d and length %d has an area of %d.", width, length, area);

  // calculate the length of a diagonal (hint: think Pythagoras)
  // and print it with two decimal places
  
  double diagonal = sqrt((width * width) + (length * length));
  printf("The diagonal has length %.2f", diagonal);
}
```
## Activity 4 Part 2
```
#include <stdio.h>

int main()
{
    int a = 2;

    if (a == 2)
 		    printf("value of a is %d", a);
 
    else printf("value of a is not equal to 2 ");
}
```
## Activity 4 Part 3

#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[])
{
  int temp=0,
      odd=0;
  char answer[5];
  // printf("%s",argv[1]);
  // printf("%d\n", sscanf(argv[1], "%d", &temp));

  if (argc==2) {
    if (1==sscanf(argv[1], "%d", &temp)) { //if succesfully inputted an integer
      // determine whether the # is even or odd with one operator
      // if it's odd, set odd to 1 
     if (1==temp%2){
        odd = 1;
     } 
      
     if (odd) {
        strncpy(answer,"Odd", sizeof(answer));
      }
      else {
        strncpy(answer, "Even", sizeof(answer));
      }
      puts(answer);
      return(0);
    }
  }
	else {
  	fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
  	return 1;
	}
}

## Activity 4 Part 4
```
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[])
{
  int sum=0, max=0;
  if (argc==2) {
    if (1==sscanf(argv[1], "%d", &max)) {
      
			// make sure the max is valid
      if (max >= 1) {
      // use a loop to calculate the sum
        for (int i = 1; i <= max; i++) {
          sum += i; 
        }
      }
  		// display the answer
      printf("The sum of the numbers 1 through %d is %d\n", max, sum);
    }
    else {
      // user entered a non-number, so issue error message and exit
      fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
      return 1;
    }
  }
	else {
  	fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
  	return 1;
	}
}
```
## Activity 4 Part 5
```
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[])
{
  int year = 0;
  if (argc==2) { // check if user inputted one argument
    if (1==sscanf(argv[1], "%d", &year)) { // check if argument is int
      // check if year is a leap year
      if ((year % 4 == 0 && year % 100 != 0) || year % 400 == 0){
        printf("The year %d is a leap year\n", year);
      }
      else{
        printf("The year %d is not a leap year\n", year);
      }
    }
    else{
      fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
      return 1;
    }
  }
  else {
    fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
    return 1;
  }
}
```
## Activity 4 Part 6
```
#include <stdio.h>
#include <string.h>

int main(void)
{
    printf("char: %zu bytes\n", sizeof(char));
    printf("int: %zu bytes\n", sizeof(int));
    printf("short: %zu bytes\n", sizeof(short));
    printf("long: %zu bytes\n", sizeof(long));
    printf("float: %zu bytes\n", sizeof(float));
    printf("double: %zu bytes\n", sizeof(double));
    return 0;
}
```
## Activity 4 Part 7
```
#include <stdio.h>
#include <string.h>

int main(int argc, char *argv[]){
  int rows = 0;
  if (argc==2) {
    if (1==sscanf(argv[1], "%d", &rows)) {
	// print the pyramid
      for (int i = 1; i<=rows; i++){
        for (int j=1; j<=i; j++){
          printf("%d ",i);
        }
        printf("\n");
      }
    }
    else {
  	  fprintf(stderr,"Please input a positive integer");
  	  return 1;
	  } 
  }
  else {
  	fprintf(stderr,"Usage: %s num , where num is an integer\n", argv[0]);
  	return 1;
	}
}
```
