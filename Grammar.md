# Python
## grammar
```
def intersect(self, nums1, nums2):
    a, b = map(collections.Counter, (nums1, nums2))   # counter是 clt库中的特殊字典子类，用于元素计数
    return list((a & b).elements()) # counter 交集操作，取最小数，.elements()方法返回包含所有重复元素的迭代器
```

# C++   
## vector       
set_intersection，传入两个vector的四个迭代器，第五个参数是要返回的迭代器，位置是交集末尾 + 1；        
emplace_back 无法推断隐式类型，try push_back或显示指定数据类型

## grammar
```
class Solution {
public:
    bool canPermutePalindrome(string s) {
        unordered_map<char, int> cnt;
        for (auto& c : s) {
            ++cnt[c];
        }
        int sum = 0;
        for (auto& [_, v] : cnt) {   //结构化绑定 c++17 auto [a, b, c] = tup;
            sum += v & 1;   //判断奇偶性
        }
        return sum < 2;
    }
};
```

# Java
## grammar
```
class Solution {
    public boolean canPermutePalindrome(String s) {
        Map<Character, Integer> cnt = new HashMap<>();
        for (int i = 0; i < s.length(); ++i) {
            cnt.merge(s.charAt(i), 1, Integer::sum);  // merge方法用于更新key中value的计数，为map接口的通用方法
        }
        int sum = 0;
        for (int v : cnt.values()) {
            sum += v & 1;
        }
        return sum < 2;
    }
}
```
