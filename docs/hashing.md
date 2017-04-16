# Hashing

Using R’s [`digest`](https://cran.r-project.org/web/packages/digest/index.html) package to generate a [cryptographic hash](http://en.wikipedia.org/wiki/Cryptographic_hash_function) for a piece of text or a file is fairly simple.  The only trick is to remember to set `serialize` to `FALSE`

To hash a [reference text](http://en.wikipedia.org/wiki/SHA-1#Example_hashes):

```
library(digest)

digest("The quick brown fox jumps over the lazy dog", algo = "sha1", serialize = FALSE)
```

To check the integrity of a file:

```
digest("R-3.3.3.pkg", algo = "md5", serialize = FALSE, file = TRUE)
```

The default behavior of digest is to serialize the input, which generally should be turned off in order to compare the outputted digest with a known reference.
