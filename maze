#include<iostream>
#include<cstdio>
#include<cstring>
#include<queue>
using namespace std;
 
 
int n;
int tu[10][10];
int vist[10][10];
 
 struct Point{
    int x,y;
    int len;
} p;
 
queue<Point> Q;
 
 int flag=0;
 
void bfs(){
	Point a=Q.front();Q.pop();
	int dx=a.x;int dy=a.y;
		if(dx==n-2&&dy==n-2){
			flag=a.len;
			return;
}

	if(!tu[dx][dy-1]&&!vist[dx][dy-1]){
		Point b;b.x=dx;b.y=dy-1;b.len=a.len+1;
		vist[dx][dy-1]=1;Q.push(b);
}
	if(!tu[dx][dy+1]&&!vist[dx][dy+1]){
		Point b;b.x=dx;b.y=dy+1;b.len=a.len+1;
		Q.push(b);vist[dx][dy+1]=1;
}
	if(!tu[dx+1][dy]&&!vist[dx+1][dy]){
		Point b;b.x=dx+1;b.y=dy;b.len=a.len+1;
		Q.push(b);vist[dx+1][dy]=1;
}
	if(!tu[dx-1][dy]&&!vist[dx-1][dy]){
		Point b;b.x=dx-1;b.y=dy;b.len=a.len+1;
		Q.push(b);vist[dx-1][dy]=1;
}
	if(Q.empty()) return;
	else bfs();
}
 int main(){
 cin>>n;
 for(int i=0;i<n;i++){
     for(int j=0;j<n;j++)
         scanf("%d",&tu[i][j]);
}
		p.x=1;p.y=1;p.len=0;
		Q.push(p);vist[1][1]=1;
		bfs();
	if(flag) printf("%d",flag);
	else printf("No solution");
}
