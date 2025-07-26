## FIX CODE
```c++
#include <stdio.h>
#include <math.h>

int isPrime(int num) {
    if(num<2)return 0;
    for (int i = 2; i <= sqrt(num); i++) {
        if (num % i == 0)return 0;

    }
    return 1;
}

int main() {
    int n;
    printf("Enter N : ");scanf("%d",&n);
    int arr[n]; 
    for(int i=0;i<n;i++){
        printf("Enter value[%d] : ",i);
        scanf("%d",&arr[i]);

    }

    printf("Index:  ");
    for (int i = 0;i < n;i++){
        printf("%2d ", i);

    }
    printf("\n");

    printf("Array:  ");
    for(int i=0;i<n;i++){if (isPrime(arr[i]))
        printf("%2d ", arr[i]); 
    else
        printf("%2s ", "#"); 
    }
    printf("\n");
    
    return 0;
}
```

## TEST CASE
### Input
```bash
Enter N: 5
Enter value[0]: 1
Enter value[1]: 2
Enter value[2]: 3
Enter value[3]: 4
Enter value[3]: 5
```
### Output
```bash
Index:   0  1  2  3  4
Array:   #  2  3  #  5
```
<img width="1646" height="955" alt="image" src="https://github.com/user-attachments/assets/68f2f4b0-5260-4044-b137-f37ae43b893e" />


