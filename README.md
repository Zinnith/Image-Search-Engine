Step 1 : Create a database on your MySQL Server
Mysql Code: 
Scripts to create the tables necessary for search engines.
Run all these queries on your MySQL Database server.




create table section(serno int, head char(40) primary key,description char(100))

insert into section values(1,'Arts and Humanities','Artists, Literature, Arts'),(2,'Business and Economy','Employment and careers, finance'),(3,'Careers and Employment','Computers, Information technology'),(4,'Computers and Internet','Free stuff, hardware, software'),(5,'Entertainment','Humor, Jokes, Movies and Film'),(6,'Free Stuff','Games and Downloads'),(7,'Health','Disease and symptoms, First aid'),(8,'News and Current Events','Government, Lottery, Radio, Weather'),(9,'Opportunities','Aids, Franchises, Home-based'),(10,'Recreation and Leisure','Fitness, Shopping, Sports, Travel'),(11,'Reference','Religion and Encyclopedia'),(12,'Shopping and Services','Classifieds, Footwear, Gift ideas'),(13,'Science','Biology, Chemistry, Education and employment'),(14,'Wealth Development','Bonds, Collectables, Commodities');

create table categories(serno int primary key,description char(50),section_code int);

insert into categories values(1,'Art History',1),(2,'Artists',1),(3,'Awards',1),(4,'Books',1),(5,'Censorship',1),(6,'Criticism and Theory',1),(7,'Culture and Groups',1),(8,'Design Arts',1),(9,'Education',1),(10,'Employment',1),(11,'Events',1),(12,'Institutes',1),(13,'Literature',1),(14,'Museums and Galleries',1),(15,'News and Media',1),(16,'Performing Arts',1),(17,'Photography',1),(18,'Prints and Paintings',1),(19,'Reference',1);

insert into categories values(20,'Classifieds',2),(21,'Companies',2),(22,'Conventions and Conferences',2),(23,'Education',2),(24,'Electronic Commerce',2),(25,'Employment',2),(26,'Entrepeneurs',2),(27,'Finance',2),(28,'Franchises',2),(29,'Free Stuff',2),(30,'Home Business',2),(31,'International',2),(32,'Investments',2),(33,'Magazine',2),(34,'Mail Order',2),(35,'Marketing',2),(36,'MLM',2),(37,'Network Marketing',2),(38,'Online Malls',2),(39,'Real Estate',2),(40,'Small Business',2),(41,'Product and Services',2);

insert into categories values(42,'Accounting',3),(43,'Arts',3),(44,'Biology',3),(45,'Business',3),(46,'Chemistry',3),(47,'Computers',3),(48,'Cooking',3),(49,'Denisty',3),(50,'Engineering',3),(51,'Health',3),(52,'Information Technology',3),(53,'Management',3),(54,'Mathematics',3),(55,'Medicine',3),(56,'Nursing',3),(57,'Physics',3),(58,'Science',3),(59,'Web Design',3);

insert into categories values(60,'Communications',4),(61,'Companies',4),(62,'Contests and prizes',4),(63,'Discussion Forum',4),(64,'Employment',4),(65,'FAQ',4),(66,'Free Stuff',4),(67,'Games',4),(68,'Hardware',4),(69,'Help Desk',4),(70,'Information and Reviews',4),(71,'Mobile Computing',4),(72,'Networking',4),(73,'Online Gaming',4),(74,'Operating Systems',4),(75,'Security and Encryption',4),(76,'Software',4),(77,'Tech Support',4),(78,'TECH talk',4),(79,'Training and Certification',4),(80,'Utilities',4),(81,'Web Development',4),(82,'World Wide Web',4);

insert into categories values(83,'Actors and Actresses',5),(84,'Bestsellers',5),(85,'Books and Magazines',5),(86,'Comics and Cartoon',5),(87,'Companies',5),(88,'Computer',5),(89,'Employment',5),(90,'Humor, Jokes and Laugh',5),(91,'Movies and Film',5),(92,'Music',5),(93,'Party Games',5),(94,'Music',5),(95,'Party Games',5),(96,'Radio',5),(97,'Reviews',5),(98,'Space',5),(99,'Talk Show',5),(100,'Television',5),(101,'Trivia',5);

