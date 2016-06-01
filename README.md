##### 斯坦福iOS7开发公开课笔记
###### 第二课、Xcode5
1. 初始化指针的最好方式是在getter()中判断，并分配空间：  
```Object-c
- (NSMutableArray *)cards
{
	//这样，只有在要用到该数组时，才创建数组，避免占用太多内存。
	if(!_cards)
	{
		_cards = [[NSMutableArray alloc] init];
	}

	return _cards;
}
```