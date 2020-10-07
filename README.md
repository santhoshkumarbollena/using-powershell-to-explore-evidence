# using-powershell-to-explore-evidence

## Team Members
 1. Santhosh kumar Bollena
 1. Kamal Reddy Donthireddy
 1. Isaac Adesope (Cyber Security)
 1. Sneha Ojha
 
## Idea
Assuming there are two users UserA and UserB. UserB will be sharing the public key to the UserA. Now UserA can generate some data to a file and encrypt the data using the public key of the UserB and send the encrypted file to the UserB. Here, UserB can decrypt the data using the Private key of his own.

## Professor Suggestion

“crime” with three of your group members and then show how the forth member (or your viewers) could solve the case if they can get access to a perpetrator’s private key?

## GPG intallation steps

1. Open powershell window as administrator.
1. Copy and paste the following command
 ``` 
 $uri = 'https://raw.githubusercontent.com/adbertram/Random-PowerShell-Work/master/Security/GnuPg.psm1'
$moduleFolderPath = 'C:\Program Files\WindowsPowerShell\Modules\GnuPg'
$null = New-Item -Path $moduleFolderPath -Type Directory
Invoke-WebRequest -Uri $uri -OutFile (Join-Path -Path $moduleFolderPath -ChildPath 'GnuPg.psm1')
```
1. Copy and paste the next command to get command for gnupg:

``` 
Get-Command -Module GnuPg | ft -a 
```

1. To install gpg, use the following command

``` 
Install-GnuPG -DownloadFolderPath 'C:\'
```

1. Try to execute the gpg command.

``` 
gpg 
```

1. If the gpg is not found try to install again with the following command.

``` 
Install-GnuPg

```

1. Try to execute gpg, If the gpg is not found try to close and reopen the powershell then execute the command.

## References

https://4sysops.com/archives/encrypt-and-decrypt-files-with-powershell-and-pgp/
