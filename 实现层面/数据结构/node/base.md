这里记载node的基础结构

头信息：

由于replace函数的存在，每个node的头信息都必须有一个node指针指向替换目标
当目标为自身时表示此node未被替换
当目标为其他时，ptr类在访问此node时将进行重定向

引用计数的gc策略要求node头信息包含引用计数与弱引用计数

成员函数：

arec函数返回对应的setter以达到成员访问的目的

arec_for_gc使gc可不触发访问器进行node的遍历

for_each作为内置函数以提供，接受mapper，并当mapper返回true时停止遍历

for_each_for_gc是for_each的不触发访问器版本

be_watch此值被观测，默认返回自身

be_eval此值被求值，默认返回自身的be_watch结果的be_eval

