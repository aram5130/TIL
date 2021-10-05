2021.10.05

------

## 4장

#### Algorithms 알고리즘

**배열**은 한 자료형의 여러 값들이 메모리상에 모여 있는 구조이다.

컴퓨터는 이 값들에 접근할 때 배열의 인덱스 하나하나를 접근한다. 만약 어떤 값이 배열 안에 속해 있는지를 찾아 보기 위해서는 배열이 정렬되어 있는지 여부에 따라 아래와 같은 방법을 사용할 수 있다.



###### 선행 검색

배열의 인덱스를 처음부터 끝까지 하나씩 증가시키면서 그 값이 속하는지를 검사하는 것으로 아래와 같은 의사 코드를 나타낼 수 있다.

```
for i from 0 to n-1
	if i'th element is 50
		Return true
		
Return false
```



###### 이진 검색

배열이 정렬되어 있다면, 배열 중간 인덱스부터 시작하여 찾고자 하는 값과 비교하여 그보다 작은인덱스(작은 값이 저장) 또는 큰 인덱스(큰 값이 저장)로 이동을 반복한다.

```
if no items
	Return false
if middle item is 50
	Return true
Else if 50 < middle item
	Search left half
Else if 50 > middle item
	Search right half
```



##### 알고리즘 표기법

![image-20211005155848976](C:\Users\A Ram\AppData\Roaming\Typora\typora-user-images\image-20211005155848976.png)

**Big O 표기법**

여기서 O는 **“on the order of”**의 약자로, 쉽게 생각하면 **“~만큼의 정도로 커지는”** 것이라고 볼 수 있다. O(n) 은 n만큼 커지는 것이므로 n이 늘어날수록 선형적으로 증가하게 된다. O(n/2)도 결국 n이 매우 커지면 1/2은 큰 의미가 없어지므로 O(n)이라고 볼 수 있다.

주로 아래 목록과 같은 Big O 표기가 실행 시간을 나타내기 위해 많이 사용

- O(n^2)
- O(n log n)
- O(n) - 선형 검색
- O(log n) - 이진 검색
- O(1)



**Big O**가 알고리즘 **실행 시간의 상한**을 나타낸 것이라면, 반대로 **Big** **Ω**는 알고리즘 **실행 시간의 하한**을 나타내는 것.

예를 들어 선형 검색에서는 n개의 항목이 있을때 최대 n번의 검색을 해야 하므로 상한이 O(n)이 되지만 운이 좋다면 한 번만에 검색을 끝낼수도 있으므로 하한은 Ω(1)이 된다.

역시 아래 목록과 같은 Big Ω 표기가 많이 사용.

- Ω(n^2)
- Ω(n log n)
- Ω(n) - 배열 안에 존재하는 값의 개수 세기
- Ω(log n)
- Ω(1) - 선형 검색, 이진 검색



##### 선형 검색

찾고자 하는 자료를 검색하는데 사용되는 알고리즘중의 하나.

선형 검색은 **원하는 원소가 발견될 때까지 처음부터 마지막 자료까지 차례대로 검색**한다. 선형 검색은 찾고자하는 자료를 찾을 때까지 모든 자료를 확인해야한다.



**선형 검색 알고리즘**은 **정확하지만 효율성은 떨어지는 방법**

리스트의 길이가 n이라고 가정한다면, 찾고자 하는 자료가 맨 마지막에 있거나 리스트 안에 없는 최악의 경우에는 모든 원소를 확인해야 하므로 n번만큼 실행된다. 따라서 효율성이 매우 떨어지는 것을 알 수 있다.

반대로 최선의 상황은 처음 시도했을 때 찾고자 하는 값이 있는 경우에는 효율적이라고 할 수 있다. 선형 검색은 **자료가 정렬되어 있지 않거나 그 어떤 정보 없이 하나씩 찾아야 하는 경우에 유용**하다. 이러한 경우 무작위로 탐색하는 것도바 순서대로 탐색하는 것이 더 효율적이다.

- 주어진 배열에서 특정 값을 찾기 위한 코드

  ```c
  #include <cs50.h>
  #include <stdio.h>
  
  int main(void)
  {
      //numbers 배열 정의 및 값 입력
      int numbers[] = {4, 8, 15, 16, 23, 43};
      
      //값 50 검색
      for (int i = 0; i < 6, i++)
      {
          if (numbers[i] == 50)
          {
              printf ("Found\n");
              return 0;
          }
      }
      printf ("Not found\n");
      return 1;    
  }
  ```

  배열의 크기만큼 for 루프를 돌면서 배열의 인덱스를 차례대로 방문하여 찾는 값이 있는지를 검사한다.

- 문자열로 이루어진 배열 (전화번호부에서 특정 이름을 찾아 해당하는 전화번호 출력하기)

  ```c
  #include <cs50.h>
  #include <stdio.h>
  #include <string.h>
  
  int main(void)
  {
      string names[] = {"EMMA", "RODRIGO", "BRIAN", "DAVID"}
      string numbers[] = {"617-555-0100", "617-555-0101", "617-555-0102", "617-555-0103"};
      
      for (int i = 0; i < 4; i++)
      {
          if (strcmp(names[i], "EMMA") == 0)
          {
              printf("Found %s\n", numbers[i]);
              return 0;
          }
      }
      printf("Not Found %s\n");
      return 1;
  }
  ```

  names 배열과 numbers 배열을 따로 정의하고 names 배열에서 검색해 해당하는 인덱스의 numbers 배열 값을 출력하는 것. 하지만 이 경우에는 names 배열과 numbers 배열이 서로 같은 인덱스를 가져야 한다는 한계가 있다. 

  

  더 좋은 방법은 아래의 코드와 갗이 새로운 자료형의 **구조체**를 정의하여 이름과 번호를 묶어주는 것이다.

  ```c
  #include <cs50.h>
  #include <stdio.h>
  #include <string.h>
  
  typedef struct
  {
      string name;
      string number;
  }
  person;
  
  int main(void)
  {
      person people[4];
  
      people[0].name = "EMMA";
      people[0].number = "617–555–0100";
      people[1].name = "RODRIGO";
      people[1].number = "617–555–0101";
      people[2].name = "BRIAN";
      people[2].number = "617–555–0102";
      people[3].name = "DAVID";
      people[3].number = "617–555–0103";
  
      // EMMA 검색
      for (int i = 0; i < 4; i++)
      {
          if (strcmp(people[i].name, "EMMA") == 0)
          {
              printf("Found %s\n", people[i].number);
              return 0;
          }
      }
      printf("Not found\n");
      return 1;
  }
  ```

  person 이라는 이름의 구조체를 자료형으로 정의하고 person 자료형의 배열을 선언하면 그 안에 포함된 속성값은 '.'으로 연결해서 접근할 수 있다.

  person a; 라는 변수가 있다면, a.name 또는 a.number 각각의 이름과 전화번호를 저장하는 변수가 된다. 이렇게 함으로써 확장성 있는 전화번호부 검색 프로그램을 만들 수 있다.

























