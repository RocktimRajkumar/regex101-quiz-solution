#  [regex101 quiz](https://regex101.com/quiz)
If you find better and short solution pls let me know.

## My Solution

 1. Check if a string contains the word `word` in it (case insensitive). If you have no idea, I guess you could try `/word/`.
		
	**Regular Expression**
	> \bword\b
2. Use substitution to replace every occurrence of the word `i` with the word `I` (uppercase, I as in me). E.g.: `i'm replacing it. am i not?` -> `I'm replacing it. am I not?`. A regex match is replaced with the text in the `Substitution` field when using substitution.
	
   **Regular Expression**
	> \bi\b
	
	**Substitution**
	> Blockquote

	

3. With regex you can _count_ the number of matches. Can you make it return the number of uppercase consonants (B,C,D,F,..,X,Y,Z) in a given string? E.g.: it should return `3` with the text `ABcDeFO!`. **Note:** Only ASCII. We consider `Y` to be a consonant! **Example:** the regex `/./g` will return **3** when run against the string `abc`.
	
   **Regular Expression**
	> [^AEIOUa-z_\W\d]
	
4. Count the number of integers in a given string. Integers are, for example: `1, 2, 65, 2579`, etc.
	
   **Regular Expression**
	> \	d+

5. Find all occurrences of **4 or more** whitespace characters in a row throughout the string.
   **Regular Expression**
	> \s{4,}
6. Oh no! It seems my friends spilled beer all over my keyboard last night and my keys are super sticky now. Some of the time whennn I press a key, I get two duplicates. Can you ppplease help me fix thhhis?
	
   **Regular Expression**
	> (.)\1{2}
	
	**Substitution**
	> $1
7. Validate an IPv4 address. The addresses are four numbered separated by three dots, and can only have a maximum value of 255 in either octet. Start by trying to validate `172.16.254.1`.
	
   **Regular Expression**
	> ^(?:(?:25[0-5]|2[0-4][0-9]|1[0-9][0-9]|[1-9][0-9]|[0-9])(?:\.(?!$)|$)){4}$
8. Strip all HTML tags from a string. HTML tags are enclosed in `<` and `>`. The regex will be applied on a line-by-line basis, meaning partial tags will need to be handled by the regex. Don't worry about opening or closing tags; we just want to get rid of them all. **Note:** This task is meant to be a learning exercise, and not necessarily the best way to parse HTML.
	
   **Regular Expression**
	> <?[^<>]*>|<[^<>]*>?
	
	**Substitution**
	>  
