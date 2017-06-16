# One-Liners

A collection of one-line scripts in various languages that do various things. Mostly for my own reference.

### Ubuntu banner grab/remote port test
```
cat < /dev/tcp/<destip>/<port>
```

### Powershell get a user's email address from AD
```
Get-ADUser <samaccountname> -Properties mail | Select-Object -ExpandProperty mail
```

### Powershell list groups a user belongs to
```
Get-ADPrincipalGroupMembership <samaccountname> | select name
```

### Powershell quick DNS reverse lookup
```
[System.Net.Dns]::GetHostEntry("<hostname>").IPAddressToString
```

### Dig my WAN IP
```
dig +short myip.opendns.com @resolver1.opendns.com
```

### Nslookup my WAN IP
```
nslookup myip.opendns.com. resolver1.opendns.com

```
