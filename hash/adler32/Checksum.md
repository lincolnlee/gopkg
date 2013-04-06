## func Checksum(data []byte) uint32

参数列表

- data 表示需要校验返回Adler-32校验数据的字节数组 

返回值：

- 返回uint32

功能说明：

这个函数主要是用来校验返回Adler-32算法的校验数据。

代码实例：

	package main

	import (
		"fmt"
		h "hash/adler32"
	)

	func main() {
		str := "Hello World."
		strbyte := []byte(str)
		i := h.Checksum(strbyte)
		fmt.Println(i)
	}