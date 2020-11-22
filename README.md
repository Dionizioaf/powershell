# powershell

## Filtrar membros de um grupo noAD

### Alterar %%NOMEGRUPO%%

Get-ADGroupMember -Identity '%%NOMEGRUPO%%' -Recursive | select-object  samaccountname > usuarios.txt

## Listar todos os usuários filtrando se estão ativos ou não

### Alterar %%ATIVO%% = true | false
### Alterar %%CAMINHO%%

Get-ADUser -Filter * -Property Enabled | Where-Object {$_.Enabled -like “%%ATIVO%%”} | Export-Csv -Path C:\%%CAMINHO%%\dados.csv -Encoding ascii -NoTypeInformation
