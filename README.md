#include<pthread.h>
#include<stdio.h>
#include<unistd.h>
#include<sys/wait.h>
#include<stdlib.h>
void *fun();
void *fun1();
void *fun2();
int c=1;
int fib[100];
void main()
{
pthread_t th1;
pthread_create(&th1,NULL,fun,NULL);
pthread_join(th1,NULL);
}
void *fun()
{
printf("enter a no. you wish to get a fibonacci series");
scanf("%d",&c);
pthread_t th3;
pthread_create(&th3,NULL,fun2,NULL);
pthread_join(th3,NULL);
int f=c;
printf("size of array %d \n",f);
int i;
fib[0]=0;
fib[1]=1;
for(i=2;i<f;i++)
fib[i]=fib[i-1]+fib[i-2];
wait(NULL);
pthread_t th2;
