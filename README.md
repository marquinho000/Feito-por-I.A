-- Defina as opções do menu
local opcoes = {
    "Pegar só bau comum",
    "Pegar só bau de ouro",
    "Pegar só bau de diamante",
    "Pegar frutas",
    "Subir de level instantaneamente",
    "Sair"
}

-- Função para exibir o menu
local function exibirMenu()
    print("Menu:")
    for i, opcao in ipairs(opcoes) do
        print(i .. ". " .. opcao)
    end
end

-- Função para lidar com a escolha do usuário
local function lidarComEscolha(escolha)
    if escolha == 1 then
        print("Você escolheu pegar só bau comum")
    elseif escolha == 2 then
        print("Você escolheu pegar só bau de ouro")
    elseif escolha == 3 then
        print("Você escolheu pegar só bau de diamante")
    elseif escolha == 4 then
        print("Você escolheu pegar frutas")
        print("Você pegou uma fruta!")
    elseif escolha == 5 then
        print("Você escolheu subir de level instantaneamente")
        print("Seu level agora é 2600!")
    elseif escolha == 6 then
        print("Você escolheu sair")
        return false
    else
        print("Opção inválida")
    end
    return true
end

-- Loop principal do menu
while true do
    exibirMenu()
    print("Digite o número da opção desejada:")
    local escolha = tonumber(io.read())
    if not lidarComEscolha(escolha) then
        break
    end
end
