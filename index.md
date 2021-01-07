Mac terminal直接远程+ termius 远程连接
1.切换root账号
2.Mac创建秘钥对： terminal 输入   ssh-keygen -t rsa
2.1 查找生成的秘钥对文件 一般文件默认名为id_rsa,id_rsa.pub, 可通过terminal open ~/.ssh  找到，一般保存在user中的.ssh文件夹中
2.2 用文本编辑器打开公钥文件，复制，打开GCP的元数据的SSH秘钥， 添加公钥

3. Mac terminal直接连接， shell远程连接， 输入  SSH 用户名@外部ip地址 ， 方便下次使用可以创建一个名称

4. 配置termius
4.1 打开performance 中的keychain， 添加key，  label随便写， 密码空着， 复制私钥中的所有内容粘贴
4.2 新建host， address:外部ip，  用户名：前面设置秘钥对的用户名，此处设置的是MAc用户的用户名， 密码则点击Key选择刚刚设置好的key，
4.3 双击配置好的host可连接成功。
