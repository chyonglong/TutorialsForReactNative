# ScrollView 中按钮按第二次才有效果

在ScrollView加属性
keyboardShouldPersistTaps="handled"

!注意：所有由ScrollView派生出来的都需要加改属性

``` javascript
<ScrollView
	keyboardShouldPersistTaps={'handled'}
	>
	<TouchableOpacity
		onPress={() => _click()}>
		<Text}>登录</Text>
	</TouchableOpacity>
</ScrollView>
```

