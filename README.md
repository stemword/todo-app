# todo-app
Todo note app in node js

Clone this repository.
Go to the todo-app folder.

For listing of notes 
node app list

Add Note 
node app add --t=firstnote --b=first note body

Remove note
node app remove --t=firstnote
```
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'root',
  password : 'root',
  database : 'productsdb'
});



const data = new Promise((resolve, reject) => {
	connection.query('SELECT * FROM products', (err, resp) => {
            if (err) {
                reject(err)
            } else {
                const table = [];
                resp.forEach((product) => {
                    obj = {
                    'name ID': product.name,
                    'phone': product.code
                    }
                    table.push(obj)
                })
                resolve(table)
            }
});
});

data.then(value => {
  console.log(value); // Success!
}, reason => {
  console.error(reason); // Error!
});
```
