[link](https://www.reddit.com/r/dailyprogrammer/comments/cmd1hb/20190805_challenge_380_easy_smooshed_morse_code_1/)

## Easy

For the purpose of this challenge, Morse code represents every letter as a sequence of 1-4 characters, each of which is either . (dot) or - (dash). The code for the letter a is .-, for b is -..., etc. The codes for each letter a through z are:

```
.- -... -.-. -.. . ..-. --. .... .. .--- -.- .-.. -- -. --- .--. --.- .-. ... - ..- ...- .-- -..- -.-- --..

```

Normally, you would indicate where one letter ends and the next begins, for instance with a space between the letters' codes, but for this challenge, just smoosh all the coded letters together into a single string consisting of only dashes and dots.

### Examples

```

smorse("sos") => "...---..."
smorse("daily") => "-...-...-..-.--"
smorse("programmer") => ".--..-.-----..-..-----..-."
smorse("bits") => "-.....-..."
smorse("three") => "-.....-..."

```

An obvious problem with this system is that decoding is ambiguous. For instance, both bits and three encode to the same string, so you can't tell which one you would decode to without more information.

### Optional bonus challenges

For these challenges, use the enable1 word list. It contains 172,823 words. If you encode them all, you would get a total of 2,499,157 dots and 1,565,081 dashes.

- The sequence -...-....-.--. is the code for four different words (needing, nervate, niding, tiling). Find the only sequence that's the code for 13 different words.

-  autotomous encodes to .-..--------------..-..., which has 14 dashes in a row. Find the only word that has 15 dashes in a row.

- Call a word perfectly balanced if its code has the same number of dots as dashes. counterdemonstrations is one of two 21-letter words that's perfectly balanced. Find the other one.

- protectorate is 12 letters long and encodes to .--..-.----.-.-.----.-..--., which is a palindrome (i.e. the string is the same when reversed). Find the only 13-letter word that encodes to a palindrome.

- `--.---.---.--` is one of five 13-character sequences that does not appear in the encoding of any word. Find the other four.

## Hard

Smooshed Morse code means Morse code with the spaces between encoded letters left out. See this week's Easy challenge for more detail. We'll also be stripping all punctuation, capitalization, and spacing, so the only encoded characters are the letters a-z.

Your challenge today is to decode smooshed Morse code representations of English text. As I said in the Easy challenge, the decoding is ambiguous. You're not expected to do a perfect job, but the more your output resembles English, the better you're doing. You are not expected to reproduce the punctuation, just the spacing between words.

A standard approach involves training on a corpus of English text. Last time I posted a similar challenge, u/dreugeworst got excellent results this way. You can use any training data sources you want, but your program must run autonomously on the input, without human intervention.

The challenge inputs this time are all English-language movie quotes, some of which involve proper names, contractions (without the apostrophe), or other words you might not find in a standard word list.

(I have no idea how difficult this is, so I'll be happy to provide challenge inputs that are easier/harder/shorter/longer/whatever.)
Example input
```
-.---..--.....--.--..-..-.--....--.--..-.--.-.....--.-......-....-......-...-.-......-.--.--.--
```
Example output
```
no im simply saying that life uh finds a way
```
### Challenge inputs

Input 1

```
......---.--..--...-....-..-----.....-..-.--.-.-.-..-.--.-....-.-.-.....--..-..-...-.--.-...--..--.----.-.--..--...-.-.-.....--.--.....----.-.....-.-..----..-.-.-..-....--...-........-.---.-.....-..-.-.-.---.--.--...-....-...----....----.---.-..-..--...-...-..-.-.-..----.
```

Input 2 (contains proper names)

```
...--.--.-----.......---.---.-----..-...-----.-......-.--.....----.--.-.-..-..---......-...--.-...-..-------.--.-..-..---.....-...-....-....-.-...-.-.....-.--.---...-..-.-.--.-.-....--..-.-....-.--..--....-.---.....-...-..-..----...--.....-.-.-----..--.-..--......-...-.-.-----.---.--..-.-..-......--..-...-.-..----..-..-.---.........----..-.-..--.-....-.-..--.-....-.-..-..--.-.----.-.-.---.-...-...-..-...-.--.---..-...-.-..--....-.....-...-..--...-.---......---.-.--..--...........--...-.-.----.-.-..--.-.----.-.....--....---.-.-.....---.....-.--..--..-.-----.....-..-.-..-.-.-..-.--.--.-.--.-..-...-..-...--....---.-...-..-.-----.---..-.......--........-.....-.-.......---..-......--..-...-...-.-....-...-.-.......
```

Input 3

```
-.-----..-.-..-......-.......-..........------..-..-.-..--.-..-.-....-.---..-..--...--.-....-.-...--.-.-..-...--.-..-.--..----...-.......-..-.------......--..-.-----..-..-----..-.--.---..-.-.....--.--.-...-..--.-----..-.-.-..-.........-.-.-..-.-.-....--.-----..-..--..--.-----.-.-..-.--.--......-.-.....-.......--...-.---.--.....-.-.-...-.....-...-...-.---.-.-..........-...-.-.....-...--..--....-...----..-....--..-..--...-..-.-----.--.....--.....----......-..--.......-.....-.-.------.-.-----..-.--.--.....--.--..-.-..-.-...--..-..-.-........----..--.......-.....-.-..--.-..-.....--.....-.-.-...-..-........-....----..-....-..-.--.-...----..-...-....-.....-.----..--..-..-.--..-.-.-.-...--.-..-......-...-.-----....-.------.-...---..-.....-.-..---..-.-.-.----.-.-.---.-...--......-.-..........-....-...-..-.-----..-..-..-..----.-..--....-..-.--......-..
```



