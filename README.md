# powershell

## Filtrar membros de um grupo noAD

Get-ADGroupMember -Identity 'Usuários Oracle Cloud' -Recursive | select-object  samaccountname > usuarios.txt
