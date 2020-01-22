# blfresh (碧蓝航线自动刷战斗脚本)

## 目录  

[0. 环境 ](#0)  
[1. 初始化 ](#1)  
........[1.1. 匹配模拟器窗口 ](#1.1)  
........[1.2. 匹配按钮位置 ](#1.2)  
................[1.2.1. 主界面四大按钮 ](#1.2.1)  
................[1.2.2. 确认舰队按钮 ](#1.2.2)  
................[1.2.3. 出击按钮 ](#1.2.3)  
................[1.2.4. 结算按钮 ](#1.2.4)  
........[1.3. 设定战斗等待时长 ](#1.3)  
[2. 使用 ](#2)  

<h2 name="0">0 环境</h2>

这里列出开发所用Python版本与相关PIP包版本

|程序名|版本|
|:----|:---|
|Python|3.6.6|
|pywin32|225|

~~_(CMD：那我呢？明明是我先来的！)_~~

<h2 name="1">1 初始化</h2>

1. 进入游戏，进入“特别作战”画面  
2. 打开CMD，进入脚本所在目录，输入`python3 blfresh.py check`(这里不需要管理员权限)  
3. 根据提示操作  

<h3 name="1.1">1.1 匹配模拟器窗口</h3>

4. 根据提示，选中模拟器窗口，复制以下内容到 `blconf.py` 中的 `窗口标题`  
`窗口句柄`不是必要的，当窗口标题变化时才需要填写
<div align="center">
  <img src="https://github.com/BoringCat/blfresh/blob/master/images/SelectWindow.png" alt=""/><br />
  （选择窗口提示与信息）
</div>

<h3 name="1.2">1.2 匹配按钮位置</h3>

<h4 name="1.2.1">1.2.1 主界面四大按钮</h4>

根据提示，将鼠标指针置于四大按钮上，并在CMD中按回车键输出按钮位置信息
<div align="center">
  <img src="https://github.com/BoringCat/blfresh/blob/master/images/MainPage.png" alt=""/><br />
  （主界面四大按钮）
</div>

将信息连同括号复制到 `blconf.py` 中 `mode` 的各个难度中

<h4 name="1.2.2">1.2.2 确认舰队按钮</h4>

根据提示，将鼠标指针置于确认舰队按钮上，在CMD中按回车键输出按钮位置信息，并复制内容连同括号到 `blconf.py` 中的 `选择舰队` 
<div align="center">
  <img src="https://github.com/BoringCat/blfresh/blob/master/images/Fleet_Select.png" alt=""/><br />
  （确认舰队按钮）
</div>

<h4 name="1.2.3">1.2.3 出击按钮</h4>

根据提示，将鼠标指针置于出击按钮上，在CMD中按回车键输出按钮位置信息，并复制内容连同括号到 `blconf.py` 中的 `确认出击` 
<div align="center">
  <img src="https://github.com/BoringCat/blfresh/blob/master/images/Weigh_Anchor.png" alt=""/><br />
  （出击按钮）
</div>

<h4 name="1.2.4">1.2.4 结算按钮</h4>

根据提示，将鼠标指针置于结算按钮上，在CMD中按回车键输出按钮位置信息，并复制内容连同括号到 `blconf.py` 中的 `战斗结算` 
<div align="center">
  <img src="https://github.com/BoringCat/blfresh/blob/master/images/Victory.png" alt=""/><br />
  （结算按钮）
</div>

<h3 name="1.3">1.3 设定战斗等待时长</h3>

在 `blconf.py` 中 `mode` 的各个难度中输入等待时间(秒)，需要确保在这个时间内战斗能进行到结算页面

<h2 name="2">2 使用</h2>

`blfresh.py (难度) (次数)`

刷困难： `python3 blfresh.py Hard 15`  
刷普通： `python3 blfresh.py Normal 15`  
刷简单： `python3 blfresh.py Easy 15`  
(或者输入自己改mode里面的名字)
