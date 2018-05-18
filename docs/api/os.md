# os

> `os` module has system functions related to operating system of the current user.

## `os.runCommand(string command, function success(data), function error)`

### Parameters

#### *string command*

command you want to execute 

#### *function success(data)*

function that will be fired when connection is successful with Neutralino server. `data` is json content that has content as per below.

```js
{
  "success" : "Command successfully executed",
  "stdout" : "<Output of command>"
}
```

### Example

```js
Neutralino.os.runCommand('help', 
  (data) => {
    console.log(data);
  },
  () => {
    console.error('error');
  }
);
```
