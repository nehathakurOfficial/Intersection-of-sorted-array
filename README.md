# Intersection-of-sorted-array
      //intersection of array  
      #include<bits/stdc++.h>
      using namespace std;

     vector<int> ArrayIntersection(vector<int>& nums1 ,vector<int>& nums2){
     vector<int>ans;
     vector<int>visited(nums2.size(),0);
     for(int i = 0; i<nums1.size(); i++){
        for(int j = 0; j<nums2.size();j++){
            if(nums1[i] == nums2[j]  && visited[j] == 0){
                ans.push_back(nums1[i]);
                visited[j] = 1;
                break;
            }
        
        if(nums2[j] >nums1[i]) break;

     }

     }
     return ans;
     }

     int main(){

     vector<int> nums1 = {1, 2, 2, 3};
     vector<int> nums2 = {2, 2, 3, 4};


     vector<int> result  =  ArrayIntersection(nums1,nums2);
     
     cout<<" intersection";
     for(int  x : result){
     cout<<x<< " ";
     }
     cout<<endl;
     return 0;

     
     }
     
