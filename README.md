### argv
---
https://github.com/codenothing/argv

```
npm install argv
```

```js
var argv = require( 'argv' );
var args = argv.option( options ).run();
-> { target: [], options: {} }

argv.run();
argv.run([ '--option=123', '-o', '123' ]);
argv.optin({
  name: 'option',
  short: 'o',
  type: 'string',
  description: 'Defines an option for your script',
  example: "'script --option=value' or 'script -o value'"
});

argv.mod({
  mod: 'module',
  description: 'Description of what the module is used for',
  options: [ list of options ]
});

argv.option({
  {
    name: 'option',
    type: 'csv, int'
  },
  {
    name: 'path',
    short: 'p',
    type: 'list, path'
  }
});
$ script --option=123,456.001,789.01
-> option: [ 123, 456 789 ]
$ script -p /path/to/file1 -p /path/to/file2
-> option: [ '/path/to/file1', '/path/to/file2' ]

argv.type( 'squared', function( value ){
  value = parseFloat( value );
  return value * value;
});
argv.option({
  name: 'square',
  short: 's',
  type: 'squared'
});
$script -s 2
-> 4

argv.ersion( 'v1.0' );

argv.info( 'Special script info' );
argv.clear().option( [new options] );
argv.help();
```

```
```


