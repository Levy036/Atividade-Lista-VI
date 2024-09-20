try {
    $contas = Get-LocalUser
} catch {
    Write-Error "Erro ao recuperar as contas de usuário locais: $_"
    exit
}

Write-Output "Lista de contas de usuário locais:"

foreach ($conta in $contas) {
    Write-Output $conta.Name
}
