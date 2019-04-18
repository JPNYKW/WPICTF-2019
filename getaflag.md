WPICTF web / getaflag / 150pt

# How 2 solve this.

**1.** Open Dev tool in top page (login form)

**2.** Find a comment encoded by base64 in html.

```html
<!-- SGV5IEdvdXRoYW0sIGRvbid0IGZvcmdldCB0byBibG9jayAvYXV0aC5waHAgYWZ0ZXIgeW91IHVwbG9hZCB0aGlzIGNoYWxsZW5nZSA7KQ== -->
```

**3.** Decode that. n read that sentence.

```
Hey Goutham, don't forget to block /auth.php after you upload this challenge ;)
```

That sentence is message for developer who is made that website.  
We can understand it has a hint or answer of the flag.

**4.** Access `/auth.php`.

There is the php source code.  

```php
// Pseudocode
$passcode = '???';
$flag = '????'

extract($_GET);
if (($input is detected)) {
  if ($input === get_contents($passcode)) {
    return $flag
  } else {
    echo "Invalid ... Please try again!"
  }
}
```

**5.** Watch out this line.

```php
extract($_GET)
```

This is the point of exploit.  
This method will be generate an array from primitive parameters.  
But, if the name was already taken on scope, that value will be override.  
Cuz, u can override passcode. n `$_GET` was input from URL parameters.

**6.** Access top page. do use parameters.

```
input=&passcode=
``` 

**7.** Displayed successful login.

N, it'll show a link button written "get a flag".  
But, that is a dummy. (If u click, jump 2 [YouTube](https://www.youtube.com/watch?v=dQw4w9WgXcQ))  
So, u must open Dev tool. open console. U can get a flag!

**8.** Get the flag.

```
WPI{1_l0v3_PHP}
```

Enter that 2 form.

# Done

**U G07 150 p7;**

![image](https://github.com/JPNYKW/WPICTF/blob/master/img/getaflag.png)
