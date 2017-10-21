# One-Liners

A collection of one-line scripts in various languages that do various things. Mostly for my own reference.

# BASH 
### banner grab/remote port test
`cat < /dev/tcp/<destip>/<port>`

### Dig my WAN IP
`dig +short myip.opendns.com @resolver1.opendns.com`

### Nslookup my WAN IP
`nslookup myip.opendns.com. resolver1.opendns.com`

# Powershell 
### get a user's email address from AD
`Get-ADUser <samaccountname> -Properties mail | Select-Object -ExpandProperty mail`

### list groups a user belongs to
`Get-ADPrincipalGroupMembership <samaccountname> | select name`

### quick DNS reverse lookup
`[System.Net.Dns]::GetHostEntry("<hostname>").IPAddressToString`

### find AD users who might be...interesting (from killswitch-GUI/PenTesting-Scripts)
Search an account's description

```
powershell Get-NetUser -Filter "(description=*keyword*)" | Select-Object -Prop samaccountname.description,title
```

Search by title (Administrator? Director? CEO? Yes, please.)

`powershell Get-NetUser -Filter "(title=*keyword*)" | Select-Object -Prop samaccountname.description,title`
