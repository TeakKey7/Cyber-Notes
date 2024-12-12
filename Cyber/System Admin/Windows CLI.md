# Command Line
## Powershell
Powershell is an object-oriented language. Powershell returns an object for each command which can be piped `|` into a function.
* * *
`Recommended Tools: VS-Code`
* * *
### Helpful Commands
- `Get-Command`
	- Lists all available commands
	- Using `Get-Command -CommandType "Function"` limits results to functions such as math operations
- `Get-Help`
	- Can be used to explain any command
	- `Get-Help Get-Date`
	- Adding `-examples` shows common uses
- `Get-FileHash`
	- Deafults to SHA256. Use `-Algorithm`.
### Windows commands
- `Get-ComputerInfo`
- `Get-LocalUser`
	- Returns a list of all local accounts
- `Get-NetIPConfiguration`
	- DNS, Gateway, Adapter descriptions
- `Get-NetIPAddress`
	- Useful to determine IPv6 schemes
- `Invoke-Command`
	- Uses PSRemoting (WinRM) to execute commands on a remote machine
#### Live commands
- `Get-Process`
	- Similar to Task Manager
- `Get-Service`
- `Get-NetTCPConnection`
### File manipulation
- `New-Item`
	- `New-Item -Path "C:\folder" -ItemType "Directory"`
	- `New-Item -Path "C:\file.txt" -ItemType "File"`
- `Remove-Item -Path`
- `Copy-Item -Path`
- `Get-Content -Path`
	- Similar to cmd's `type` and Unix's `cat`
### Aliases
- Common commands such as `cd` or `dir` are actually aliases to their *Verb-Noun* counterparts; `Set-Location` and `Get-ChildItem` respectively.
- Avoid using aliases in scripts when alternatives are available. VS-Code will warn when alternatives are available.
### Piping
- `Sort-Object`
	- `Get-ChildItem | Sort-Object Length`
		- Sorts the directory by file size
- `Where-Object`
	- `Get-ChildItem | Where-Object -Property "Name" -like "flag*"`
	- Recursively searches an array (or folder) for anything matching. Returns multiple objects
### Operations
- == `-eq`, != `-ne`, > `-gt`, >= `-ge`, < `-lt`, <= `-le`
- `Select-String`
	- Uses `-pattern` to search for Regex
* * *
### Further reading
- Modules
	- Just like any other programming language, Powershell contains libraries called *Modules.* They can be searched using `Find-Module` and installed using `Install-Module`.

## Cmd Commands
* * *

### `Systeminfo`

- Hostname
- OS Version
- IP address + NICS
### `Control`
-	Opens control panel / settings windows
	-	`control /name Microsoft.WindowsUpdate`
### `Tracert`
### `Netstat`

- Active connections
- `netstat -abon`
	- `-a` displays all established connections and listening ports
	- `-b` shows the program associated with each listening port and established connection
	- `-o` reveals the process ID (PID) associated with the connection
	- `-n` uses a numerical form for addresses and port numbers

### File navigation

- `dir`
	- The Windows equivalent of ls
	- /a displays hidden and system files
	- /s displays files in the current directory and subdirectories
		- Use tree instead
- `mkidr` and `rmdir`

### File manipulation

- `type`
	- Windows equivalent of `cat`
- `more`/`less`
	- Pipe long commands into more command | more
- `copy`/`move` 
- `del`/`erase`

### `Tasklist`

- Use filters
	- `tasklist /?`
- `tasklist /FI "imagename eq sshd.exe"`
- `taskkill /PID 1234`
