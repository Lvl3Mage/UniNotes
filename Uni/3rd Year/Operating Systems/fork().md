A `fork()` command in C creates a child process with all the context of a parent process and returns the ID of this child process. Both processes (new child and old parent) continue from the return of the `fork` call. 

>[!info] 
>The fork returns 
>- The child ID if the process is a parent
>- 0 when the process is a child
>- -1 when there is an error

```c
void main(){
	if(fork() 
	// both processes will continue from here 
	//fork() will return 0 for child and 1 for parent
	!= 0){ 
		printf("Am Parent\n");
	}
	else{
		printf("Am Child);
	}
}
```