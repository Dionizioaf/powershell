# powershell

## Filtrar membros de um grupo noAD

Get-ADGroupMember -Identity 'Usuários Oracle Cloud' -Recursive | select-object  samaccountname > usuarios.txt

## Listar todos os usuários filtrando se estão ativos ou não

Get-ADUser -Filter * -Property Enabled | Where-Object {$_.Enabled -like “true”} | Export-Csv -Path C:\Users\dionizio.ferreira\Desktop\eport.csv -Encoding ascii -NoTypeInformation