insert into categories values(102,'Antivirus',6),(103,'Communication & Email',6),(104,'Compression',6),(105,'Contest',6),(106,'Desktop Themes',6),(107,'Educational',6),(108,'Fragmentation',6),(109,'Game and Downloads',6),(110,'Graphics and Video',6),(111,'Hobbies',6),(112,'Macintosh',6),(113,'Money',6),(114,'Music',6),(115,'Programming',6),(116,'Screen Savers',6),(117,'Simulators',6),(118,'Utilities and Applications',6),(119,'Webs and internet',6);

insert into categories values(120,'Babies and Pregnancy',7),(121,'Children',7),(122,'Dentistry',7),(123,'Diseases and Symptoms',7),(124,'Doctors',7),(125,'Education',7),(126,'Employment',7),(127,'First Aid',7),(128,'Fitness and Weight',7),(129,'Health Care',7),(130,'Insurance',7),(131,'Mail Order',7),(132,'Medicine',7),(133,'Nursing',7),(134,'Nutrition',7),(135,'Pharmacology',7),(136,'Psychiatrist',7),(137,'Women',7);

insert into categories values(138,'Arts and Humanities',8),(139,'Automotive',8),(140,'College and University',8),(141,'Commercial Services',8),(142,'Crime',8),(143,'Employment',8),(144,'Entertainment',8),(145,'Government',8),(146,'Health',8),(147,'Journals and Newspaper',8),(148,'Legal Aid',8),(149,'Lottery',8),(150,'Music',8),(151,'Politics',8),(152,'Radio',8),(153,'Sports',8),(154,'Taxes',8),(155,'Technology',8),(156,'Television',8),(157,'Travel',8),(158,'Weather',8);

insert into categories values(159,'Aids',9),(160,'Franchises',9),(161,'Home based',9),(162,'Internet',9),(163,'Investments',9),(164,'Mail Order',9),(165,'Network Marketing',9),(166,'World Wide Investments',9)

insert into categories values(167,'Amusement and Theme Parks',10),(168,'Cars',10),(169,'Cooking',10),(170,'Dance',10),(171,'Dating',10),(172,'Fitness',10),(173,'Gambling',10),(174,'Games',10),(175,'Home and Garden',10),(176,'Pets',10),(177,'Shopping',10),(178,'Sports',10),(179,'Stamps',10),(180,'Television',10),(181,'Toys',10),(182,'Travel',10),(183,'Wine',10);

insert into categories values(184,'Religion',11),(185,'Biblography',11),(186,'Calender',11),(187,'Dictionaries & Thesauri',11),(188,'Encyclopedia',11),(189,'Health Jourmnals',11),(190,'Maps',11),(191,'Music',11),(192,'Quotations',11),(193,'Research Papers',11),(194,'Time',11);

insert into categories values(195,'Art and Painting',12),(196,'Books and Magazines',12),(197,'Classifieds',12),(198,'Computer',12),(199,'Cooking',12),(200,'Electronics',12),(201,'Fashion and Clothing',12),(202,'Florist',12),(203,'Footwear',12),(204,'Furniture',12),(205,'Gift Ideas',12),(206,'Health',12),(207,'Help Wanted',12),(208,'Insurance',12),(209,'Jewelry',12),(210,'Music',12),(211,'Perfume',12),(212,'Toys',12),(213,'Wedding',12);;

insert into categories values(214,'Aeronautics and Aviation',13),(215,'Agriculture',13),(216,'Astrology',13),(217,'Others',13);

insert into categories values(218,'Bonds',14),(219,'Collectables',14),(220,'Commodities',14),(221,'Currency',14),(222,'Stocks',14),(223,'Tax Free',14)


create table listings (serno int,login char(15) primary key,password char(15),address char(200),city char(30),state char(30),zip char(10),country char(30),telephone char(30),email char(50),url char(100),category int,caption char(100),descp char(200),mailing_list char(1),posted_on datetime)



create table listings(serno int,login char(15) primary key,password char(15) not null,street char(100),city char(30),state char(30),zip char(10),country char(30),telephone char(30),email char(50),url char(100),category int,caption char(100),descp char(200),mailing_list char(1),posted_on datetime)

Step 3 : Run the Quieries 
Step 4 : Compile search.java file and install the servlet on you web server.
To test your search engine key http://localhost:serverport/servlet/search in your browser
