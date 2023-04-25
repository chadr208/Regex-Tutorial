# CSS Regex Tutorial: Validating Hexadecimal Color Codes

Welcome to this tutorial on validating hexadecimal color codes using a regex in CSS. In this tutorial, I will break down the regex pattern for validating hexadecimal color codes and explain what it does.

## Summary
The regex pattern featured in this tutorial is ^#(?:[0-9a-fA-F]{3}){1,2}$. This pattern matches valid 3 or 6 digit hexadecimal color codes, starting with the "#" symbol.

## Table of Contents

- [What is a Regular Expression?](#What-is-a-Regular-Expression-?)
- [Regex pattern breakdown](#Regex-pattern-breakdown)

## Regex Components

### What is a Regular Expression?

A regular expression, or regex, is a sequence of characters that define a search pattern. Regular expressions can be used to match and manipulate text.

### Regex-pattern-breakdown
* '^' The caret symbol ^ at the beginning of the regex pattern matches the start of a string.
* '#' The "#" symbol matches the literal character "#", which is the first character in a valid hexadecimal color code.
* '(?:[0-9a-fA-F]{3})' The non-capturing group '(?:)' matches a group of three characters that can be either numbers or letters from A to F, in either uppercase or lowercase. The '{3}' quantifier means that there must be exactly three of these characters in the group.
* '{1,2}' 
The '{1,2}' quantifier means that the non-capturing group that matches the hexadecimal color code can occur one or two times.
* '$'
 at the end of the regex pattern matches the end of a string.
 
 ## Example
 /^\.([a-zA-Z0-9_-]+)$/

## Example of code in use: 
		function validateClass() {
			const classNameInput = document.getElementById("class-name");
			const className = classNameInput.value;
			const regex = /^\.([a-zA-Z0-9_-]+)$/;
			if (regex.test(className)) {
				document.getElementById("result").className = "valid";
				document.getElementById("result").textContent = "Valid class name!";
			} else {
				document.getElementById("result").className = "invalid";
				document.getElementById("result").textContent = "Invalid class name. Must start with a dot (.) and contain only letters, numbers, underscores, or hyphens.";
			}
		}

## Author

This tutorial was written by Chad Rajcooar, a web development student who is passionate about web development and learning new things. You can find more of my projects on my GitHub profile at https://github.com/chadr208.
