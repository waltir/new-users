# new-users
### A straightforward and lightweight Node.js module for generating random user data using the [randomuser.me](http://randomuser.me) REST API.



### Install using the node.js package manager npm:
`$ npm install new-users`



## Examples: 
* Demos of the module are located in: [./test](test.js)
* Example JSON output is located in: [./output](output.json)



# Usage
## Require Module and Initialize Client
`var nu = require('new-users');`



## Get User  -  GetUser will return one random user
`nu.getUser(callback)`
```
nu.getUser((data) => {
    console.log(data);
});
```



## Get Users - GetUsers will return multiple users
`nu.getUsers(params, callback)`
```
nu.getUsers({nat: 'us,gb', pass: 'upper,18', gender: 'male', results: 3}, (data) => {
    console.log(data);
});
```



## params {Object} Documentation

* `results` - num - The number of users to return
* `genders` - string - The gender to return `'male', 'female'`
* `nat` - string - The users nationality `US, AU, BR, CA, CH, DE, DK, ES, FI, FR, GB, IE, IR, NO, NL, NZ, TR`
* `pass` - string - Specify password characteristics `length,special,upper,lower,number`



## Testing
Clone the repo and run the `test.js` file using `$ node test`

```
$ git clone git://github.com/waltir/new-users.git
$ cd new-users
$ npm install
$ node test
```