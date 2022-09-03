# reverse-addition
# Let's write 3 characters in 2 lines as much as the number entered in n and add the characters in the opposite direction! n에 입력된 개수 만큼 2줄에 3개의 문자들을 써서 서로 역방향에 해당되는 문자끼리 더해보자!
# c program
#include <stdio.h>
int add(int *i,int *j,int *r,int n);
int main(void){
	int n;
	int num[3];
	int num2[3];
	int sum_n[3]={0};
	int *i,*j,*r,*p1;
    scanf("%d",&n);
    for(i=num;i<n+num;i++){
    	scanf("%d",i); //&를 처음에 사용했는데 주소값이 필요한게 X  그냥값  
	}
	for(j=num2;j<n+num2;j++){
		scanf("%d",j);}
	r=sum_n;
	add(num,num2,sum_n,n);
	for(p1=r;p1<r+n;p1++){
		printf("%d",*p1);
	}
    return 0;
}
int add(int *i,int *j,int *r,int n){
	int *p;
	for(p=r;p<r+n;p++){
		*p=*i+*(j+n-1);
		i++;
		j--;
	}
}
#input--> 1 2 3   5 10 15
#result-->16 12 8(1+15,2+10,3+5)
