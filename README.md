# satr.codes--SQL-102


مشروع

باستخدام ما تعلمته خلال هذهِ الدورة قم بتطبيق المتطلبات التالية، علما أن هذا المشروع مكمّل لمشروع SQL المستوى الأول.


المتطلبات:


إنشاء جدول للطلاب المتفوقين من جدول الطلاب، بحيث يحتوي هذا الجدول على بيانات الطلاب الذي يكون معدلهم التراكمي أعلى من ٩٠.
إنشاء جدول للطلاب الغير مجتازين من جدول الطلاب، بحيث يحتوي هذا الجدول على بيانات الطلاب الذي يكون معدلهم التراكمي أقل من ٦٠.
عرض أسماء الطلاب التي تبدأ بحرف A.
عرض أسماء الطلاب التي تحتوي أسمائهم على أربع خانات.
تطبيق AVG, MAX, MIN) Aggregate functions) على المعدل التراكمي للطالب مع إضافة تسمية واضحة للناتج.
حصر وعرض أسماء الطلاب المتفوقين في المستوى السادس الحاصلين على معدل تراكمي يساوي 100.
عرض الطلاب اللذين في المستوى الأول وأعمارهم بين ١٥ و ١٦ سنة.
عرض عدد الطلاب الموجودين بالمستوى ٢.
استعراض مسارات الطلاب في المدرسة بدون تكرار.
عرض أسماء المواد ويتم عرض الكلمات بالأحرف الكبيرة.
عرض المتوسط الحسابي للمعدل التراكمي وقرب الرقم لأقرب أصغر عدد (باستخدام numeric functions).
تبديل جميع الصفوف من جدول الطلاب التي تحتوي على الجنس F إلى Female، و M إلى Male (باستخدام string functions).
تحديث المعدل التراكمي للطلاب الذي معدلهم التراكمي أقل من ٦٠ وزيادة معدلهم بخمس درجات.






create database student






use student;
create table student(
id int primary key,
nam varchar (255),
Average varchar (255),
Levels varchar (255),
grades varchar(255),
age int
);




