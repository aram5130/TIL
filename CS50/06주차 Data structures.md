2021.10.14

------

## 6장

#### Data Structures 자료구조

##### malloc, 포인터 학습

```c
int main(void)
{
    int *x;
    int *y;

    x = malloc(sizeof(int));

    *x = 42;
    *y = 13;
}
```

main 함수 안의 첫 두줄에서는 **포인터 x와 y**를 선언한다. 그리고 x에는 **malloc**함수를 이용해서 int 자료형 크기에 해당하는 메모리를 할당한다.

그 다음에 x와 y포인터가 가르티는 지점에 각 42, 13을 저장한다. 여기서 문제가 될 수 있는 부분은 *y = 13인데, y는 포인터로만 선언되었을 뿐, 어디를 가르킬지에 대해서는 아직 정의되어 있지 않다. 따라서 **초기화 되지 않은 *y** 는 프로그램 어딘가를 임의로 가르키고 있을 수도 있다.

따라서 그곳에 13이라는 값을 저장하는 것이 오류를 발생시킬 수도 있다. 아래 코드와 같이 **y = x;**라는 코드를 더해주면, y는 x가 가르키는 곳과 동일한 곳을 가르키게 된다. 따라서 *y = 13;으로 저장하면 x가 가르키는 곳도 동일하게 13으로 저장될 것이다.

```c
y = x;

*y = 13;
```



##### 배열의 크기 조정하기

컴퓨터 안의 메모리는 마치 **사물함**과 같은 구조로, 우리가 사용하고자 하는 사물함의 개수를 한 번 정한 이후에는, 공간이 모자란다고 해서 주변의 사물함을 마음대로 더 사용할 수는 없다. 이미 다른 목적으로 사용되고 있을 수도 있기 때문에, 이와 같이 이미 일정한 크기의 메모리가 할당되어 있는 상황에서, 그 크기를 늘리는 일은 생각만큼 단순하지는 않다.

일정한 크기의 배열이 주어졌을 때, 그 크기를 키우려면 **새로운 공간에 큰 크기의 메모리를 다시 할당**하고 기존 배열의 값들을 하나씩 옮겨주어햐 한다.

이러한 작업은 O(n), 즉 배열의 크기 n만큼 실행 시간이 소요된다.

```c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    //int 자료형 3개로 이루어진 list 라는 포인터를 선언하고 메모리 할당하고
    int *list = malloc(3 * sizeof(int));

    // 포인터가 잘 선언되었는지 확인한다
    if (list == NULL)
    {
        return 1;
    }

    // list 배열의 각 인덱스에 값 저장
    list[0] = 1;
    list[1] = 2;
    list[2] = 3;

    //int 자료형 4개 크기의 tmp 라는 포인터를 선언하고 메모리 할당
    int *tmp = malloc(4 * sizeof(int));

    if (tmp == NULL)
    {
        return 1;
    }

    // list의 값을 tmp로 복사
    for (int i = 0; i < 3; i++)
    {
        tmp[i] = list[i];
    }

    // tmp배열의 네 번째 값도 저장
    tmp[3] = 4;

    // list의 메모리를 초기화
    free(list);

    // list가 tmp와 같은 곳을 가리키도록 지정
    list = tmp;

    // 새로운 배열 list의 값 확인
    for (int i = 0; i < 4; i++)
    {
        printf("%i\n", list[i]);
    }

    // list의 메모리 초기화
    free(list);
}
```



위와 동일한 작업을 **realloc** 이라는 함수를 이용해서 수행할 수 있다.

```c
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    int *list = malloc(3 * sizeof(int));
    if (list == NULL)
    {
        return 1;
    }

    list[0] = 1;
    list[1] = 2;
    list[2] = 3;

    // tmp 포인터에 메모리를 할당하고 list의 값 복사
    int *tmp = realloc(list, 4 * sizeof(int));
    if (tmp == NULL)
    {
        return 1;
    }

    // list가 tmp와 같은 곳을 가리키도록 지정
    list = tmp;

    // 새로운 list의 네 번째 값 저장
    list[3] = 4;

    // list의 값 확인
    for (int i = 0; i < 4; i++)
    {
        printf("%i\n", list[i]);
    }

    //list 의 메모리 초기화
    free(list);
}
```



















