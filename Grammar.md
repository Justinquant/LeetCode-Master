## Python

def intersect(self, nums1, nums2):
    a, b = map(collections.Counter, (nums1, nums2))   # counter是 clt库中的特殊字典子类，用于元素计数
    return list((a & b).elements()) # counter 交集操作，取最小数，.elements()方法返回包含所有重复元素的迭代器


## C++   
# vector       
set_intersection，传入两个vector的四个迭代器，第五个参数是要返回的迭代器，位置是交集末尾 + 1；        
emplace_back 无法推断隐式类型，try push_back或显示指定数据类型        
