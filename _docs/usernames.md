---
title: Usernames
---
A "username" is the filename of the Myfile, seen after the "//" in a Myfile address.

Usernames:
* can have alphanumeric characters (i.e. `[0-9a-zA-Z]`)
* can have parentheses (`( and )`), brackets (`[ and ]`), curly braces (`{ and }`), apostrophes and simple quotes (`' and "`). They do not have to match.
* can have the less-than (`<`) and greater-than (`>`) symbols.
* cannot have emoji. They can be represented in the `xn--...` punycode form.
* can be any (reasonable) length. They must be at least one character, for blank usernames refer to the domain.
* can have the plus +, minus -, ampersand ("and" sign) &, asterisk \*, forward-slashes / (these are not used for navigation past the // in the path), tildes ~, underscores (underlines) _, periods ., commas ,, question marks ?, and exclamation points !.
* cannot have backslashes (\\). This is to allow them to escape curly braces that may be in the address.
* cannot have two successive forward-slashes, such as `//`. This is used to separate the path from the username.

<!--To test it, see this:
<input pattern="[0-9a-zA-Z-+&\/\\_\*@$%^`~ \[\]\{\}\!]+" class="myfile-username-test">
<style>
.myfile-username-test {color: white}
.myfile-username-test:invalid[!value] {
    border-bottom-color: white
}
.myfile-username-test:invalid {
    border-bottom-color: red
}
.myfile-username-test:valid {
    border-bottom-color: green
}
</style>-->