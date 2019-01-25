# 在render函数中怎么使用循环


jsx中只能写表达式，不能写多行语句
所以最佳循环写法是使用map函数

## 一层循环

``` javascript
<View>
{
    数组.map((单个元素, 索引) => <View key={单个元素.id || 索引} />);  // 单行箭头函数无需写return
}
</View>

// 或

<View>
{
    数组.map((单个元素, 索引) => {
        return (
            <View key={单个元素.id || 索引} >
            </View>
            );  // 多行箭头函数需要加括号和return
    })
}
</View>
```

## 二层循环

``` javascript
<View>
{
    数组.map((单个元素, 索引) => {
        return (
            <View key={单个元素.id || 索引} >
            {
                数组.map((单个元素, 索引) => {
                    return (
                        <View key={单个元素.id || 索引} >
                        
                        </View>
                        );  // 多行箭头函数需要加括号和return
                })
            }
            </View>
        );  // 多行箭头函数需要加括号和return
    })
}
</View>
```

[参考链接](http://bbs.reactnative.cn/topic/845/%E5%9C%A8render%E5%87%BD%E6%95%B0%E4%B8%AD%E6%80%8E%E4%B9%88%E4%BD%BF%E7%94%A8for%E5%BE%AA%E7%8E%AF)

## 技术 