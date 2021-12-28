Regex rule

1. When I use Regex, I have to use Forward slash.
 ex: / <!--something write here--> /  

2. After second forward slash, I can added instructions like grobal or case insentives

ex: / <!--something write here--> / gi

3. If I use square brackets, I can add same meaning to inside of square brackets letters.

ex: / gr[ae]y / 
The regex accept gray or grey.

4. If I use square brackets with Carat, it means it will match everything except inside of square brackets letters.

ex: / [^p]000/
It accepts except p000. 
(a000 or b000 or c000..., all accept)

5. If I use Hyphen, I can use range expression.

ex: / [a-z] /
It is the same meaning as [abcdefghigklmnopqrstuvwxyz]

6. If I use Opening and Closing bracket, I can set exact amount of times to repeat.

ex: / [0-9]{11}/ 
It is the same meaning as 
/[0-9][0-9][0-9][0-9][0-9][0-9][0-9][0-9][0-9][0-9][0-9]/

So, the regex accepts the number of 11 length like 01234567890 or 12345678901.

7. 7 is advanced of 6. 
I can set second number in the Opening and Closing bracket.

ex: / [a-z]{1,5}/ 
The regex accepts five strings of a to z like "hello" or "ninja" ...

8. Regex has some Metacharacters.(Of course, Metacharacters set in the Forward slash 
/ <!--Metacharacters here-->/)

ex:
\d : same as [0-9]
\w : match any word char(a-z, A-Z, 0-9, _(underscore))
\s : match a white space
\t : match a tab character only

9. Regex has some special characters.

ex:
'?': accept character zero time or one time
ex: /hello?/ 
It accepts "hell" or "hello"
ex2:/he?llo?/
It accepts "hll" or "hllo" or "hell" or "hello"

'.': accept every character
ex: /car./
It accepts "car@" or "cas" or "car5" or etc.etc.

10. If I would like to use special characters for just special characters, I have to use special characters with back slash.

ex: /abc\*/ === abc*
ex2: /abc\./ === abc.

11. If I start to carot and end to doller sign in regex, I can decide to length of string.

ex: /^hello$/
It is allowed only word of "hello". It is not allowed word of "helloooooo" or "hell1234". Because, it is more than 5 length.(If it start with hello.)

12. In Regex, I can use Vertical bar. It means "or"
ex: /(hello|human) world/
It accepts "hello world" or "human world".
ex2: /(hello|human)? world/
If I use with question mark, it accepts "hello world" or "human world" or " world".

13. In Javascript world, there are two ways to use Regex

ex1: const reg = /[a-z]/gi;
ex2: const reg2 = new RegExp(/[a-z]/, "gi");