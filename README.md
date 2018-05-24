# tzdata
A uncompressed zip file of IANA time zone database files, can be used to set timezone in go program.

Example
========

```
// rootPath is the workdir or some absolute path
os.Setenv("ZONEINFO", filepath.Join(rootPath,"assets/tz/data.zip"))
l,_ := time.LoadLocation("Asia/Shanghai")
fmt.Println(time.Now().In(l)) // 2018-05-24 18:29:45.988478846 +0800 CST
l,_ = time.LoadLocation("America/Adak")
fmt.Println(time.Now().In(l)) // 2018-05-24 01:29:45.98922405 -0900 HDT
```
