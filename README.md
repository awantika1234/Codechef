# Codechef
#include<iostream>
#include<cstdlib>
#include<algorithm>
#include<list>
using namespace std;
int main()
{
    int t;
    cin>>t;
    while(t!=0)
    {
        int n;
        list <int> arrr;
        cin>>n;
        int v[n];
        for(int i=0;i<n;i++)
            cin>>v[i];
        int sml=0,p=0,temp,diff;
        for(int j=0;j<n;j++)
        {
            for(int k=j+1;k<n;k++)
            {
                diff=abs(v[j]-v[k]);
                arrr.push_back(diff);
            }
        }
        arrr.sort();
        list<int>::iterator it = arrr.begin();
        advance(it, 0);
        cout<<*it<<endl;
        t--;
    }
    return 0;
}
