# Python
## Syntax
```
def intersect(self, nums1, nums2):
    a, b = map(collections.Counter, (nums1, nums2))   # counter是 clt库中的特殊字典子类，用于元素计数
    return list((a & b).elements()) # counter 交集操作，取最小数，.elements()方法返回包含所有重复元素的迭代器
```
## Cache decorator
```
from functools import cache
# @cache 是一个装饰器（decorator），用于自动缓存函数的返回结果。这个装饰器属于 Python 3.9 和更高版本中的 functools 模块。使用 @cache 装饰器可以帮助你保存函数对于特定输入参数的计算结果，如果同样的参数再次传
# 入时，它将直接返回之前缓存的结果而不是重新计算 @cache 装饰器的主要目的是提高程序性能，特别是在涉及到重复调用计算成本高的函数时。在递归函数中使用缓存尤为有效，因为递归函数经常会多次调用相同参数的函数。
@cache
def fibonacci(n):
    if n < 2:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))  # 输出斐波那契数列的第10项
```

# C++   
## vector       
set_intersection，传入两个vector的四个迭代器，第五个参数是要返回的迭代器，位置是交集末尾 + 1；        
emplace_back 无法推断隐式类型，try push_back或显示指定数据类型

## Syntax
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
## Syntax
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
