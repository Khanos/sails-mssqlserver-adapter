![sails logo](https://sailsjs.com/images/hero_squid.png)

# Sails-MSsqlserver



Microsoft SQL Server adapter for [sails.js](http://sailsjs.org/) intended for Sails v1.0.x

## Getting Started
### 1. Install
```sh
$ npm install sails-mssqlserver --save
```

### 2. Configure

#### `config/datastores.js`
```js
{
  default: {
    adapter: 'sails-mssqlserver-adapter',
    user: 'some@user',
    password: 'some@ssword',
    host: 'abc123.database.windows.net',
    port: '1433',
    database: 'mymsdb',
    options: {
      encrypt: true
    }
  }
}
```

## Query Examples

### Select with certain columns
``` javascript
Plugins.find({
  select: ['name','author'] // Optional
})
.where({
  framework: 'sails.js'
})
.then(function(results){
  if (results) {
    results.forEach(function(plugin)){
      console.log(plugin)
    }      
  } else {
    console.log('No plugins found')
 }
})
```

For further examples check out Sail's [Waterline ORM page](http://sailsjs.org/documentation/concepts/models-and-orm/query-language)

## License
MIT

## Credits

This project is a fork from [misterGF/sails-mssqlserver](https://github.com/misterGF/sails-mssqlserver). The code is also available under the MIT license.

[npm-image]: https://img.shields.io/npm/v/sails-mssqlserver.svg?style=flat-square
[npm-url]: https://npmjs.org/package/sails-mssqlserver-adapter
