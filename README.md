-- Carregar a Redz UI Library
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/main/Redzhubui"))()

-- Criar a janela
local Window = library:MakeWindow({
    Title = "StarHub",
    SubTitle = "Visual Trolls | by Star",
    SaveFolder = "StarHubData"
})

-- Criar a aba de trollagens
local Tab = Window:MakeTab({
    Name = "Troll Visual",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

-- Função para marcar objetos criados pelo hub
local function marcar(obj)
    obj.Name = "StarHubItem"
end

-- **Grupo 1: Efeitos Visuais Aleatórios**
-- Botão 1 a 10
for i = 1, 10 do
    Tab:AddButton({
        Name = "Efeito Visual " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(5, 1, 5)
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-10,10), 10, math.random(-10,10))
            part.Anchored = false
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.Neon
            marcar(part)
        end
    })
end

-- **Grupo 2: Partículas e Movimentos**
-- Botão 11 a 30
for i = 11, 30 do
    Tab:AddButton({
        Name = "Partícula " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(3, 3, 3)
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-15,15), 10, math.random(-15,15))
            part.Anchored = false
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.SmoothPlastic
            local bodyVelocity = Instance.new("BodyVelocity", part)
            bodyVelocity.MaxForce = Vector3.new(10000, 10000, 10000)
            bodyVelocity.Velocity = Vector3.new(math.random(-5,5), 50, math.random(-5,5))
            marcar(part)
        end
    })
end

-- **Grupo 3: Construções Aleatórias**
-- Botão 31 a 50
for i = 31, 50 do
    Tab:AddButton({
        Name = "Construção Aleatória " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(math.random(5,10), 1, math.random(5,10))
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-15,15), 20, math.random(-15,15))
            part.Anchored = true
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.Metal
            marcar(part)
        end
    })
end

-- **Grupo 4: Objetos Flutuantes**
-- Botão 51 a 70
for i = 51, 70 do
    Tab:AddButton({
        Name = "Objeto Flutuante " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(3, 3, 3)
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-10,10), 20, math.random(-10,10))
            part.Anchored = true
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.SmoothPlastic
            local bodyGyro = Instance.new("BodyGyro", part)
            bodyGyro.MaxTorque = Vector3.new(100000, 100000, 100000)
            bodyGyro.CFrame = CFrame.Angles(math.random(), math.random(), math.random())
            marcar(part)
        end
    })
end

-- **Grupo 5: Trollagens com Sons**
-- Botão 71 a 90
for i = 71, 90 do
    Tab:AddButton({
        Name = "Trollagem Sonora " .. i,
        Callback = function()
            local sound = Instance.new("Sound", workspace)
            sound.SoundId = "rbxassetid://1836819" -- Som aleatório
            sound.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
            sound:Play()
            marcar(sound)
        end
    })
end

-- **Grupo 6: Efeitos Interativos com o Mundo**
-- Botão 91 a 110
for i = 91, 110 do
    Tab:AddButton({
        Name = "Efeito Interativo " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(math.random(5,10), math.random(5,10), math.random(5,10))
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-10,10), 20, math.random(-10,10))
            part.Anchored = false
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.ForceField
            local bodyVelocity = Instance.new("BodyVelocity", part)
            bodyVelocity.MaxForce = Vector3.new(10000, 10000, 10000)
            bodyVelocity.Velocity = Vector3.new(math.random(-5,5), 50, math.random(-5,5))
            marcar(part)
        end
    })
end

-- **Grupo 7: Mais Trollagens Visuais**
-- Botão 111 a 130
for i = 111, 130 do
    Tab:AddButton({
        Name = "Trollagem Visual " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(math.random(2, 5), math.random(1, 3), math.random(2, 5))
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-10,10), 20, math.random(-10,10))
            part.Anchored = false
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.SmoothPlastic
            part.Transparency = math.random(0, 1)
            marcar(part)
        end
    })
end

-- **Grupo 8: Objetos Flutuantes Interativos**
-- Botão 131 a 150
for i = 131, 150 do
    Tab:AddButton({
        Name = "Objeto Flutuante Interativo " .. i,
        Callback = function()
            local part = Instance.new("Part", workspace)
            part.Size = Vector3.new(3, 3, 3)
            part.Position = game.Players.LocalPlayer.Character.HumanoidRootPart.Position + Vector3.new(math.random(-10,10), 20, math.random(-10,10))
            part.Anchored = true
            part.BrickColor = BrickColor.Random()
            part.Material = Enum.Material.Neon
            local bodyGyro = Instance.new("BodyGyro", part)
            bodyGyro.MaxTorque = Vector3.new(100000, 100000, 100000)
            bodyGyro.CFrame = CFrame.Angles(math.random(), math.random(), math.random())
            part.Touched:Connect(function(hit)
                if hit.Parent:FindFirstChild("Humanoid") then
                    hit.Parent:BreakJoints()
                end
            end)
            marcar(part)
        end
    })
end

-- **Efeito Final: Limpar Todos**
Tab:AddButton({
    Name = "Limpar Tudo do StarHub",
    Callback = function()
        for _, obj in ipairs(workspace:GetChildren()) do
            if obj.Name == "StarHubItem" then
                obj:Destroy()
            end
        end
    end
})
