管理信息系统第三次作业
====================
一、	数据库建表
---------------
保养消耗表

DROP TABLE IF EXISTS `consume`;

CREATE TABLE `consume` (

  `id` int(11) NOT NULL,
  
  `name` varchar(225) NOT NULL,
  
  `count` int(11) DEFAULT NULL,
  
  `lcount` int(11) DEFAULT NULL,
  
  `proid` int(11) DEFAULT NULL,
  
 PRIMARY KEY (`id`)
 
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

设备表

DROP TABLE IF EXISTS `equipment`;

CREATE TABLE `equipment` ( 

  `id` int(11) NOT NULL,
  
  `rid` int(11) NOT NULL,
  
  `date` date NOT NULL,
  
  `tid` int(11) NOT NULL,
  
  PRIMARY KEY (`id`)
  
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

设备类型表

DROP TABLE IF EXISTS `equipment_type`;

CREATE TABLE `equipment_type` (

  `id` int(11) NOT NULL, 
  
  `etype` varchar(225) NOT NULL,
  
  `rtype` varchar(225) NOT NULL,
  
  PRIMARY KEY (`id`)
  
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

保养人表

DROP TABLE IF EXISTS `people`;

CREATE TABLE `people` (

  `id` int(11) NOT NULL,
  
  `name` tinytext NOT NULL,
  
  PRIMARY KEY (`id`)
  
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

保养项目表

DROP TABLE IF EXISTS `project`;

CREATE TABLE `project` (

  `id` int(11) NOT NULL,
  
  `content` text NOT NULL,
  
  `situation` text NOT NULL,
  
  `remarks` varchar(45) NOT NULL,
  
  `etid` int(11) DEFAULT NULL,
  
  PRIMARY KEY (`id`)
  
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

保养记录表

DROP TABLE IF EXISTS `record`;

CREATE TABLE `record` (

  `id` int(11) NOT NULL,
  
  `date` date NOT NULL,
  
  `describe` text CHARACTER SET big5 NOT NULL,
  
  `pid` int(11) NOT NULL,
  
  PRIMARY KEY (`id`)
  
) ENGINE=InnoDB DEFAULT CHARSET=utf8;

二、	查询
---------
select * from record where id='1'

select * from equipment where id='1'

select * from type where id='1'

SELECT * FROM people where name='小明'

SELECT * FROM project where tid='1'


![1](https://cloud.githubusercontent.com/assets/16081097/19418450/a277da3e-93f6-11e6-8b66-dbb64707cef2.jpg)

![2](https://cloud.githubusercontent.com/assets/16081097/19418476/21fb9af2-93f7-11e6-9c99-ed22c7602d48.png)

![3](https://cloud.githubusercontent.com/assets/16081097/19418480/2bbc1d64-93f7-11e6-98ee-670eed38f661.png)

![4](https://cloud.githubusercontent.com/assets/16081097/19418483/32881940-93f7-11e6-80d2-37faa6f9f4de.png)

![5](https://cloud.githubusercontent.com/assets/16081097/19418485/37a0a460-93f7-11e6-8ef9-a7233da57faa.png)


三、	ER图
----------
![er](https://cloud.githubusercontent.com/assets/16081097/19418487/3b1b302e-93f7-11e6-88c2-e295e0d800ae.png)

Axure网站链接
------------
http://2u63xd.axshare.com/

Axure原型链接
------------
http://pan.baidu.com/s/1jHOqotS
