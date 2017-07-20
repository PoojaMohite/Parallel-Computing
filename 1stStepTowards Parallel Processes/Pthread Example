/*
Program to create 1 to 10n threads on user demand
Created by : Pooja Mohite
MTSU ID : M01348984
*/

#include <pthread.h>
#include <stdio.h>


void * thread_fun(void *x_void_ptr)
{

int *x=(int *)x_void_ptr;
printf("Hello World From Child Thread %d \n ",(*x));
}

int main()
{

	pthread_t threads_count[10];
	int req_threads=0,arr[10];
	int loopcount,joincount;
	printf("Input number of threads");
	scanf("%d",&req_threads);
	if(req_threads<=10 && req_threads>=1 )
	{
		for(loopcount=0;loopcount<req_threads;loopcount++)
		{
			arr[loopcount]=loopcount;
			pthread_create(&threads_count[loopcount],NULL,thread_fun,(void *) & arr[loopcount] );
	
	
		}

		for(joincount=0;joincount<req_threads;joincount++)
		{	

			pthread_join(threads_count[joincount],NULL);

		}
		printf("That's all from parent");
	}
	else
	{
		printf("Please enter the required threads between 1 to 10 only ");
	}
	
	return 0;

}
