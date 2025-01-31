# Operators
## &
Runs commands in the background
## &&
Runs multiple commands in one line
## >
Redirects the output of a command somewhere else
## >>
Appends the output of a command somewhere else
## `2>/dev/null`
Ignores any file permission errors
# Dumb stuff
- `stty sane` fix dumb tty errors after SSH (no backspace or arrows)
	- Also try `export TERM=linux`