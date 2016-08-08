# FE-Tips

每天一个前端Tips 包括但不限于JavaScript、Android、IOS

###基本格式

\#语言分类\# 日期：Tip的标题

这里是内容。。。

这是必要的注释

###基本格式举例

#### #JavaScript# 2016-08-11：对象数组根据某个属性排序

	function compare(prop){
		return function(obj1,obj2){
			var prop1 = obj[prop];
			var prop2 = obj[prop];
			if(prop1<prop2){
				return -1;
			} else if(prop1>prop2){
				return 1;
			} else {
				return 0;
			}
		}
	}
	var arr = [
		{"name":"bsunhui","age":"23"},
		{"name":"csunhui","age":"22"}
	];
	arr.sort(compare("age"));
	console.log(arr);					//[{"name":"csunhui","age":"22"},{"name":"bsunhui","age":"23"}]
	arr.sort(compare("name"));
	console.log(arr); 					//[{"name":"bsunhui","age":"23"},{"name":"csunhui","age":"22"}]

`compare`函数返回了一个**闭包**，这样就可以根据传入的属性进行排序。
