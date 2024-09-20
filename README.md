try {
    $contas = Get-LocalUser
} catch {
    Write-Error "Erro ao recuperar as contas de usuário locais: $_"
    exit
}

# Exibe uma mensagem indicando que a lista a seguir são os nomes dos usuários
Write-Output "Lista de contas de usuário locais:"

# Exibe o nome de cada conta de usuário
foreach ($conta in $contas) {
    Write-Output $conta.Name
}
