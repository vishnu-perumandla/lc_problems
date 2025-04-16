# maximum 69 number
```c++
class Solution {
public:
    int maximum69Number (int num) {
        int max;
        int n=num;
        int k=10;
        vector<int>v;
        int c=0;
       while(n>0){
            max=n%10;
            v.push_back(max);
            n=n/10;
        }
        for(int i=v.size()-1;i>=0;i--){
            if(v[i]!=9){
                v[i]=9;
                break;
            }
        }
        int q=0;
        int m=1;
        for(int i=0;i<v.size();i++){
            q+=v[i]*m;
            m=m*10;
        }
        return q;
    }
};
```