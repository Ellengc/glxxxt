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

![alt text](/path/to/1.png "Title")
![alt text](/path/to/2.png "Title")
![alt text](/path/to/3.png "Title")
![alt text](/path/to/4.png "Title")
![alt text](/path/to/5.png "Title")
三、	ER图
----------
![alt text](/path/to/er.png "Title")

Axure网站链接
------------
http://2u63xd.axshare.com/

Axure原型链接
------------
http://pan.baidu.com/s/1jHOqotS
