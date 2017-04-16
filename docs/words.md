# words (Unix)

[`words`](https://en.wikipedia.org/wiki/Words_(Unix)) is a standard file on most *nix operating systems, including Apple’s Mac OSX. It is a newline delimited list of 234,936 dictionary words from Webster’s Second International edition in 1934. The README file provides additional information.

    The supplemental 'web2a' list contains hyphenated terms as well as assorted noun and adverbial phrases.

```
[/usr/share/dict]$ ls -l
total 2904
-r--r--r--  1 root  wheel     1311 Jul 30  2016 README
-r--r--r--  1 root  wheel      706 Jul 30  2016 connectives
-r--r--r--  1 root  wheel     8546 Jul 30  2016 propernames
-r--r--r--  1 root  wheel  2493109 Jul 30  2016 web2
-r--r--r--  1 root  wheel  1012731 Jul 30  2016 web2a
lrwxr-xr-x  1 root  wheel        4 Oct  1  2016 words@ -> web2
```

To read the `words` data file into R:

```
words <- scan("/usr/share/dict/words", what = character())
```

To find the length of the longest words:

```
max(nchar(words))
```

To find the number of 24 character words:

```
sum(nchar(words) == 24)
```

To find the number of words of length 1 through 24:

```
sapply(1:24, function(len) sum(nchar(words) == len))
```

To randomly pick 3 words that are 9 characters long:

```
sample(words[which(nchar(words) == 9)], 3)
```
