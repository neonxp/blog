---
title: "⚙️ Скрипт выставления TTL в macOS для обхода раздачи интернета в Йоте"
date: 2018-08-16T14:44:19+03:00
subtitle: ""
tags: ["разное"]
---

Накидал небольшой AppleScript для коллеги выставляющий TTL=65 для обхода ограничений Йоты на раздачу интернета с телефона.

Если коротко, то вот код:

```
try
	do shell script "sudo sysctl -w net.inet.ip.ttl=65" with administrator privileges
	display notification "TTL=65 сделан"
on error errorMessage number errorNumber
	display alert errorNumber message errorMessage
end try
```

Для ленивых вот скрипт в виде программы, чтобы удобно запускать: [https://cloud.mail.ru/public/G4d2/mjwMQkLF6](https://cloud.mail.ru/public/G4d2/mjwMQkLF6)