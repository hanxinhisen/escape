###基于 golang builin包
####实现python中 urllib.parse.quote(uri, safe='-_.~/') safe部分
新增 
```PathEscapeWithOutCharacters```
```QueryEscapeWithOutCharacters```

其余保持不变

使用方法
```
import "github.com/hanxinhisen/escape"


fun main(){
 // 例子1
 url := escape.PathEscapeWithOutCharacters("/aa/bb","-_.~/")  //后面参数中的字符将不进行转换
 // output : /aa/bb
 
 // 例子2
 url := escape.PathEscapeWithOutCharacters("/aa/bb","-_.~")  //后面参数中的字符将不进行转换
 // output : %2Faa%2Fbb
 
 QueryEscapeWithOutCharacters用法相同
}

```


