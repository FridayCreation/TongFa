### Tong Fa Project Page
This is a page that contains an installation instruction for iOS, Android and Server. If you have any questions, contact us.

### Default users

#####Admin
username: tongfa  
password: 123

#####送貨中心:
username: delivery  
password: 123

#####提貨站
username: pickuper  
password: 123

### iOS Setup Instruction
Before running the project, you have to set up the environment. We are using [Cocopods](http://cocoapods.org) to manage librarys for the iOS app. Open the terminal and input following command:

```
$ sudo gem install cocoapods
```

After installed Cocoapods, go to the project directory and install the librarys that we need.

```
$ cd project_root
$ pod install
```

Then everything is prepared to roll, open the `tongfa.xcwordspace` and build the project.

### Android Setup Instruction


### Server
To make the server execute properly, you have to install the dependencies. 

```
$ npm install
$ npm install -g bower
$ npm install -g sequelize
$ bower install
```

After install, you can start the server by `node server.js` command.

####Datebase setup
	node seed/sync.js && node seed/seed.js

####Rebuild Indexes
	sequelize -m -u # rollback
	sequelize -m

####API explorer
#####獲取目錄, 地點資料
get `/api/v1/metadata`:

	{
	"success": true,
	"doc": {
		"states": [
			{
				"id": 1,
				"name": "到倉"
			},
			{
				"id": 2,
				"name": "發貨"
			},
			{
				"id": 3,
				"name": "到提貨站"
			},
			{
				"id": 4,
				"name": "已提貨"
			}
		],
		"locations": [
			{
				"id": 2,
				"name": "氹仔"
			},
			{
				"id": 1,
				"name": "澳門"
			}
		],
		"categories": [
			{
				"id": 2,
				"name": "家具"
			},
			{
				"id": 1,
				"name": "衣服"
			}
		]
		}
	}

#####登記貨物
post `/api/v1/orders`  
接收參數:  

	{
		'tid': '29gj20g',
		'phone': '+853xxxxxxx',
		'CategoryId': 1,
		'LocationId': 1,
		'remark': 'hello world'
	}

### Support or Contact
Having trouble with setting up? contact info@fridaycreation.com and we’ll help you sort it out.


