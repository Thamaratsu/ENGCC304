## โจทย์
จงเขียนโปรแกรมทายตัวเลขซึ่งทำงานดังนี้
- ตอนเริ่มเกมผู้เล่นจะมีคะแนนเต็ม 100
- โปรแกรมจะสุ่มตัวเลขที่มีค่าตั้งแต่ 1 ถึง 100
- ให้ผู้เล่นทายว่าตัวเลขที่โปรแกรมสุ่มมามีค่าเป็นเท่าใด
- หากทายผิด โปรแกรมจะลบคะแนนของผู้เล่นไป 10 หน่วย พร้อมแจ้งคะแนนปัจจุบันให้ผู้เล่นทราบด้วย
- หากทายผิด โปรแกรมจะต้องบอกใบ้ว่าคำตอบที่ถูกมีค่า "มากกว่า" หรือ "น้อยกว่า" ตัวเลขที่ผู้ใช้ทาย
- หากทายผิด ให้โปรแกรมรอรับตัวเลขถัดไปได้เลย
- หากทายถูก ให้โปรแกรมแสดงความยินดีกับผู้ใช้ พร้อมแจ้งคะแนนปัจจุบันให้กับผู้เช่น
- เมื่อเล่นเสร็จโปรแกรมรอรับคำสั่งจากผู้ใช้ หากผู้ใช้กรอกเลข 1 จะเข้าสู่โหมดการเล่นเกมใหม่อีกครั้ง หากกด -1 ให้หยุดการทำงานของโปรแกรม

<br />หมายเหตุ : การสุ่มตัวเลขจะใช้คำสั่ง rand() ที่อยู่ใน stdlib.h หากต้องการสุ่มตัวเลข 0 ถึง 100 ต้องใช้คำสั่งดังนี้
```c++
rand() % 100 + 1
```
<br />หมายเหตุ : หากต้องการสุ่มตัวเลขที่เปลี่ยนแปลงตามเวลา ต้องใช้คำสั่ง srand( time( NULL ) ) ในตอนต้นของโปรแกรมด้วย
```c++
srand( time( NULL ) ) ;
```

## FIX CODE
```c++
#include <stdio.h>
#include <stdbool.h>
#include <time.h>
#include <stdlib.h>


int main() {
    srand( time( NULL ) ) ;
    int random = rand() % 100 + 1;
    int gusnum = 1;
    int score = 100;
    int exit;
    bool start = false;


    do {
        printf("Do you want to play game (1=play, -1=exit): ");

        if (scanf("%d", &exit) != 1) {
             printf("\nPlease enter only 1 or -1.\n");
        while (getchar() != '\n');
            exit = 0;
        } else if (exit == 1) {
            start = true;
        } else if (exit == -1) {
            start = false;
            printf("\nsee you again");
            return 0;
        } else {
            printf("\nPlease enter only 1 or -1.\n");
        }
    } while(exit != 1 && exit != -1);

    while(start = true) {

        printf("(score=%d)\n\n", score);
        printf("Guess the winning number (%d-100)\n", gusnum);
        scanf("%d", &gusnum);

        if(gusnum < random) {
            printf("\nSorry, the winning number is HIGHER than %d", gusnum);
            score -10; 

        } else if(gusnum > random) {
            printf("\nSorry, the winning number is LOWER than %d", gusnum);
            score -10;

        } else if(gusnum == random) {
            printf("\nThat is correct! The winning number is %d\n", gusnum);
            printf("\nScore this game: %d\n", score);
            start = false;

            printf("\nDo you want to play game (1=play, -1=exit): ");

            if (scanf("%d", &exit) != 1) {
                printf("Please enter only 1 or -1.\n");
            while (getchar() != '\n');
                exit = 0;
            } else if (exit == 1) {
                start = true;
            } else if (exit == -1) {
                start = false;
                printf("\nsee you again");
                return 0;
            } else {
                printf("\nPlease enter only 1 or -1.\n");
            }
                
        } 


    }

    
}
```

## TEST CASE
### Input & Output
```bash
<img width="583" height="733" alt="Screenshot 2025-08-26 210311" src="https://github.com/user-attachments/assets/7a67a7b3-78e1-4a4a-a6b8-14ada5c8416b" />

```

## TEST CASE
### Input & Output
```bash
<img width="443" height="170" alt="Screenshot 2025-08-26 210713" src="https://github.com/user-attachments/assets/9c96c062-5f85-4875-af09-71a56387b63c" />

```

## TEST CASE
### Input & Output
```bash
<img width="559" height="831" alt="Screenshot 2025-08-26 211024" src="https://github.com/user-attachments/assets/47d0a5c9-319f-4b02-91df-1eda8b740922" />
<img width="470" height="274" alt="Screenshot 2025-08-26 211029" src="https://github.com/user-attachments/assets/dd1ceb83-70a4-4022-bf35-0f6f91c2503f" />

```
