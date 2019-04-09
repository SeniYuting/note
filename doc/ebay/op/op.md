# 基本操作

## 访问Production（不需要bastion）
```
1. 开机后执行：ssh -N -f -D 2001 phxbastion100.phx.ebay.com
2. 输入prod密码
3. 输入PIN+ubikey
4. 后面直接ssh prod机器，例如：ssh slcunix71.slc.ebay.com
5. 输入prod密码，再输入PIN+ubikey
```

## 从Gitlab拷贝代码示例
```
1. git clone https://git.vip.ebay.com/cosa/KeyHub.git
2. 输入用户名：yutcao
3. 输入密码：PIN+ubikey
```

## 生成SSH文件
```
ssh-keygen -t rsa -C “yutcao@ebay.com”
```

[返回目录](../CONTENTS.md)