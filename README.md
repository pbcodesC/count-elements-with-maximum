# count-elements-with-maximum
3005 leetcode daily challange
class Solution {
public:
    int maxFrequencyElements(vector<int>& nums) {
        unordered_map<int , int> freqMap;
        int maxFreq = 0;

        for(int num : nums){
         freqMap[num]++;
         maxFreq = max(maxFreq , freqMap[num]);
        }
      int result = 0;
      for ( const auto& entry : freqMap){
        if( entry.second == maxFreq){
            result += entry.second;
        }
      }
      return result;  
    }
};
