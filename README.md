# Bash Symbols & Operators Cheat Sheet

## Navigation
[Basics](#basics) | [Quotes](#quotes-speech-marks) | [Variables & Expansions](#variables--expansions) | [Special Variables](#special-variables) | [Redirections](#redirections) | [Logic & Execution](#logic--execution) | [Grouping & Testing](#grouping--testing) | [Finding Files](#finding-files) | [History](#history-bangs) | [Common Flags](#common-flags) | [Math Operators](#math-operators) |[Operators](#numeric--string-operators) | [String Manipulation](#string-manipulation)

---

## Basics
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `#` | Comment | The computer ignores everything after this symbol. Use it to leave helpful notes |
| `\` | Escape | Tells Bash to treat the next character as normal text, not a command |
| `~` | Tilde (Home) | A quick shortcut to your user's "Home" folder |
| `-` | Dash (Previous) | A shortcut to the folder you were in before your last move |
| `:` | Null Command | Does absolutely nothing, but always reports "Success" |

## Quotes (Speech Marks)
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `' '` | Single Quotes | Strict Mode! Everything inside stays exactly as written. Variables ($) do not work inside |
| `" "` | Double Quotes | Relaxed Mode. Keeps text together, but allows variables ($) to show their actual value |
| `` ` ` `` | Backticks | An old way to run a command inside another command |

https://www.geeksforgeeks.org/linux-unix/bash-script-quotes-and-its-types/

## Variables & Expansions
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `$` | Variable Call | Put this in front of a word to grab the data saved inside that variable |
| `${}` | Safe Variable | Wraps the variable name safely so the computer doesn't get confused |
| `$()` | Command Substitution | Runs the command inside the brackets and pastes the result right there |
| `$(( ))` | Math Mode | Does basic whole-number math |

https://www.geeksforgeeks.org/linux-unix/bash-script-define-bash-variables-and-its-types/

## Special Variables
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `$0` | Script Name | Holds the name of the script you are currently running |
| `$1 to $9` | Arguments | The 1st, 2nd, and 3rd words you typed after the script name |
| `$#` | Argument Count | Tells you exactly how many arguments the user typed |
| `$@` | All Arguments | A list of every single argument the user typed |
| `$?` | Exit Status | Did the last command work? Returns 0 if successful |

https://guide.bash.academy/expansions/

## Redirections
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `>` | Overwrite File | Saves command text into a file. Erases previous content |
| `>>` | Append to File | Adds command text to the bottom of a file |
| `<` | Feed Input | Takes text from a file and feeds it into a command |
| `|` | The Pipe | Takes results of the left command and feeds it into the right command |
| `2>` | Redirect Errors | Saves only error messages into a file |

https://www.reddit.com/r/linux/comments/g3zel7/heres_an_extremely_useful_guide_to_redirection_of/
https://www.gnu.org/software/bash/manual/html_node/Redirections.html

## Logic & Execution
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `;` | Semicolon | Lets you type multiple commands on one line |
| `&` | Background Job | Put at the end of a command to run it in the background |
| `&&` | Logical AND | Runs the second command only if the first was successful |
| `||` | Logical OR | Runs the second command only if the first failed |

https://www.linux.com/training-tutorials/logical-ampersand-bash/

## Grouping & Testing
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `( )` | Subshell | Runs commands inside a temporary "mini-terminal". |
| `[ ]` | Basic Test | Asks a simple question, like "Does this file exist?". |
| `[[ ]]` | Advanced Test | A smarter, more modern version of `[]`. |

https://dev.to/rpalo/bash-brackets-quick-reference-4eh6

## Finding Files (find, ls, cp, rm commands)
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `*` | Wildcard (Anything) | Stands in for "any text". |
| `?` | Wildcard (One Char) | Stands in for exactly one character. |
| `{ , }` | Brace Expansion | Quickly generates lists or combinations. |

https://labex.io/tutorials/linux-linux-wildcard-character-271447

## History Bangs
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `!!` | Repeat Last | Instantly runs the exact same command you just typed. |
| `!$` | Last Word | Grabs the very last word you typed in your previous command. |

https://opensource.com/article/20/6/bash-history-commands
https://www.redhat.com/en/blog/bash-bang-commands

## Common Flags
| Flag | Name | Description |
| :--- | :--- | :--- |
| `-i` | Ignore Case | Ignore the difference between UPPERCASE and lowercase. |
| `-h` | Human / Help | Makes numbers readable (MB/GB) or shows the help manual. |
| `-a` | All | Show everything, including hidden files. |
| `-r` or `-R` | Recursive | Apply action to a folder and everything inside it. |
| `-v` | Verbose | Makes the command talkative. |
| `-f` | Force | Tells the command to just do its job and NOT ask for permission. |
| `--` | End of Flags | Tells the computer: "I am done giving you flags." |

## Math Operators
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `+` | Addition | Adds two numbers together |
| `-` | Subtraction | Subtracts the second number from the first |
| `*` | Multiplication | Multiplies two numbers |
| `/` | Division | Divides the first number by the second |
| `%` | Modulo (Remainder) | Divides two numbers and returns only the remainder |
| `**` | Exponent (Power) | Raises the first number to the power of the second |
| `++` | Increment | Increases the value of a variable by 1 |
| `--` | Decrement | Decreases the value of a variable by 1 |

## Numeric & String Operators
### Numeric Operators
- `-eq` : Equals
- `-ne` : Not equals
- `-gt` : Greater than
- `-ge` : Greater than or equal to
- `-lt` : Less than
- `-le` : Less than or equal to

### String Operators
- `=` or `==` : Equals
- `-z` : Is empty
- `-n` : Is not empty

## String Manipulation
| Symbol | Name | Description |
| :--- | :--- | :--- |
| `${#}` | String Length | Count how many characters are inside a variable. |
| `${/}` | Find and Replace | Replaces the first match of a word. |
| `${//}` | Replace ALL | Replaces every match of a word. |
