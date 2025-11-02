# [Home](/)
# [../Linux/User and Group Management](../)
# User
- # [Check how many users](#check-how-many-users)
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

## Check how many users
```bash
getent passwd | grep -Ff /etc/shells | cut -d: -f1 | sort
```
getent passwd (數據庫名稱)類似 cat /etc/passwd (文件名稱), 但 getent passwd 遵循 /etc/nsswitch.conf 配置, 可能返回本地 + 網絡用戶; cat /etc/passwd 只顯示本地文件中的用戶, 不考慮網絡用戶源。 
<br/>  
-F 視作固定字符串,禁用正則表達式的特殊字符(如. , * , + , [ ] 等)  
例如:  
```bash
echo "/bin/bash" | grep "/bin.bash"
```
會匹配(. 匹配任意字符)  

```bash
echo "/bin/bash" | grep -F "/bin.bash"
```
不會匹配(只尋找字面字符串"/bin.bash")
<br/>  
-f 讀取指定文件中的每一行用作獨立搜索
<br/> 
/etc/shells文件存放系統認可的有效登錄shell列表  
所以  
```bash
getent passwd | grep -Ff /etc/shells
```
getent passwd 先輸出所有用戶的信息, 然後 grep -Ff /etc/shells 從 shells中讀取有效shell路徑, 兩者再匹配對應的行
