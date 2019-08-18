# react-contacts
contacts  &amp; department select

威发微服务选人组件/Wafer microservice selection component

# react-rotate-menu
React Rotate Menu

[![npm](https://img.shields.io/npm/v/react-contacts.svg?maxAge=2592000?style=plastic)](https://www.npmjs.com/package/react-rotate-menu)
[![NPM downloads](http://img.shields.io/npm/dm/react-conacts.svg?style=flat-plastic)](https://npmjs.org/package/react-rotate-menu)

## Example

![Example](./example.gif)

## How to use

### install

`yarn react-contacts`

### React 

```js
import Contacts from 'react-contacts'

<Contacts {...props}/>

```

Properties  | Description | Type | Default Values
------------- | ------------- | --------------| ------------- 
deptTree  | Department of Tree（[Department Data](###Department Data)） | array | []
users  | User data （[User & Search Result Data](###User & Search Result Data)） | object | { records: []}
loading | Loading status | bool | false
searchResult | Query user data return results （[User & Search Result Data](###User & Search Result Data)） | object | { records: []}
handleSearchUser | Handle search user function | func | function(page,nameKey,depId)
deptSearch | Show department search input | bool | tree
updateSelectUsers | Update user list when select user | func | function(userSelected)
deptCheckBox | Show department checkbox | bool | true


### Department Data

````
[
      {
        id: 1,
        parentId: 0,
        children: [
          {
            id: 3,
            parentId: 1,
            children: [
              {
                id: 4,
                parentId: 3,
                children: [
                  {
                    id: 5,
                    parentId: 4,
                    children: [],
                    name: '院校农信',
                  },
                ],
                name: '高新农信',
              },
            ],
            name: '潍坊农信',
          },
        ],
        name: '山东农信',
      },
  ]
````

### User & Search Result Data

```

 {
      records: [
        {
          userId: 1,
          username: 'admin',
          password: '$2a$10$QOfWxxFyAMmEEmnuw9UI/..1s4B4eF/u9PzE2ZaGO.ij9YfmcUy.u',
          salt: null,
          wxOpenid: 'o_0FT0uyg_H1vVy2H0JpSwlVGhWQ',
          qqOpenid: null,
          createTime: '2018-04-20 07:15:18',
          updateTime: '2019-03-12 16:04:42',
          mail: 'a@a.com',
          delFlag: '0',
          lockFlag: '0',
          phone: '17034642888',
          avatar: 'lengleng-0d2a7b025da14d8d93f595b3fa082d82.jpg',
          deptId: 1,
          tenantId: 1,
          deptName: '真理部',
          roleList: [
            {
              roleId: 1,
              roleName: '管理员',
              roleCode: 'ROLE_ADMIN',
              roleDesc: '管理员',
              dsType: 2,
              dsScope: '2',
              createTime: '2017-10-29 15:45:51',
              updateTime: '2018-12-26 14:09:11',
              delFlag: '0',
            },
          ],
        },
	   ......
      ],
      total: 11,
      size: 10,
      current: 1,
      searchCount: true,
      pages: 1,
    },

```

### Development

````
$ git clone https://github.com/wafersystems/react-contacts.git
$ yarn
$ yarn start

````
