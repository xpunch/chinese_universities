# Chinese Universities
中国大陆所有大学数据，数据库脚本，数据来自于学信网(https://gaokao.chsi.com.cn/sch/)。

## 院校类型
综合、工科、师范、财经、政法、语言、医药、农业、林业、民族、艺术、体育、军事

## JSON
```json
{
    "name": "北京大学",			//名称
    "type": "综合",				//院校类型
    "region": "北京",			//院校所在地
    "superior": "教育部",		//教育行政主管部门
    "is_985": true,				//985院校
    "is_211": true,				//211院校
    "syl": "双一流A",			//双一流
    "is_yldx": true,			//一流大学建设院校
    "is_ylxk": false,			//一流学科建设学院
    "is_bk": true,				//本科
    "has_yjsy": false,			//研究生院
    "score": 4.7				//满意度
}
```

## MySQL
```sql
CREATE TABLE `chinese_universities` (
	`id` BIGINT AUTO_INCREMENT,
	`name` VARCHAR (32),			#名称
	`type` VARCHAR (2),				#院校类型
	`region` VARCHAR (16),			#院校所在地
	`superior` VARCHAR (16),		#教育行政主管部门	
	`is_985` Tinyint,				#985院校
	`is_211` Tinyint,				#211院校
	`syl` varchar(4),				#双一流
	`is_yldx` Tinyint,				#一流大学建设院校
	`is_ylxk` Tinyint,				#一流学科建设院校
	`is_bk` Tinyint,				#本科
	`has_yjsy` Tinyint,				#研究生院
	`score` float,					#满意度
	PRIMARY KEY (`id`)
);
```