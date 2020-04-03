# gittest
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int list[5];
    int *plist[5] = {NULL,};    //포인터 배열 선언 및 초기화

    plist[0] = (int *)malloc(sizeof(int)); //포인터에 동적할당으로 heap영역의 메모리 영역을 가리킴

    list[0] = 1;                   
    list[1] = 100;

    *plist[0] = 200;            //plist[0]이 가리키는 주소에 값을 대입

    printf("==========이름: 신윤성 학번: 2017038015==========\n");
    printf("value of list[0] = %d\n", list[0]);             
    printf("address of list[0]       = %p\n",&list[0]);  
    printf("value of list            = %p\n", list);   
    printf("address of list(&list)   = %p\n", &list);   //list배열의 주소. list[0]의 주소, 그리고 배열의 이름과 같은 값이 나옴.

    printf("-----------------------------------------\n");
    printf("value of list[1]    = %d\n", list[1]); 
    printf("address of list[1]  = %d\n", &list[1]);  
    printf("value of *(list+1)  = %d\n", *(list +1));  //list[1]이 가리키는 실제값 출력.
    printf("address of list+1   = %d\n", list+1);  //list[1]의 주소와 같음. list[0]에서 4바이트 더한 값.

    
    printf("-----------------------------------------\n");

    printf("value of *plist[0]  = %d\n", *plist[0]);   //plist[0]안에 들어있는 주소가 가리키는 값.
    printf("&plist[0]           = %p\n", &plist[0]);   
    printf("&plist              = %p\n", &plist);      
    printf("plist               = %p\n", plist);       //&plist[0],&plist,plist모두 같은 값 출력.
    printf("plist[0]            = %p\n", plist[0]);
    printf("plist[1]            = %p\n", plist[1]);
    printf("plist[2]            = %p\n", plist[2]);
    printf("plist[3]            = %p\n", plist[3]);
    printf("plist[4]            = %p\n", plist[4]);    //나머진 모두 null로 되어있음.

    free(plist[0]);   //할당한 메모리를 해제 시킨다. 

}
