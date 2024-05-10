# LeetCode-Master
Noob Camp mix Crack the Code Interview(CCI) && Acwing 算法基础班(ACW) && 代码随想录(YYY)  

## Apr 3, 2024
My 4080 Super has finally arrived !!!   

The most tricky part is to login the leetcode extension on VSCode.   
Remember to use cookie of ur leetcode account since the orther ways are all dead ends!!!    
![image](https://github.com/Justinquant/LeetCode-Master/assets/147337004/be3a455b-3135-4c9d-a95b-2fee2128787d)

CCI book:    
the sytle of every company

YYY camp:         
[707]binary search (704) - nothing fancy. 
[707]square root (69) - use newton method.      
[707]two pointer (27) - can goes both directions.  

## Apr 4, 2024
Watch the Rockets VS Warriors game tonight.
My old man isn't that old hhh~          
![image](https://github.com/Justinquant/LeetCode-Master/assets/147337004/432aee56-099e-4552-8ea9-bb7ff247f447)

CCI book:    
what kind of code style you should write

YYY camp:         
[977] Squares of a Sorted Array - easy.  
[209] Minimum Size Subarray Sum - sliding window, set the target threshold.  
[59]Spiral Matrix II - four pointers end when they overlapped horizontally or vertically.  

# Summary of Array
![Array](https://github.com/Justinquant/LeetCode-Master/assets/147337004/600d5385-7dc6-43ec-91c5-7500bc517eab)

## Apr 5, 2024
CCI book:    
No time for it

YYY camp:         
LinkedList chapter started
[203] Remove Linked List Elements - easy.   
[707] Design Linked List - easy.   
[206] Reverse Linked List - set up the return condition / exit situation for recusion !!!   

## Apr 6, 2024
CCI book:    
coding style.Make certain struct instead of long enumeration

YYY camp:         
[24] Swap Nodes in Pairs - use **pp = &head can replace dummyHead, bullseye bullseye bullseye!!!                   
[19] Remove Nth Node From End of List - easy, make the fast pointer go nth step in advance.<br>
[160] Intersection of Two Linked Lists - make the starts point same.     
[142] Linked List Cycle II - mainly about math prove.    
https://en.wikipedia.org/wiki/Cycle_detection##Floyd's_Tortoise_and_Hare

# Summary of LinkedList
![LinkedList](https://github.com/Justinquant/LeetCode-Master/assets/147337004/c857c573-1e57-4018-9167-d2e98e2f8306)

## Apr 8, 2024
CCI book:    
The operation of string and char array            

YYY camp:            
[242] Valid Anagram - easy           
[349] Intersection of Two Arrays - notice the constraints, use array when u can. set use insert method.               
[202] Happy Number - can use __Floyd Cycle detection Algo__ instead of set.     
[1] Two Sum - finally the very first question two sum ！！！    

## Apr 9, 2024
CCI book:    
The operation of string and char array     

YYY camp:    
[454] 4Sum II - no index request then can apply unordered_map             
[383] Ransom Note - easy     
[15] 3Sum - notice the weird behaviour of emplace_back when use uncertain type variable           
[18] 4Sum -  prune           
if the constraints set to be lowercase English letters __use array instead of unordered_map__                  

## Apr 10, 2024
Acwing:               
find the the kth in n: n >> k & 1               
return the last 1 of n：lowbit(n) = n & -n, -n = ~n + 1 // Two's Complement

YYY camp:  
[344] Reverse String - easy s[i] ^= s[j]; s[j] ^= s[i]; s[i] ^= s[j]; 
[541] Reverse String II - easy    
[151] Reverse Words in a String - can use stack as well,erase is On time complexity   

## Apr 11, 2024
Acwing:                
use array to implentment linkedlist/stack/queue/monotonic stack & recurring queue               

YYY camp:            
[28] Find the Index of the First Occurrence in a String - KMP                
[459] Repeated Substring Pattern - Round cycle & KMP!!! 
```
int n = needle.size();
int next[n];
ne[0] = 0;
for (int i = 1, j = 0; i < n; i++) {
  while (j && needle[i] != needle[j])
      j = ne[j - 1];
  if (needle[i] == needle[j])
      j++;
  ne[i] = j;
}
```

## Apr 12, 2024
Acwing:   
Practice yesterday data structure              

YYY camp:     
[225] Implement Stack using Queues  - use one queue                       
[232] Implement Queue using Stacks - use two stacks      
[20] Valid Parentheses - edge case and special verdict for beating 100%!!!                      
[1047] Remove All Adjacent Duplicates In String - space O1 we use origin string as stack + two pointer     
[150] Evaluate Reverse Polish Notation - Reverse Polish Notation used for computer without reverse                 
```
// lambda expression  bullseye again ！！！
unordered_map<string, function<int(int, int)>> map = {{"+", [](int a, int b) { return a + b; }},
                                                              {"-", [](int a, int b) { return a - b; }},
                                                              {"*", [](int a, int b) { return a * b; }},
                                                              {"/", [](int a, int b) { return a / b; }}};
```
 
## Apr 13, 2024
Acwing:  
implementation of min/max heap is tricky  - use up / down function

YYY camp:     
[239] Sliding Window Maximum - use monotonic queue        
[347] Top K Frequent Elements - priority_queue          
```
priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq; // less heap
for (auto &[num, freq] : count) {   // Structured Binding
    pq.push({freq, num});
    if (pq.size() > k) {
        pq.pop();
    }
}
```
[71] Simplify Path - vector can do everything even pop_back()！     

## Apr 15, 2024
Acwing:    
Searching and Graph Theory          

YYY camp:           
DFS algo                   
[129] Sum Root to Leaf Numbers | [144] Binary Tree Preorder Traversal |  [145] Binary Tree Postorder Traversal | [94] Binary Tree Inorder Traversal
When non recursion use stack with null point tail              
[199] Binary Tree Right Side View - can use both BFS || DFS         
   


## Apr 16, 2024
Acwing:    
revision and exercise

YYY camp:             
BFS algo       
[102] Binary Tree Level Order Traversal |  [107] Binary Tree Level Order Traversal II |  [637] Average of Levels in Binary Tree | [429] N-ary Tree Level Order Traversal | [515] Find Largest Value in Each Tree Row | [117] Populating Next Right Pointers in Each Node II | [111] Minimum Depth of Binary Tree | [226] Invert Binary Tree | 104] Maximum Depth of Binary Tree | [572] Subtree of Another Tree | [100] Same Tree | [101] Symmetric Tree | [116] Populating Next Right Pointers in Each Node           

## Apr 17, 2024
Acwing:    
Searching and Graph Theory II

YYY camp:             
BFS & DFS algo         
[559] Maximum Depth of N-ary Tree | [404] Sum of Left Leaves |  [257] Binary Tree Paths | [513] Find Bottom Left Tree Value        
[222] Count Complete Tree Nodes - the characteristic of complete tree                  
[110] Balanced Binary Tree - use recusive DFS               
[112] Path Sum | [113] Path Sum II - use backttrack algo                   

## Apr 18, 2024
 YYY camp:  
[106] Construct Binary Tree from Inorder and Postorder Traversal - use index
[105] Construct Binary Tree from Preorder and Inorder Traversal | [654] Maximum Binary Tree | [617] Merge Two Binary Trees - recursion method is better           
[700] Search in a Binary Search Tree - BST  | [98] Validate Binary Search Tree - verify BST must use inorder search & stack      

## Apr 19, 2024
Acwing:    
Dijkstra algo      

YYY camp:  
[501] Find Mode in Binary Search Tree - operate in the inorder traverse                   
[236] Lowest Common Ancestor of a Binary Tree - recursion better  | [235] Lowest Common Ancestor of a Binary Search Tree - iteration better      
[701] Insert into a Binary Search Tree | [450] Delete Node in a BST | [669] Trim a Binary Search Tree | [108] Convert Sorted Array to Binary Search Tree | [538] Convert BST to Greater Tree     

# Backtracking
## Apr 25, 2024
YYY camp:                     
[77] Combination | [216] Combination Sum III - can use fixed sub array which is fast               

## Apr 26, 2024
YYY camp:     
[17] Letter Combinations of a Phone Number | [39] Combination Sum     

## Apr 27, 2024
YYY camp:     
[40] Combination Sum II  | [131] Palindrome-partitioning | [93] Restore IP Adress              

## Apr 28, 2024
YYY camp:  
[78] Subsets | [90] Subsets II | [491] Non-decreasing-subsequences | [46] Permutations   

## Apr 29, 2024
YYY camp:  
[332] Reconstruct Itinerary - ```unordered_map<string, priority_queue<string, vector<string>, greater<string>>> targets;```  
[51] N-Queens - ``` vector<int> cols(n, 0), diag1(2 * n - 1, 0), diag2(2 * n - 1, 0); if (cols[col] || diag1[row + col] || diag2[row - col + n - 1]) continue; ```
[37] Sudoku Solver - ``` boxes[i / 3 * 3 + j / 3] |= 1 << num; boxes[box] & (1 << num); boxes[box] &= ~(1 << num);```             

# Summary of Backtracking
![e73a6529ff1cdd82fadd07281ea81dc](https://github.com/Justinquant/LeetCode-Master/assets/147337004/87aa6a88-a993-4018-bb7c-f188898761fc)

# Greedy Algo
## Apr 30, 2024
YYY camp:  
[455] assign-cookies | [376] Wiggle Subsequence | [53] Maximum Subarray | [122] Best Time to Buy and Sell Stock II | [714] Best Time to Buy and Sell Stock | [55] Jump Game |         
[1005] Maximize Sum Of Array After K Negations - 
```
priority_queue<int, vector<int>, greater<int>> pq(nums.begin(), nums.end()); pq.push(sth);
sort(nums.begin(), nums.end(), [](int a, int b) { return abs(a) > abs(b); });              
return accumulate(nums.begin(), nums.end(), 0);
```

## May 1, 2024
YYY camp:  
[134] Gas Station | [135] candy | [860] Lemonade-change | [452] Minimum Number of Arrows to Burst Balloons | [435] Non-overlapping Intervals | [763] Partition Labels |            
[56] Merge-intervals | [738] monotone-increasing-digits | [968] binary-tree-cameras
[406] Queue-Reconstruction-by-height -   
```
static bool cmp(const vector<int>& a, const vector<int>& b) // inside the class need to add static since this is a invisible this* pointer
list<vector<int>> que; std::list<vector<int>>::iterator it = que.begin(); pos--; it++; que.insert(it, people[i]);
```

# Dynamic Programming
## May 2, 2024
YYY camp:  
[509] Fibonacci Number | [70] Climbing-stairs | [746] Min-cost-climbing-stairs | [62] Unique-path | [63] Unique-path II | [343] Integer Break | [96] Unique Binary Search Trees

## May 4, 2024
YYY camp:  
[416] Partition Equal Subset Sum | [1049] Last Stone Weight II | [698] Partition to K Equal Sum Subsets | [473] Matchsticks to Square | [494] Target-sum | [474] Ones and Zeroes

## May 5, 2024
[518] Coin Change II - include every step start from 2D vector
[377] Combination-sum-iv | [322] Coin Change | [279] Perfect Squares | [139] Word-break
```
unordered_set<string> dict(wordDict.begin(), wordDict.end());
int n = s.size();
vector<bool> dp(n + 1, false);
dp[0] = true;
for (int i = 1; i <= n; i++) {
  for (int j = 0; j < i; j++) {
    if (dp[j] && dict.count(s.substr(j, i - j))) {
      dp[i] = true;
      break;
    }
  }
}
return dp[n];
```
[198] House Robber | [213] House Robber II | [337] House Robber III 
```
function<pair<int, int>(TreeNode*)> dfs = [&](TreeNode* node) -> pair<int, int> {
  if (!node) return {0, 0};
  auto [left_rob, left_not_rob] = dfs(node->left);
  auto [right_rob, right_not_rob] = dfs(node->right);
  int rob = node->val + left_not_rob + right_not_rob;
  int not_rob = max(left_rob, left_not_rob) + max(right_rob, right_not_rob);
  return {rob, not_rob};
};
auto [rob, not_rob] = dfs(root);
return max(rob, not_rob);
```

## May 6, 2024
[121] [122] [123] [188] [309] Best-time-to-buy-and-sell-stock I | II | III | IV | with cooldown | 
[392] Is-subsequence | [53] Maximum-subarray | [1035] uncrossed-lines | [1143] Longest-Common-Subsequence
[300] Longest-increasing-subsequence
```
vector<int> dp;
    for (int i = 0; i < nums.size(); i++) {
      auto it = lower_bound(dp.begin(), dp.end(), nums[i]);
      if (it == dp.end()) dp.push_back(nums[i]);
      else *it = nums[i];
    }
    return dp.size();
```

## May 7, 2024
[115] Distinct-subsequence | [583] Delete-operation-for-two-strings | [72] Edit-distance            
[647] Palindromic-substrings | [516] Longest-Palindromic-subsequence 

# Monotonic Stack
## May 8, 2024
[739] Daily-temperature | [496] Next-greater-element I | II | [42] Trapping-rain-water | [84] Largest-rectangle-in-histogram    

# Graph Theory
## May 9, 2024
[797] All-path-from-source-to-target | [200] Number-of-islands | [695] Max-area-of-island | [130] Surrounded-regions | [1020] Number-of-enclaves     
[417] Pacific-atlantic-water-flow  | [827] Making-a-large-island | [127] Word-ladder
```
auto dfs = [&](int x, int y, int(&visited)[N][N], auto &&dfs) -> void {};
void dfs(int x, int y, vector<vector<int>> &heights, int (&visited)[N][N])
```





















