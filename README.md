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
