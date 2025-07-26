## CODE
```c++
#include <stdio.h>
int main() {

    int score =-1;

    printf("Enter your score :");
    scanf("%d",&score);
    printf("Grade :");
    if (score >= 80) {
        printf("A \n");
    } else if(score >= 75 && score <80) {
        printf("B+\n");
    } else if(score >= 70 && score < 75) {
        printf("B \n");
    } else if(score >= 65 && score < 70) {
        printf("C+\n");
    } else if (score >= 60 && score < 65) {
        printf("C \n");
    } else if(score >= 55 && score < 60) {
        printf("D+\n");
    } else if(score >= 50 && score < 55) {
        printf("D \n");
    } else if(score < 50 && score >= 0) {
        printf("F \n");
    } else {
        printf("please enter number only.");
    }
    return 0;
    
}
```

## TEST CASE
### Input
```bash
enter score :
80
```
### Output
```bash
A !
```
<img width="577" height="208" alt="image" src="https://github.com/user-attachments/assets/724e7cb1-ea8f-4f23-933b-f4e079a0350e" />

## TEST CASE
### Input
```bash
enter score :
55
```
### Output
```bash
D+ !
```
<img width="612" height="200" alt="image" src="https://github.com/user-attachments/assets/dd29baed-9846-4c2a-b3ed-fbe8786598ea" />

## TEST CASE
### Input
```bash
enter score :
64
```
### Output
```bash
C !
```
<img width="538" height="161" alt="image" src="https://github.com/user-attachments/assets/c2d650d5-d9a1-45ac-b3b9-3d4b214566fb" />

## TEST CASE
### Input
```bash
enter score :
44
```
### Output
```bash
F !
```
<img width="576" height="196" alt="image" src="https://github.com/user-attachments/assets/7f9d2b2e-2ebc-4b2e-9a03-131b75cfc9ae" />

## TEST CASE
### Input
```bash
enter score :
hello
```
### Output
```bash
please enter number only.
```
<img width="679" height="223" alt="image" src="https://github.com/user-attachments/assets/efd7349d-9b05-4638-b030-9ebe2278daf8" />
