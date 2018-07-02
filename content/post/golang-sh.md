---
title: Go программа как shell скрипт
date: 2018-07-02
slug: go-prog-as-shell
tags: [ "разное" ]
---

Маленькая заметка.

Программы на Go можно использовать как shell скрипты без предварительной компиляции или чего -то такого.

Достаточно в начале программы добавить строку `//usr/bin/env go run $0 $@ ; exit`, затем дать права на запуск (`chmod +x script.go`) и можно запускать (`./script.go`)

Пример:

```
//usr/bin/env go run $0 $@ ; exit
package main

import "fmt"

func main() {
	fmt.Println("Hello, world!")
}
```

```
➜  ~ chmod +x test.go
➜  ~ ./test.go
Hello, world!
```



