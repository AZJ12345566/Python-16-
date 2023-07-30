# Python-16-
Python学习笔记(16)
# p53 列表元素的添加操作
#向列表的末尾添加一个元素 append()
lst=[10,20,30]
print('添加元素之前',lst)
lst.append(100)
print('添加元素之后‘,lst,id(lst)) #这里标识是一样的，所以是同一个数组

#在列表的末尾至少添加一个元素 extend()
lst2=['hello','world']
lst.append(lst2)  #将lst2作为1个元素添加到列表的末尾
print(lst)  #输出为[10,20,30,100,['hello','world']]
#向列表的末尾一次性添加多个元素
lst.extend(lst2)
print(lst)  #输出为[10,20,30,100,'hello','world']

#在列表的任意位置去添加一个元素 insert()
lst.insert(1,90)  #这里的1是指一个列表的下标
print(lst)

#在列表的任意位置添加至少一个元素 切片
lst3=[True,False,'hello']
lst[1:]=lst3 #从下标为1的地方开始切，dest默认为列表最后一个元素，step默认为1
print(lst)



# p54 列表元素的删除操作
lst=[10,20,30,40,50,60,30]
lst.remove(30)  #从列表中移除一个元素，如果有重复元素只移第一个元素
print(lst)
lst.remove(100)  #会输出在列表当中不存在

#pop()根据索引去移除元素
lst.pop(1)
print(lst) #将索引为1的位置就移除了
lst.pop(5) #输出：未有索引
lst.pop()
print(lst) #如果不指定参数，会自动清除列表当中的最后一个元素

#切片：一次删除至少一个元素，值得注意的是切片会产生一个新的列表对象
new_list=lst[1:3]
print('原列表',lst)
print('切片后的列表',new_list)  #输出为[40,50]

#不产生新的列表对象，而是删除原列表中的新的内容
lst[1:3]=[]
print(lst)  #输出为[10,60]

#clear:清除列表中的所有元素
lst.clear()
print(lst)

#del:将列表对象删除
del lst
print(lst)  #输出为：未定义



# p55 列表元素的修改操作
lst=[10,20,30,40]
#一次修改一个值
lst[2]=100
print(lst)

#修改列表当中的多个元素
lst[1:3]=[300,400,500,600]
print(lst)
