--// Certifique-se de que Rayfield está carregado antes de rodar este script

-- Carrega a biblioteca Rayfield
local Rayfield = loadstring(game:HttpGet('https://[Log in to view URL]'))()

-- Cria a janela principal
local Window = Rayfield:CreateWindow({
    Name = "Gravity Hub",
    LoadingTitle = "Gravity Hub - Loading...",
    LoadingSubtitle = "Feito por ChatGPT",
    ConfigurationSaving = {
        Enabled = false
    }
})

-- Cria uma aba
local MainTab = Window:CreateTab("Gravidade", 4483362458)

-- Cria uma seção
local GravitySection = MainTab:CreateSection("Controle de Gravidade")

-- Valor padrão
local currentGravity = workspace.Gravity

-- Slider para ajustar a gravidade
local GravitySlider = MainTab:CreateSlider({
    Name = "Gravidade do Jogador",
    Range = {0, 500}, -- limite mínimo e máximo
    Increment = 5,
    Suffix = "gravidade",
    CurrentValue = currentGravity,
    Flag = "GravityValue",
    Callback = function(Value)
        workspace.Gravity = Value
    end,
})

-- Botão para resetar gravidade
MainTab:CreateButton({
    Name = "Resetar Gravidade",
    Callback = function()
        workspace.Gravity = 196.2 -- valor padrão do Roblox
        Rayfield:Notify({
            Title = "Gravidade Resetada",
            Content = "A gravidade foi restaurada para 196.2",
            Duration = 4,
        })
        GravitySlider:Set(196.2)
    end,
})

print("The Gravity Hub script ran successfully ✅️")

print(":3")

print("by robloxn_944")

print("💫🔥💫")
