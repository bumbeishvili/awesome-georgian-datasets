Georgian Parliament Elections 2016 (Proportional System)
========================================================

საქართველოს პარლამენტის არჩევნები 2016 (პროპორციული საარჩევნო სისტემით)
========================================================

Sources: 
* Some data are drained from publically avaliable final results on the website of CEC Elenction Aministration of Georgia http://cesko.ge
* Other data were provided by CEC Elenction Aministration of Georgia upon request in PDF format and were transformed into processing friendly format


geolocations.csv
----------------
Geographical locations of voting stations (საარჩევნო უბანი)
It also contains the number of registered voters for every station.

| Field         |Key            | Type          | Comment           |
| ------------- |---------------|:-------------:| -----------------:|
|District       |*              |int            |District (საარჩევნო ოლქი)     |
|Station        |*              |int.int.int    |Id of a voting station (საარჩევნო უბანი)|
|Lat            |               |decimal(9,6)   |Geographical latitude|
|Long           |               |decimal(9,6)   |geographical longitude|




turnout.csv
-----------
Turnout (გამოცხადება) of voters per district at 12:00, 17:00 and end of voting accordingly. 
District 0 corresponds to some ad-hoc districts (დროებითი საარჩევნო უბანი) 

| Field         |Key            | Type          | Comment           |
| ------------- |---------------|:-------------:| -----------------:|
|District       |*              |int            |District (საარჩევნო ოლქი)     |
|Voters         |               |int            |Number of registered voters|
|Station        |*              |int.int.int    |Id of a voting station (საარჩევნო უბანი)|
|A              |               |int            |Number of voters at 12:00|
|B              |               |int            |Number of voters at 17:00|
|C              |               |int            |Number of voters at the end of voting|

votes.csv
---------
Voutes counted per party.

| Field         |Key            | Type          | Comment           |
| ------------- |---------------|:-------------:| -----------------:|
|District       |*              |int            |District (საარჩევნო ოლქი)     |
|Station        |*              |int.int.int    |Id of a voting station (საარჩევნო უბანი)|
|Note           |               |string         |Some notes from CEC|
|1..N           |               |int            |Number of votes counted per party|

Fileds with numeric names 1..N correspond to long time stable party ids assigned by CEC.

|1..N| Name|
| ------------- |---------------------------------------------------------------|
|2|პროგრესულ - დემოკრატიული მოძრაობა („თქვენგან, თქვენთვის, თქვენთან ერთად!|
|4|ჯონდი ბაღათურია - ქართული დასი|
|6|უსუფაშვილი - რესპუბლიკელები|
|7|თამაზ მეჭიაური ერთიანი საქართველოსთვის|
|9|ახალი პოლიტიკური ცენტრი - გირჩი|
|10|შალვა ნათელაშვილი - საქართველოს ლეიბორისტული პარტია|
|11|სახალხო ხელისუფლება|
|12|საქართველოს კომუნისტური პარტია - სტალინელები” (ივანე წიკლაური)|
|13|ევროპელი დემოკრატები|
|14|დავით თევზაძე - საქართველოს მშვიდობისათვის|
|15|მშრომელთა სოციალისტური პარტია|
|16|საქართველოს ერთიანი კომუნისტური პარტია|
|17|საქართველო|
|18|ქართული იდეა|
|19| - საარჩევნო ბლოკი „თოფაძე-მრეწველები, ჩვენი სამშობლო|
|20|საქართველოს ეროვნული ერთიანობის პარტია|
|21|საქართველოს კონსერვატიული (მონარქისტული) პარტია|
|22|მერაბ კოსტავას საზოგადოება|
|23| - საარჩევნო ბლოკი „ჩვენები - სახალხო პარტია|
|24|გიორგი ლაღიძე - მომავალი საქართველო|
|25|კახა ძაგანია, სოსო შატბერაშვილი, პაატა ჯიბლაძე, არჩილ ბენიძე - მემარცხენე ალიანსი|
|26|ეროვნული ფორუმი|
|27|ირაკლი ალასანია - თავისუფალი დემოკრატები|
|28|ზვიადის გზა - უფლის სახელით|
|29|ეროვნულ - დემოკრატიული პარტია (ედპ)”
|30|ჩვენი საქართველო” (ბადრი პატარკაციშვილის საარჩევნო შტაბი)|

Author: George Mamaladze