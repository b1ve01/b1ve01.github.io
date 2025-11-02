# [Home](/)
# [../Linux/User and Group Management](../)
# User
- # [Check how many users](#check_how_many_users)
<br/>
<br/>
<br/>
<br/>

## Check how many users
```bash
getent passwd | grep -Ff /etc/shells | cut -d: -f1 | sort
```
