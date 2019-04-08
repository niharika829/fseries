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
