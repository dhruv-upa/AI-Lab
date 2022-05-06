#BFS
#include<iostream>
#include<bits/stdc++.h>
using namespace std;
int main()
{
    int V,e;
    cout<<"Enter no of vertices: "<<endl;
    cin>>V;
    cout<<"Enter no of edges: "<<endl;
    cin>>e;
    vector<int>adj[V];
    cout<<"Create graph: "<<endl;
    for(int i=0;i<e;i++)
    {
        int start,end;
        cin>>start>>end;
        adj[start].push_back(end);
    }
    vector<int>ans;
    bool visited[V]={false};
    queue<int>q1;
    q1.push(0);
    while(!q1.empty())
    {
        int node=q1.front();
        q1.pop();
        visited[node]=true;
        ans.push_back(node);
        for(auto it:adj[node])
        {
            if(visited[it]==false)
            {
                q1.push(it);
                visited[it]=true;
                
            }
            
        }
        
    }
    cout<<"BFS: "<<endl;
    for(auto it:ans)
    cout<<it<<" ";
}

#DFS
#include<iostream> 
#include<bits/stdc++.h> 
using namespace std;
void dfs(int node,vector<bool>&visited,vector<int>adj[],vector<int>&ans)
{
    if(visited[node]==true)
    return;
    ans.push_back(node);
    visited[node]=true;
    for(int i=0;i<adj[node].size();i++)
    {
        if(visited[adj[node][i]]==false)
        dfs(adj[node][i],visited,adj,ans);
    }
}

int main()
{
    int V,e;
    cout<<"Enter no of vertices: "<<endl;
    cin>>V;
    cout<<"Enter no of edges: "<<endl;
    cin>>e;
    vector<int>adj[V]; 
    cout<<"Create graph: "<<endl; 
    for(int i=0;i<e;i++)
    {
        int start,end;
        cin>>start>>end;
        adj[start].push_back(end);
    } 
    vector<bool>visited(V,false);
    vector<int>ans;
    dfs(0,visited,adj,ans);
    cout<<"DFS: "<<endl;
    for(auto it:ans)
    cout<<it<<" "; 
}
