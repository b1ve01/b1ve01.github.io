# [Home](/)
# [../Home/Linux/User and Group Management](../)
# User
[Show how many users](#show-how-many-users)
<br/>  
## Show how many users
查看系統中有哪些可登錄用戶
```
getent passwd | grep -Ff /etc/shells | cut -d: -f1 | sort
```
getent passwd (數據庫名稱)類似 cat /etc/passwd (文件名稱), 但 getent passwd 遵循 /etc/nsswitch.conf 配置, 可能返回本地 + 網絡用戶; cat /etc/passwd 只顯示本地文件中的用戶, 不考慮網絡用戶源。 
<br/>  
-F 視作固定字符串,禁用正則表達式的特殊字符(如 . , * , + , [ ] 等)
<br/>  
例如: 
<br/>  
會匹配( . 匹配任意字符)
```
echo "/bin/bash" | grep "/bin.bash"
```
不會匹配(只尋找字面字符串"/bin.bash")
```
echo "/bin/bash" | grep -F "/bin.bash"
```
-f 讀取指定文件中的每一行用作獨立搜索
<br/> 
/etc/shells 文件存放系統認可的有效登錄 shell 列表 
<br/>  
所以  
```
getent passwd | grep -Ff /etc/shells
```
getent passwd 先輸出所有用戶的信息, 然後 grep -Ff /etc/shells 從 shells 中讀取有效 shell 路徑, 兩者再匹配對應的行
