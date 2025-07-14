-- Aurora Hub | Tabs com Ícones Laterais | Criado por YURIEliteFF7💙
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

local Window = Fluent:CreateWindow({
    Title = "🌌 Aurora Hub",
    SubTitle = "Roube um Brainrot",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 380),
    Acrylic = true,
    Theme = "Amethyst",
    MinimizeKey = Enum.KeyCode.RightControl
})

-- TABS organizadas em tabela com ícones
local Tabs = {
    Main = Window:AddTab({ Title = "Main", Icon = "gamepad-2" }),
    steale = Window:AddTab({ Title = "steale", Icon = "flame" }),
    Player = Window:AddTab({ Title = "Player", Icon = "user" }),
    Note = Window:AddTab({ Title = "Note", Icon = "mail" }),
    security = Window:AddTab({ Title = "security", Icon = "shield" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)

InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)

Fluent:Notify({
        Title = "Bem  video ao 🌌 Aurora Hub",
        Content = "Essa é uma versao gratis do Hub feito por YURIEliteFF7",
        SubContent = "", -- Optional
        Duration = 6 -- Set to nil to make the notification not disappear
})

local Section = Tabs.security:AddSection("Conta security")

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "ANTI BAN", 
    Description = "Nao é sempre eficaz",
    Default = false,
    Callback = function(state)
	if state then
	    print("ANTI BAN On")
	else
	    print("ANTI BAN Off")
        end
    end 
})

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "ANTI KICK", 
    Description = "Nao é sempre eficaz",
    Default = false,
    Callback = function(state)
	if state then
	    print("ANTI KICK On")
	else
	    print("ANTI KICK Off")
        end
    end 
})

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "Hide Executor", 
    Description = "Tenta esconder que você está usando executor de scripts.",
    Default = false,
    Callback = function(state)
	if state then
	    print("toggle On")
	else
	    print("toggle BAN Off")
        end
    end 
})

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "Anti Spectate", 
    Description = "Impede que admins ou jogadores te observem.",
    Default = false,
    Callback = function(state)
	if state then
	    print("toggle On")
	else
	    print("toggle Off")
        end
    end 
})

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "Server Hop Seguro", 
    Description = "Troca de servidor automático se detectar risco (admin, muitos reports etc).",
    Default = false,
    Callback = function(state)
	if state then
	    print("Toggle On")
	else
	    print("Toggle Off")
        end
    end 
})

local Toggle = Tabs.security:AddToggle("Conta security", 
{
    Title = "Spoof Name / Fake Display Name", 
    Description = "Muda seu nome visual para evitar ser identificado facilmente.",
    Default = false,
    Callback = function(state)
	if state then
	    print("Toggle On")
	else
	    print("Toggle Off")
        end
    end 
})

Tabs.Note:AddParagraph({
    Title = "📌 Informações úteis",
    Content = "Algumas funções podem não funcionar em servidores privados.\ Use as funções com moderação para evitar banimentos.\ Scripts testados no executor Swift"
})

Tabs.Note:AddParagraph({
    Title = "⚠️ Avisos de risco",
    Content = "Anti Ban e Anti Kick não são 100% eficazes.\ Funções de TP podem causar lag ou detecção."
})

Tabs.Note:AddParagraph({
    Title = "🤝 Créditos",
    Content = "Aurora Hub criado por YURIEliteFF7 💙.\ Agradecimentos especiais à comunidade Fluent UI"
})

Tabs.Note:AddParagraph({
    Title = "Canal do Youtube.",
    Content = "Canal: https://www.youtube.com/@YURIEliteFF7 "
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "🏃 Super Velocidade",
    Description = "Ativa corrida muito rápida",
    Default = false,
    Callback = function(state)
        if state then
            print("Super Velocidade ON")
        else
            print("Super Velocidade OFF")
        end
    end
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "🚪 Noclip",
    Description = "Permite atravessar paredes e objetos",
    Default = false,
    Callback = function(state)
        if state then
            print("Noclip ON")
        else
            print("Noclip OFF")
        end
    end
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "🦘 Pulo Alto",
    Description = "Permite pular bem mais alto",
    Default = false,
    Callback = function(state)
        if state then
            print("Pulo Alto ON")
        else
            print("Pulo Alto OFF")
        end
    end
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "👻 Invisibilidade",
    Description = "Fica invisível para os outros",
    Default = false,
    Callback = function(state)
        if state then
            print("Invisível ON")
        else
            print("Invisível OFF")
        end
    end
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "💀 God Mode",
    Description = "Fica imortal, não leva dano",
    Default = false,
    Callback = function(state)
        if state then
            print("God Mode ON")
        else
            print("God Mode OFF")
        end
    end
})