use student;
insert into student
values(1,'Robert','80','level6','m','15'),
(2,'Veronica','15','level6','f','8'),
(3,'Joseph','50','level4','m','15'),
(4,'Aaron','15','level5','m','6'),
(5,'Cory','15','level1','f','11'),
(6,'Kimberly','90','level6','m','8'),
(7,'Julie','100','level5','m','12'),
(8,'Darrell','60','level3','f','6'),
(9,'Johnny','80','level4','m','10'),
(10,'Christopher','50','level6','f','12'),
(11,'Amanda','50','level6','m','6'),
(12,'Jessica','100','level4','m','12'),
(13,'Teresa','46','level5','f','10'),
(14,'Anthony','50','level3','m','6'),
(15,'Mary','50','level2','f','11'),
(16,'Ryan','46','level2','f','15'),
(17,'April','46','level4','m','8'),
(18,'Tyler','50','level6','f','8'),
(19,'Thomas','100','level5','m','8'),
(20,'Alexis','90','level3','m','12'),
(21,'Gregory','60','level2','f','12'),
(22,'Tyler','100','level6','m','8'),
(23,'Christopher','80','level1','m','6'),
(24,'Sheila','15','level3','m','6'),
(25,'Michelle','60','level3','f','11'),
(26,'Deanna','60','level5','m','10'),
(27,'Sean','100','level4','m','8'),
(28,'Shannon','50','level5','m','11'),
(29,'Elizabeth','46','level3','m','6'),
(30,'Leonard','90','level4','m','6'),
(31,'Jackie','60','level6','m','12'),
(32,'Ryan','15','level5','f','6'),
(33,'Melissa','90','level1','m','10'),
(34,'Rachel','100','level1','m','15'),
(35,'Riley','15','level3','m','11'),
(36,'Miranda','50','level4','m','10'),
(37,'Stephen','80','level6','f','6'),
(38,'Sheri','80','level4','f','12'),
(39,'Cathy','60','level6','m','12'),
(40,'Matthew','80','level5','m','15'),
(41,'Riley','50','level5','m','10'),
(42,'Jessica','60','level4','m','10'),
(43,'Jacob','60','level2','m','12'),
(44,'Joseph','90','level3','f','11'),
(45,'Laura','15','level1','m','12'),
(46,'Sarah','50','level2','f','8'),
(47,'Debra','50','level5','m','12'),
(48,'Stephanie','15','level2','f','10'),
(49,'Amy','60','level4','m','10'),
(50,'Mark','60','level1','m','8'),
(51,'Erik','90','level5','m','6'),
(52,'Joel','46','level5','f','15'),
(53,'Michelle','15','level4','m','6'),
(54,'Emily','80','level6','f','12'),
(55,'Theresa','15','level5','f','10'),
(56,'Joel','15','level2','f','10'),
(57,'Michael','60','level3','f','15'),
(58,'Kimberly','90','level5','f','11'),
(59,'Jacob','50','level5','m','12'),
(60,'Mathew','46','level5','m','8'),
(61,'Briana','60','level6','m','6'),
(62,'Nicholas','80','level4','f','10'),
(63,'Jonathan','15','level2','m','15'),
(64,'Olivia','60','level3','f','12'),
(65,'Adrienne','100','level4','m','6'),
(66,'Patricia','15','level5','m','11'),
(67,'Joshua','100','level3','m','11'),
(68,'Steven','100','level5','f','11'),
(69,'Denise','80','level6','f','10'),
(70,'Brian','15','level1','f','8'),
(71,'John','50','level1','f','8'),
(72,'Elizabeth','60','level4','f','12'),
(73,'Michelle','90','level2','m','8'),
(74,'Thomas','80','level5','m','12'),
(75,'Aaron','60','level5','f','11'),
(76,'Maureen','90','level4','m','8'),
(77,'Joseph','80','level2','m','11'),
(78,'Stephanie','60','level1','f','11'),
(79,'Cheryl','90','level3','m','6'),
(80,'James','100','level6','f','12'),
(81,'Lauren','90','level1','m','11'),
(82,'Mary','80','level2','m','12'),
(83,'Yolanda','80','level3','m','10'),
(84,'Kevin','15','level1','f','8'),
(85,'James','60','level5','m','6'),
(86,'Kelly','15','level2','f','6'),
(87,'Gregory','80','level6','m','6'),
(88,'Christopher','60','level2','f','11'),
(89,'Alexis','100','level1','m','11'),
(90,'Raymond','46','level6','f','15'),
(91,'Kimberly','15','level2','f','15'),
(92,'Dakota','100','level4','f','11'),
(93,'Felicia','100','level5','m','6'),
(94,'Andrew','90','level1','m','15'),
(95,'Katherine','80','level4','m','6'),
(96,'Carrie','90','level1','m','8'),
(97,'Toni','46','level5','m','6'),
(98,'Megan','60','level3','m','12'),
(99,'Michelle','60','level2','f','12'),
(100,'Diana','80','level2','f','10'),
(101,'Zachary','80','level6','m','6'),
(102,'Jacob','90','level4','f','15'),
(103,'Rebecca','46','level1','m','6'),
(104,'Courtney','15','level5','f','8'),
(105,'Savannah','80','level1','m','15'),
(106,'Kara','60','level5','f','8'),
(107,'Nicole','46','level3','f','12'),
(108,'Allen','60','level1','f','15'),
(109,'Sarah','46','level5','f','11'),
(110,'Cameron','100','level5','m','15'),
(111,'Carrie','100','level6','m','11'),
(112,'Tracy','60','level5','m','6'),
(113,'Amanda','90','level6','m','6'),
(114,'Lee','100','level3','f','10'),
(115,'Matthew','100','level6','f','8'),
(116,'Aaron','60','level1','m','15'),
(117,'Laura','60','level3','m','15'),
(118,'Danielle','80','level2','f','8'),
(119,'Cindy','50','level5','m','12'),
(120,'Sheila','80','level3','m','15'),
(121,'Jessica','50','level5','f','11'),
(122,'Devin','80','level6','m','10'),
(123,'Lauren','60','level1','m','11'),
(124,'Jacob','50','level6','f','6'),
(125,'Jeremy','46','level1','m','11'),
(126,'Evan','46','level2','f','15'),
(127,'Tiffany','60','level1','m','10'),
(128,'Amber','80','level1','f','6'),
(129,'Lindsay','46','level3','m','11'),
(130,'Jeffrey','46','level6','m','8'),
(131,'Whitney','46','level2','m','10'),
(132,'Kristie','15','level1','m','11'),
(133,'Lee','60','level1','f','12'),
(134,'Amanda','60','level2','f','6'),
(135,'Timothy','50','level3','m','10'),
(136,'Michael','80','level3','f','12'),
(137,'Matthew','80','level3','m','15'),
(138,'Ashlee','46','level1','m','12'),
(139,'Laura','60','level2','f','11'),
(140,'David','46','level6','f','11'),
(141,'Jasmin','46','level6','m','10'),
(142,'Thomas','15','level3','f','11'),
(143,'Crystal','60','level3','f','6'),
(144,'Glenda','60','level2','m','8'),
(145,'Miranda','46','level4','m','6'),
(146,'Christine','15','level3','f','11'),
(147,'Troy','90','level2','m','8'),
(148,'Tamara','15','level4','m','11'),
(149,'Melissa','46','level2','m','6'),
(150,'Veronica','46','level2','m','10'),
(151,'Jennifer','100','level4','m','15'),
(152,'John','100','level4','f','15'),
(153,'Jimmy','60','level2','f','12'),
(154,'Charlotte','90','level5','f','6'),
(155,'April','60','level6','f','10'),
(156,'Evan','80','level2','m','12'),
(157,'Julie','100','level6','f','10'),
(158,'Danielle','60','level2','m','10'),
(159,'Kenneth','50','level6','m','15'),
(160,'Loretta','80','level2','m','10'),
(161,'Daniel','46','level4','f','6'),
(162,'Mary','60','level1','m','12'),
(163,'Susan','90','level1','m','11'),
(164,'Anthony','80','level2','f','10'),
(165,'Michelle','60','level3','f','6'),
(166,'Cynthia','80','level3','m','8'),
(167,'Patricia','15','level4','f','8'),
(168,'Brian','50','level3','m','15'),
(169,'Tracy','80','level1','m','12'),
(170,'John','80','level2','f','8'),
(171,'Alicia','46','level6','f','15'),
(172,'Willie','80','level2','f','8'),
(173,'Jennifer','46','level4','m','15'),
(174,'Justin','46','level6','m','6'),
(175,'David','60','level3','f','15'),
(176,'Anna','15','level4','m','10'),
(177,'Ronald','90','level3','f','8'),
(178,'Michelle','15','level4','f','6'),
(179,'Andrew','15','level6','m','10'),
(180,'Robert','15','level5','f','15'),
(181,'Seth','90','level1','m','15'),
(182,'Rebecca','90','level3','m','8'),
(183,'Andrea','100','level5','m','8'),
(184,'Jeanette','15','level5','m','15'),
(185,'Hunter','60','level3','f','10'),
(186,'Amanda','46','level6','f','15'),
(187,'William','100','level4','f','11'),
(188,'Derek','100','level2','m','15'),
(189,'Aaron','100','level2','m','8'),
(190,'Nathan','100','level4','m','10'),
(191,'Adrienne','100','level3','f','8'),
(192,'Sheri','90','level3','f','8'),
(193,'Morgan','50','level5','f','6'),
(194,'Eric','60','level4','m','8'),
(195,'Alicia','100','level4','f','12'),
(196,'Jacob','15','level1','f','10'),
(197,'Emily','46','level3','m','11'),
(198,'Jill','90','level1','f','8'),
(199,'Matthew','50','level5','m','10'),
(200,'Michael','60','level3','m','15'),
(201,'Megan','50','level1','m','11'),
(202,'Adrienne','50','level5','f','6'),
(203,'Rachel','60','level2','f','11'),
(204,'Kathleen','100','level4','f','8'),
(205,'Steven','90','level5','m','15'),
(206,'Madison','46','level2','m','10'),
(207,'Norma','46','level2','m','10'),
(208,'Jacob','90','level4','m','12'),
(209,'Christopher','80','level2','m','10'),
(210,'Thomas','50','level3','m','12'),
(211,'Shannon','80','level3','m','6'),
(212,'Mary','80','level1','m','10'),
(213,'Lisa','90','level1','f','8'),
(214,'James','46','level1','m','11'),
(215,'Shannon','46','level4','m','8'),
(216,'Jonathan','46','level3','m','8'),
(217,'Eric','46','level5','f','6'),
(218,'Stephen','80','level5','f','10'),
(219,'Lori','100','level5','f','8'),
(220,'Alexander','50','level2','f','8'),
(221,'Jeffrey','60','level2','f','15'),
(222,'Melissa','60','level4','f','11'),
(223,'Troy','46','level2','m','11'),
(224,'Charles','60','level2','m','12'),
(225,'Christopher','100','level1','m','6'),
(226,'Ryan','100','level3','f','6'),
(227,'Sheila','50','level3','m','8'),
(228,'Richard','50','level6','f','6'),
(229,'Joshua','50','level5','m','11'),
(230,'Diana','50','level3','m','8'),
(231,'Brianna','100','level6','m','12'),
(232,'Christopher','46','level2','f','10'),
(233,'Douglas','46','level4','f','11'),
(234,'Ashley','15','level1','m','10'),
(235,'Joanne','46','level3','f','8'),
(236,'Ryan','50','level1','f','6'),
(237,'Leonard','100','level4','m','10'),
(238,'Tanner','90','level5','f','11'),
(239,'Jessica','90','level4','f','8'),
(240,'Madeline','90','level1','m','15'),
(241,'Christopher','60','level4','f','15'),
(242,'Rebecca','46','level3','f','11'),
(243,'Jamie','80','level2','f','15'),
(244,'Andrew','50','level6','f','10'),
(245,'Nicole','80','level4','f','11'),
(246,'Hunter','80','level1','m','12'),
(247,'Sheila','15','level1','m','10'),
(248,'Samuel','80','level4','f','12'),
(249,'Heather','46','level3','m','12'),
(250,'Angel','60','level4','m','10'),
(251,'Jennifer','80','level3','m','10'),
(252,'Lauren','60','level4','f','6'),
(253,'Jacob','50','level5','m','12'),
(254,'Luis','90','level4','m','12'),
(255,'Beverly','50','level5','m','12'),
(256,'Christine','90','level2','m','15'),
(257,'Billy','15','level4','f','15'),
(258,'Michelle','80','level2','f','12'),
(259,'Alex','90','level2','m','11'),
(260,'John','80','level5','m','6'),
(261,'Eugene','90','level3','f','11'),
(262,'Marissa','50','level5','m','11'),
(263,'Robert','60','level1','f','6'),
(264,'Kristina','90','level6','m','11'),
(265,'Lisa','15','level4','m','6'),
(266,'Aaron','80','level5','f','6'),
(267,'Tracey','80','level6','f','12'),
(268,'Charlotte','60','level4','m','6'),
(269,'Carl','15','level3','f','6'),
(270,'Jessica','100','level2','m','6'),
(271,'Timothy','80','level6','m','12'),
(272,'Mark','50','level1','f','8'),
(273,'Hannah','90','level5','f','6'),
(274,'Sarah','90','level1','m','12'),
(275,'Morgan','15','level2','f','6'),
(276,'Patrick','90','level6','f','12'),
(277,'Deanna','100','level4','m','15'),
(278,'Amanda','46','level2','m','8'),
(279,'Carrie','90','level5','m','11'),
(280,'Maria','80','level2','m','11'),
(281,'Amanda','46','level2','f','12'),
(282,'Christopher','80','level6','f','11'),
(283,'Derek','15','level2','m','12'),
(284,'Sarah','50','level5','f','15'),
(285,'Crystal','100','level1','f','6'),
(286,'Keith','46','level3','m','11'),
(287,'Jeffrey','46','level4','m','12'),
(288,'Dana','90','level4','m','6'),
(289,'Erica','100','level6','m','11'),
(290,'Daniel','50','level6','m','12'),
(291,'Elizabeth','90','level5','m','12'),
(292,'Jill','90','level2','f','10'),
(293,'Daniel','60','level5','m','8'),
(294,'Stephen','90','level2','f','8'),
(295,'Samantha','90','level6','f','8'),
(296,'Robert','90','level2','f','10'),
(297,'Ann','46','level4','f','11'),
(298,'Amanda','60','level2','m','12'),
(299,'Deanna','15','level2','f','6'),
(300,'David','50','level2','f','10'),
(301,'Jason','90','level4','m','10'),
(302,'Angela','100','level5','m','6'),
(303,'Jerry','90','level4','f','8'),
(304,'Amanda','90','level6','m','11'),
(305,'Richard','50','level6','m','10'),
(306,'Jessica','100','level1','f','10'),
(307,'Aaron','46','level1','f','12'),
(308,'Danielle','90','level3','m','12'),
(309,'Susan','15','level6','m','6'),
(310,'Andrew','90','level4','f','12'),
(311,'John','60','level4','m','6'),
(312,'Leslie','60','level3','f','6'),
(313,'Jill','46','level4','m','10'),
(314,'Leslie','46','level6','f','6'),
(315,'Andrea','46','level6','f','15'),
(316,'Susan','80','level6','f','10'),
(317,'Joseph','46','level3','m','12'),
(318,'Kylie','100','level4','f','10'),
(319,'Kenneth','15','level6','m','15'),
(320,'Jeffrey','46','level1','m','11'),
(321,'Emily','60','level2','f','12'),
(322,'Karen','80','level1','f','11'),
(323,'Sheila','90','level4','f','6'),
(324,'Michael','46','level6','f','11'),
(325,'Lisa','15','level2','f','10'),
(326,'Brianna','50','level1','m','12'),
(327,'Michael','46','level6','f','15'),
(328,'Melissa','80','level4','f','12'),
(329,'Amy','100','level3','f','12'),
(330,'Matthew','80','level2','f','8'),
(331,'Amanda','46','level3','f','12'),
(332,'Ryan','60','level3','f','11'),
(333,'Tanya','80','level1','m','11'),
(334,'Mark','50','level2','f','11'),
(335,'Jennifer','60','level5','m','8'),
(336,'Robert','100','level5','f','12'),
(337,'Jessica','15','level5','f','8'),
(338,'Jennifer','50','level6','m','6'),
(339,'Amanda','60','level3','f','12'),
(340,'Carl','90','level4','f','15'),
(341,'Christopher','60','level2','f','15'),
(342,'Dorothy','80','level2','f','8'),
(343,'Jeffrey','15','level1','f','6'),
(344,'Shari','15','level4','m','6'),
(345,'Thomas','50','level5','m','15'),
(346,'Robert','80','level6','m','10'),
(347,'Kenneth','90','level5','f','12'),
(348,'Joseph','46','level2','m','11'),
(349,'Kimberly','80','level6','m','10'),
(350,'Shannon','80','level1','m','12'),
(351,'Angela','100','level5','m','10'),
(352,'Anne','50','level3','m','11'),
(353,'Andre','46','level6','m','6'),
(354,'Samantha','100','level1','f','12'),
(355,'Travis','15','level5','m','15'),
(356,'Patrick','60','level5','m','15'),
(357,'Kayla','90','level6','f','12'),
(358,'Amanda','60','level2','f','15'),
(359,'Daniel','100','level2','m','15'),
(360,'Anne','80','level1','m','12'),
(361,'Laura','46','level1','f','11'),
(362,'Thomas','80','level2','m','10'),
(363,'Allen','60','level6','m','6'),
(364,'Marvin','80','level5','f','10'),
(365,'Mandy','60','level2','m','6'),
(366,'Dana','60','level5','m','6'),
(367,'Alexis','60','level3','m','6'),
(368,'Derrick','15','level2','m','6'),
(369,'Mark','15','level6','f','11'),
(370,'Danielle','100','level2','f','15'),
(371,'Michelle','50','level6','f','10'),
(372,'Luis','100','level2','f','15'),
(373,'Timothy','15','level1','m','8'),
(374,'Michelle','46','level6','f','8'),
(375,'Joseph','80','level3','f','6'),
(376,'Michael','90','level4','m','6'),
(377,'Thomas','100','level2','m','11'),
(378,'Michael','60','level6','f','8'),
(379,'Monica','15','level4','m','10'),
(380,'Justin','60','level4','m','12'),
(381,'Sheila','46','level6','m','6'),
(382,'Christina','50','level5','m','10'),
(383,'Heather','90','level1','f','8'),
(384,'Anthony','15','level5','f','10'),
(385,'Joseph','46','level6','f','8'),
(386,'Brenda','60','level3','f','6'),
(387,'Michael','80','level2','m','15'),
(388,'Dawn','100','level3','m','8'),
(389,'Jeffrey','90','level6','m','12'),
(390,'Alexander','60','level3','m','12'),
(391,'Kimberly','90','level5','f','15'),
(392,'Timothy','60','level1','f','15'),
(393,'Beverly','46','level6','f','11'),
(394,'Michelle','50','level3','f','11'),
(395,'Jamie','80','level5','f','11'),
(396,'Joseph','90','level2','m','11'),
(397,'Nancy','46','level2','f','12'),
(398,'Heather','90','level1','f','11'),
(399,'Richard','60','level5','f','8'),
(400,'Lisa','15','level5','f','12'),
(401,'Martha','46','level3','f','6'),
(402,'Tara','100','level3','m','6'),
(403,'Steven','80','level2','m','15'),
(404,'Robert','80','level2','f','11'),
(405,'Shannon','100','level4','m','8'),
(406,'Tracy','60','level3','f','15'),
(407,'Emily','50','level6','f','12'),
(408,'Angela','50','level3','f','8'),
(409,'Nicole','60','level2','m','6'),
(410,'Roy','60','level5','f','11'),
(411,'Jerry','15','level1','m','11'),
(412,'Jennifer','15','level2','m','8'),
(413,'Felicia','50','level1','m','6'),
(414,'Jeanette','100','level5','f','11'),
(415,'James','80','level1','m','11'),
(416,'Juan','46','level5','m','8'),
(417,'Ashlee','80','level6','m','8'),
(418,'Derek','50','level1','m','15'),
(419,'Jessica','46','level3','m','12'),
(420,'Brandi','60','level3','m','10'),
(421,'Sara','100','level5','f','15'),
(422,'Christina','46','level5','m','6'),
(423,'Amy','80','level3','m','15'),
(424,'Randy','50','level5','m','10'),
(425,'Kylie','100','level2','m','6'),
(426,'Robert','50','level6','f','12'),
(427,'Frank','50','level4','m','11'),
(428,'Katherine','15','level1','m','15'),
(429,'Jennifer','15','level1','m','10'),
(430,'Anthony','15','level4','m','10'),
(431,'Robert','100','level6','f','10'),
(432,'Felicia','46','level5','m','15'),
(433,'Jonathan','100','level5','f','11'),
(434,'Aaron','50','level6','f','12'),
(435,'Francisco','90','level5','m','8'),
(436,'Christopher','60','level6','f','10'),
(437,'Robert','50','level2','f','6'),
(438,'Matthew','90','level5','m','8'),
(439,'Shari','90','level3','f','8'),
(440,'Chad','100','level5','m','12'),
(441,'Evan','46','level3','m','6'),
(442,'Cheryl','80','level1','m','8'),
(443,'Austin','100','level2','f','10'),
(444,'Michelle','100','level5','m','12'),
(445,'Samuel','46','level2','f','11'),
(446,'Cory','90','level4','m','8'),
(447,'Marissa','46','level1','f','6'),
(448,'Adrienne','80','level6','m','10'),
(449,'Jeffrey','15','level5','f','8'),
(450,'Jessica','90','level1','f','12'),
(451,'Brandi','50','level3','f','10'),
(452,'Mark','50','level5','m','10'),
(453,'Jessica','46','level5','f','10'),
(454,'Travis','15','level2','f','8'),
(455,'Jamie','80','level6','f','12'),
(456,'Richard','100','level5','m','11'),
(457,'Jennifer','80','level3','m','8'),
(458,'Robert','60','level4','m','8'),
(459,'David','15','level1','f','15'),
(460,'Jeffrey','15','level6','m','10'),
(461,'Michael','50','level1','m','15'),
(462,'Debbie','60','level2','f','10'),
(463,'Steve','50','level1','f','15'),
(464,'Ashlee','80','level1','f','10'),
(465,'Regina','90','level6','f','10'),
(466,'Stephen','50','level3','f','11'),
(467,'Joseph','46','level5','m','12'),
(468,'Donald','15','level2','m','15'),
(469,'Amber','80','level3','f','11'),
(470,'Robert','80','level2','m','10'),
(471,'Carol','90','level2','f','8'),
(472,'Bill','90','level2','f','12'),
(473,'Michael','50','level6','f','11'),
(474,'Nancy','46','level2','f','6'),
(475,'Megan','46','level4','f','12'),
(476,'Shannon','100','level3','f','12'),
(477,'David','80','level4','f','15'),
(478,'Rachel','80','level3','m','12'),
(479,'Anne','90','level3','f','11'),
(480,'Eric','90','level2','f','6'),
(481,'Jenna','60','level3','f','10'),
(482,'Emily','100','level1','f','12'),
(483,'Jessica','60','level2','f','12'),
(484,'Teresa','15','level3','f','12'),
(485,'Garrett','80','level1','f','11'),
(486,'Jessica','90','level1','f','11'),
(487,'Olivia','90','level1','f','12'),
(488,'Brooke','100','level3','f','11'),
(489,'Amanda','46','level2','f','6'),
(490,'Michelle','60','level2','m','15'),
(491,'Amanda','90','level6','f','8'),
(492,'Johnny','60','level5','f','15'),
(493,'Aaron','80','level1','f','8'),
(494,'Thomas','50','level6','f','11'),
(495,'Rebecca','50','level3','f','10'),
(496,'Kayla','46','level5','f','8'),
(497,'Susan','15','level6','f','11'),
(498,'Teresa','100','level4','m','10'),
(499,'Steven','60','level1','f','11');
select*from student





use student;
create table TopStudents
select * from student
where Average>=90




use student;
create table UnavailableStudents
select * from student
where Average<=60



use student;
select * from student
where Average=100 and Levels='level6'



use student;
select * from student
where levels='level1' and age=15 or age=16 





use student;
select * from student 
where nam like 'A%';







use student;
select * from student 
where nam like '____';







use student;
select avg (average)
from student




use student;
select max(average)
from student



use student;
select min(average)
from student




use student;
select count(levels) from student
where levels='level2' 




use student;
SET SQL_SAFE_UPDATES = 0;
UPDATE student
SET grades = 'male'
WHERE grades = 'm';
select * from student





use student;
SET SQL_SAFE_UPDATES = 0;
UPDATE student
SET grades = 'Female'
WHERE grades = 'f';
select * from student














use student;
SET SQL_SAFE_UPDATES = 0;
UPDATE student
SET Average = '65'
WHERE Average = '60';
select * from student

