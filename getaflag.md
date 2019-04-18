WPICTF web / getaflag / 150pt

# How 2 solve this.

1. Open Dev tool in top page (login 4m)

2. Find a comment encoded by base64 in html.

3. Decode that. n, read that sentence.

4. Access `/auth.php`.

There is the source code.

5. Watch out this line.

```php
extract($_GET)
```

6. This is the point of exploit.

This method will be generate an array from primitive parameters.  
But, if the name was already taken on scope, that value will be override.  
Cuz, u can override passcode. n `$_GET` was input from URL parameters.

7. Access top page. do use parameters.

```
passcode=&input=
``` 

8. Displayed successful login.

N, it'll show a link button written "get a flag".  
But, that is a dummy. (If u click, jump 2 YouTube)  
So, u must open Dev tool. open console. U can get a flag!

9. Enter that copied 2 4m.

10. U get the flag.

# Done

**U G07 150 p7;**

![image](https://github.com/JPNYKW/WPICTF/blob/master/img/getaflag.png)
