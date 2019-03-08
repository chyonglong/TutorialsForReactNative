# react-native-navigation



## 跳到指定screen的上一个screen

获取当前screen 的navigation key
this.navigationKey = this.props.navigation.state.key;

用goback 跳到指定screen的上一个screen
this.props.navigation.goBack(this.navigationKey)

e.g. screen 1 2 3 我要在3 跳 跳到 1
在2中 :
this.navigationKey = this.props.navigation.state.key 传给 3
在3中 :
this.navigationKey = this.props.navigation.state.params.navigationKey;
this.props.navigation.goBack(this.navigationKey)



## 参考链接

[react-native-navigation](https://github.com/wix/react-native-navigation)

