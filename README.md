# ReadMe.md File

updated ReadMe.file



## ReadMe SubSection

Readme subsection 1

- item1
- item2



## ReadMe Subsection2

Readme subsection 2(Add codeblock)

> BOJ 10942

```c++
#include<bits/stdc++.h>
#define fastio ios_base::sync_with_stdio(0); cin.tie(0); cout.tie(0);
using namespace std;

int n,m,s,e,p[2001];
bool pal[2001][2001]={0};

void isPal(int n){
	for(int i=1;i<=n;i++)pal[i][i]=1;
	for(int i=2;i<=n;i++)if(p[i]==p[i-1])pal[i-1][i]=1;
	for(int j=3;j<=n;j++){
		for(int i=1;i<=j;i++){
			if(!pal[i][j]&&p[i]==p[j]){
				pal[i][j]=pal[i+1][j-1];
			}
		}
	}
}

int main() {fastio	
	cin >> n;
	for(int i=1;i<=n;i++)cin>>p[i];
	cin >> m;
	isPal(n);
	while(m--){
		cin >> s >> e;
		cout << pal[s][e]<<"\n";
	}

	return 0;
}
```

