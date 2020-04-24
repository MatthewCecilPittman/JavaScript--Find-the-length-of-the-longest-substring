# JavaScript--Find-the-length-of-the-longest-substring
Daily coding problem #13

```
var lengthOfLongestSubstring = function(s, k){
var n=s.length, i=0, j=0, res=0;
var numOfChars=0;
var counts ={};
for(;j<n;j++) {
var c = s.charAt(j);
if(!counts[c]) {
count[c] = 1;
numOfChars++;
}
else{
counts[c]++;
}
while(numOfChars>k) {
var cI = s.charAt(i);
counts[cI]--;
if(counts[cI]==0) {
numOfChars--;
}
i++;
}
res = Math.max(res, j-i+1);
}return res;
};
```
