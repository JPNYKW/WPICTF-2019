WPICTF web / getaflag / 150pt

# How 2 solve this.

```
1. Open Dev tool in top page(login form)
2. Find a comment in html encoded by base64.
3. Decode that. N read that sentence.
4. Access 2 auth.php. join letters.
5. Watch out this line

extract($_input)

6. This is attack point.

This method will be expend to array from primitive params. But, seem name was already taken on scope, that value will be override. Cuz, u can override passcode. N, $_input was input from URL parameters.

7. Access URL add next parameters.

passcode=&input= 

8. Displayed successful login. N show a link button written in get a flag. But, that is a dummy. (If u click, jump to YouTube)

So, u need open Dev tool. N open consoletab. U can get a flag!

9. Enter that copied to form. U solved it.

Got 150pts.

```
