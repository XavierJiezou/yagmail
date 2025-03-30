```python
import os
os.system("pip install git+https://github.com/XavierJiezou/yagmail.git")
import yagmail
yagmail.SMTP(
    user="邮箱", # 发件人邮箱地址
    password="授权码", # 授权码，QQ邮箱需要使用授权码而不是密码
    host="smtp.qq.com", # 邮箱服务器，谷歌邮箱是smtp.gmail.com
    proxy="http://localhost:7890", # 代理，如果没有代理可以不填
).send(
    to=["example@example.com", "example@example.com", "example@example.com"], # 收件人列表
    subject="subject", # 邮件主题
    contents="contents", # 邮件内容
)
```
