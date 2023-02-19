# 新装系统初始化工作

## 安装zsh包

centos ```yum -y install zsh```
ubuntu ```apt -y install zsh```

## 切换默认shell
```
chsh -s /bin/zsh
```

## 安装git
centos ```yum -y install git```
ubuntu ```apt -y install git```

## 安装oh my zsh 
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## 安装自动提示
### 自动提示zsh-autosuggestions
使用以下命令安装

```
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### 语法高亮zsh-syntax-highlighting
使用以下命令安装

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

编辑.zshrc

```
plugins=(
git
zsh-autosuggestions
zsh-syntax-highlighting
)
```

## 安装自动提示
```
wget http://mimosa-pudica.net/src/incr-0.2.zsh
mkdir ~/.oh-my-zsh/plugins/incr
mv incr-0.2.zsh ~/.oh-my-zsh/plugins/incr
echo 'source ~/.oh-my-zsh/plugins/incr/incr*.zsh' >> ~/.zshrc
source ~/.zshrc
```

## 修改主题
```ls ~/.oh-my-zsh/themes```

## 修改主题
```
vim ~/.zshrc

echo '
                _           
     /\        | |          
    /  \    ___| |__  _   _ 
   / /\ \  |_  / '_ \| | | |
  / ____ \  / /| | | | |_| |
 /_/    \_\/___|_| |_|\__,_|
' >> ~/.zshrc
```
## 更新配置文件

`source ~/.zshrc`

`sudo dpkg-reconfigure dash`
