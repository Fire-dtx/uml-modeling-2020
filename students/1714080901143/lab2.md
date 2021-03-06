# 实验二: 用例建模

## 一、实验目标

1. 理解UML用例建模的概念
2. 掌握画用例图的方法

## 二、实验内容

1. 选择个人建模选题
2. 根据建模选题画用例图

## 三、实验步骤

1. 在GitHub的issues中发布自己的建模选题

    ```
    选题：#364 ip代理池
    功能：
    1. 从代理网站获取免费代理ip，保存代理ip
    2. 验证已经存进数据库中的代理ip是否仍是有效，保存有效代理
    3. 提供有效的代理ip
    ```

2. 找出建模选题中的用例和参与者

    ```
    用例：爬取代理、验证代理、获取可用代理
    参与者：Administrator、user
    ```

3. 在StarUML中画出用例图，首先画出用例：爬取代理、验证代理、获取可用代理，接着，画出参与者：Administrator，user，最后将参与者与相关用例用直线连起来

4. 导出用例图，并使用markdown编写实验报告，在实验报告中使用导出的用例图

## 四、实验结果

### 1. 画图

![用例图](./Lab2_UseCaseDiagram.jpg)  
图1. ip代理池用例图

## 表1：爬取代理用例规约  

用例编号  | UC01
-|:-
用例名称  | 爬取代理 
前置条件  |         
后置条件  |         
基本流程  | 1.Adminstrator输入爬取命令
~| 2.系统检查命令正确，执行爬取命令
~| 3.系统爬取代理网站
~| 4.系统解析爬取到的页面，提取代理ip，保存代理
~| 5.系统提示“成功”  
扩展流程  | 2.1 系统检查发现命令错误，提示“命令错误” 
~| 3.1 系统访问目标网站出错，提示“访问错误” 


## 表2：验证代理用例规约  

用例编号  | UC02   
-|:-
用例名称  | 验证代理 
前置条件  |      
后置条件  |      
基本流程  | 1.Adminstrator输入验证命令
~| 2.系统检查命令正确，执行验证  
~| 3.系统使用代理ip，访问网页，访问网页成功，保存有效代理
~| 4.系统提示“成功”
扩展流程  | 2.1 系统检查发现命令错误，提示“命令错误” 
~| 3.1 系统使用代理ip，访问网页，访问网页失败，提示“代理无效”


## 表3：获取可用代理用例规约  

用例编号  | UC03
-|:-
用例名称  | 获取可用代理  
前置条件  |       
后置条件  |         
基本流程  | 1.Adminstrator或user输入获取代理命令      
~| 2.系统检查命令正确，执行获取命令 
~| 3.系统查询代理，查询成功，返回代理，删除代理
~| 4.系统提示“成功”
扩展流程  | 2.1 系统检查发现命令错误，提示“命令错误”
~| 3.1  系统查询失败，提示“无可获取代理”  
