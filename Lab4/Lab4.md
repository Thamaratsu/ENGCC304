## โจทย์
เขียนโปรแกรมภาษาซีเพื่อรับข้อมูลพนักงานของบริษัทซอร์ฟแวร์ โดยรับข้อมูล รหัสประจำตัวพนักงาน , จำนวนชั่วโมงที่ทำงาน , รายได้ต่อชั่วโมง จากนั้นให้แสดงข้อมูลเลขประจำตัวพนักงาน พร้อมกับรายได้ทั้งหมดที่หนักงานจะได้รับทั้งหมด

## FIX CODE
```c++
#include <stdio.h>
int main() {

    char EmID[11] ;
    int Whrs ;
    float salaryhrs ;

    printf("Input the Employees ID(Max. 10 chars):");
    scanf("%10s", EmID);
    int c;
    while ((c = getchar()) != '\n' && c != EOF);

    printf("Input the working hrs:");
    scanf("%d", &Whrs);
    while ((c = getchar()) != '\n' && c != EOF);

    printf("Salary amount/hr:");
    scanf("%f", &salaryhrs);
    while ((c = getchar()) != '\n' && c != EOF);

    printf("\n");
    printf("Employees ID = %s\n", EmID);
    printf("Salary = U$ %.2f", Whrs*salaryhrs);
   
    return 0;
}
```

## TEST CASE 1
### Input
```bash
Input the Employees ID(Max. 10 chars): 
0342
Input the working hrs: 
8
Salary amount/hr: 
15000

```
### Output
```bash
Expected Output:
Employees ID = 0342
Salary = U$ 120000.00
```
<img width="629" height="895" alt="image" src="https://github.com/user-attachments/assets/9ba4946c-68c2-4cf2-9568-871e1a262b67" />


## TEST CASE 2
### Input
```bash
Input the Employees ID(Max. 10 chars): 
0000500349
Input the working hrs: 
11
Salary amount/hr: 
34000

```
### Output
```bash
Expected Output:
Employees ID = 0000500349
Salary = U$ 374000.00
```
<img width="724" height="911" alt="image" src="https://github.com/user-attachments/assets/0cc43bcc-722e-423b-ada8-98059b32fa1e" />

