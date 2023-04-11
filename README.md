# Regex-Tutorial
In this tutorial, we will be discussing regular expressions (regex) and their purpose in finding patterns in text. Regex is a powerful tool for extracting information from large amounts of data. We will be using the example of validating an email address using regex. The regex format for validating an email address is shown as follows:

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

Although it may look like a collection of special characters and numbers enclosed in slashes, we will break it down step-by-step to understand its components and how they work.

The pattern must be in / slash charcters. This is the starting and ending of a regex. Whatever is inside the / / is what you are searching for.

In this tutorial, we will be discussing quantifiers in regular expressions (regex) and their purpose in setting limits on the number of characters that match a pattern. There are several types of quantifiers, including '*', '+', '?', and '{}'. In this tutorial, we will only be covering the curly brackets '{}' quantifier.

Curly brackets provide multiple ways to set limits on the number of characters in a pattern. They can be used in different ways:

{n}: Matches exactly 'n' occurrences of the preceding character or group.
{n,}: Matches at least 'n' occurrences of the preceding character or group.
{a, b}: Matches a minimum of 'a' and a maximum of 'b' occurrences of the preceding character or group.
In the email expression example, '.([a-z.]{2,6})$', the curly brackets '{2,6}' are used within parentheses, which means they only affect the characters within the parentheses. It sets the minimum and maximum limit for the number of characters allowed after the dot (.) character in the email pattern.

This understanding of quantifiers and curly brackets will help us better grasp how to define and set limits on patterns in regular expressions.

In this tutorial, we are discussing the use of anchors in regular expressions (regex). The '^' anchor indicates that the following pattern must appear at the beginning of the string. In the email expression example, '([a-z0-9_.-]+)' is shown followed by the '^' anchor.

This indicates that the input value must start with any characters between 'a' and 'z', followed by any numbers between '0' and '9', as well as underscore, dot, or hyphen characters.

Moving on to the ending anchor '$', the expression '.([a-z.]{2,6})$' verifies the exact string at the end of the email. The 'a-z' indicates any characters between 'a' and 'z', and '{2,6}' is a quantifier indicating that the length of the characters must be between 2 to 6 characters.

Understanding the usage of anchors and quantifiers in regular expressions allows us to define specific patterns and constraints for matching strings, such as in email validation.

In this tutorial, we are discussing the OR operator in regular expressions (regex). The OR operator is denoted by the vertical bar '|' and allows for multiple characters or patterns to match. For example, 'a|b|c' means that the matching character could be 'a', 'b', or 'c'.

However, in our email expression example, there is no OR operator used. But it's important to note that the OR operator can be used to further refine and limit matches to specific patterns. For instance, we could modify our expression to match only '.com' or '.org' email domains by using the OR operator.

Understanding the usage of the OR operator in regular expressions provides flexibility in defining patterns and allows for more precise matching based on specific requirements or constraints.

In this tutorial, we are discussing character classes in regular expressions (regex). Character classes are sets of characters that can fulfill a match in a regex pattern, serving as a shortcut for defining patterns. Some common character classes include:

'.' : Matches any character except for new line characters (\n).
'\d' : Matches any Arabic numeral digits, equivalent to the bracket expression [0-9].
'\w' : Matches any alphanumeric characters from basic Latin alphabets, including underscore (). The bracket expression equivalent is [A-Za-z0-9].
'\s' : Matches any single whitespace character, including tab spaces and line breaks.
One interesting feature of character classes is that when they are written in capitalized letters, such as '\D' or '\W', they inverse the matches. This means the regex pattern will be looking for the opposite factor of the character class.

Understanding the usage of character classes in regular expressions allows for efficient and concise pattern matching based on predefined sets of characters.

In regular expressions (regex), flags are optional components that can be placed after a regex expression to further restrict or modify the search behavior. Some common examples of flags include:

'g': Global search, which tests against all possible matches in the string.
'i': Case-insensitive search, which ignores case sensitivity while testing for a match.
'm': Multi-line search, where the input string is treated as multi-lines.
These flags are commonly used in situations where the search needs to be applied to a large pool of information, such as a document or a string with multiple lines. In the case of our email expression example, flags are not used, as the expression itself is self-contained and does not require any additional search behavior modifications.

Understanding the usage of flags in regex allows for more precise and flexible pattern matching based on specific requirements or constraints in a given scenario.

In regular expressions (regex), brackets '[]' represent a character range, indicating the range of characters or numbers that can be matched. For example, in the expression [a-z0-9_.-], the characters inside the brackets define the range of characters to be matched.

Breaking it down, the expression [a-z] matches any lowercase alphabetic character from 'a' to 'z', [0-9] matches any numerical digit from '0' to '9', and [.-] matches either an underscore '', a dot '.', or a hyphen '-'.

These character ranges can be used in any order desired, allowing for flexible and customizable pattern matching in regex. Understanding how to use brackets to define character ranges allows for precise matching of specific characters or numbers in a given input string.

In regular expressions (regex), grouping and capturing are used to focus on specific portions of an expression. In the email expression /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/, we can observe that there are three separate groups, each enclosed within parentheses '()'.

These groups are:

([a-z0-9_.-]+) - This group captures one or more occurrences of lowercase letters, numbers, underscores, dots, or hyphens before the '@' symbol, representing the username part of the email address.
([\da-z.-]+) - This group captures one or more occurrences of digits, lowercase letters, dots, or hyphens after the '@' symbol, representing the domain name part of the email address.
([a-z.]{2,6}) - This group captures a sequence of 2 to 6 lowercase letters or dots after the last dot in the email address, representing the top-level domain (TLD) part of the email address (e.g., com, org, etc.).
Using grouping and capturing allows us to simplify the expression into three separate parts, making it easier to extract specific information from the email address, such as the username, domain name, and TLD, for further processing or validation.