local Toggle = Tabs.Player:AddToggle("MyToggle",
{
    Title = "Ragdoll",
    Description = "Nao deixa seu personagem cair.",
    Default = false,
    Callback = function(state)
        if state then
            print("Ragdoll ON")
        else
            print("Ragdoll OFF")
        end
    end
})

local AutoStealToggle = Tabs.steale:AddToggle("AutoStealToggle", {
    Title = "🚀 Roubo Automático",
    Description = "Quando vc tiver com um brainrot na mao ele leva pra sua base voando",
    Default = false,
    Callback = function(state)
        if state then
            print("Auto Steal ON")
        else
            print("Auto Steal OFF")
        end
    end
})

local AutoRebirthToggle = Tabs.steale:AddToggle("AutoRebirthToggle", {
    Title = "💸 Rebirth Automático",
    Description = "Faz renascimento assim que atingir o Requesitos necessário",
    Default = false,
    Callback = function(state)
        if state then
            print("Auto Rebirth ON")
        else
            print("Auto Rebirth OFF")
        end
    end
})

local FarmToggle = Tabs.steale:AddToggle("FarmToggle", {
    Title = "⛏️ Farm AFK",
    Description = "Farm contínuo mesmo sem jogar",
    Default = false,
    Callback = function(state)
        if state then
            print("Farm AFK ON")
        else
            print("Farm AFK OFF")
        end
    end
})

local Toggle = Tabs.steale:AddToggle("Priorizar Brainrot Raro", {
    Title = "🎯 Priorizar Brainrot Raro",
    Description = "Localiza o Brainrot mais raro da sesao tipo Um highlight",
    Default = false,
    Callback = function(state)
        if state then
            print("Priorizar Brainrot Raro ON")
        else
            print("Priorizar Brainrot Raro OFF")
        end
    end
})

local Toggle = Tabs.steale:AddToggle("🔁 Trocar de Server Automático", {
    Title = "🔁 Trocar de Server Automático",
    Description = "Troca pro um serve que quase garantido um bom",
    Default = false,
    Callback = function(state)
        if state then
            print("Trocar de Server Automático AFK ON")
        else
            print("Trocar de Server Automático AFK OFF")
        end
    end
})

Tabs.Main:AddParagraph({
    Title = "🌌 Seja bem vido ao aurora HUB",
    Content = "Criado Por YURIEliteFF7"
})

local Toggle = Tabs.Main:AddToggle("Limpar Lags / Resetar Gráficos", {
    Title = "🧹 Limpar Lags / Resetar Gráficos",
    Description = "Remove partículas, sons do mapa para evitar lag.",
    Default = false,
    Callback = function(state)
        if state then
            print("Limpar Lags / Resetar Gráficos ON")
        else
            print("Limpar Lags / Resetar Gráficos OFF")
        end
    end
})

local Toggle = Tabs.Main:AddToggle("⚡ Boost de Performance", {
    Title = "⚡ Boost de Performance",
    Description = "Desativa sombras, texturas e outras coisas pra deixar o jogo leve.",
    Default = false,
    Callback = function(state)
        if state then
            print("Boost de Performance ON")
        else
            print("Boost de Performance OFF")
        end
    end
})

local Toggle = Tabs.Main:AddToggle("🔁 Recarregar Script", {
    Title = "🔁 Recarregar Script",
    Description = "Reinicia o hub e carrega tudo de novo sem reentrar no jogo.",
    Default = false,
    Callback = function(state)
        if state then
            print("Recarregar Script ON")
        else
            print("Recarregar Script OFF")
        end
    end
})
