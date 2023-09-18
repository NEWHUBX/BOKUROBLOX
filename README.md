
NpcTp.Name = "NpcTp"
NpcTp.Parent = ScriptsFrame
NpcTp.BackgroundColor3 = Color3.new(0.14902, 0.14902, 0.14902)
NpcTp.Position = UDim2.new(0.0476484038, 0, 0.224251434, 0)
NpcTp.Size = UDim2.new(0, 100, 0, 31)
NpcTp.Font = Enum.Font.SourceSansLight
NpcTp.Text = "TpNpc"
NpcTp.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
NpcTp.TextSize = 14
NpcTp.MouseButton1Click:connect(function()
    if NpcTpFrame.Visible == true then wait(.10)
                NpcTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true)
                wait(1) NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif WeaponTpFrame.Visible == true then wait(.10)
        WeaponTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) WeaponTpFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif HomeFrame.Visible == true then
        HomeFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) HomeFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif IslandTpFrame.Visible == true then
        IslandTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) IslandTpFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherScriptsFrame.Visible == true then
        OtherScriptsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif QuestTpFrame.Visible == true then
        QuestTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) QuestTpFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherTpFrame.Visible == true then
        OtherTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif TpPlayerFrame.Visible == true then
        TpPlayerFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) TpPlayerFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif SettingsFrame.Visible == true then
        SettingsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) SettingsFrame.Visible = false NpcTpFrame.Visible = true
        NpcTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    end
end)

NpcTpFrame.Name = "NpcTpFrame"
NpcTpFrame.Parent = NpcTp
NpcTpFrame.BackgroundColor3 = Color3.new(0.0235294, 0.0235294, 0.0235294)
NpcTpFrame.BorderColor3 = Color3.new(0.901961, 0.901961, 0.901961)
NpcTpFrame.BorderSizePixel = 0
NpcTpFrame.Position = UDim2.new(-1.96770537, 0, -1.82042623, 0)
NpcTpFrame.Size = UDim2.new(0, 191, 0, 269)
NpcTpFrame.Visible = false
NpcTpFrame.ScrollBarThickness = 12
NpcTpFrame.Active = true

NpcTpLabel.Name = "NpcTpLabel"
NpcTpLabel.Parent = NpcTpFrame
NpcTpLabel.BackgroundColor3 = Color3.new(0.666667, 0.333333, 1)
NpcTpLabel.Size = UDim2.new(0, 229, 0, 33)
NpcTpLabel.Font = Enum.Font.SourceSans
NpcTpLabel.Text = "TPNpc"
NpcTpLabel.TextColor3 = Color3.new(0, 0, 0)
NpcTpLabel.TextSize = 14

TPLuffy.Name = "Bring Luffy"
TPLuffy.Parent = NpcTpFrame
TPLuffy.BackgroundColor3 = Color3.new(0.168627, 0.188235, 0.168627)
TPLuffy.Position = UDim2.new(-0.00170067593, 0, 0.690840662, 0)
TPLuffy.Size = UDim2.new(0, 187, 0, 35)
TPLuffy.Font = Enum.Font.SourceSans
TPLuffy.Text = "Bring Luffy"
TPLuffy.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
TPLuffy.TextSize = 14
TPLuffy.MouseButton1Down:connect(function()
wait(1)
    game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "[Gui S.O.P]";
    Text = "Bring Luffy Thành Công";
})
for _,v in pairs(game.Workspace:GetDescendants()) do
  if string.find(v.Name, "Luffy") then
      v:FindFirstChild("HumanoidRootPart").Anchored = true
      v:FindFirstChild("HumanoidRootPart").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,-5)
   end
end
end)

IslandTp.Name = "IslandTp"
IslandTp.Parent = ScriptsFrame
IslandTp.BackgroundColor3 = Color3.new(0.14902, 0.14902, 0.14902)
IslandTp.Position = UDim2.new(0.0476484038, 0, 0.11152418, 0)
IslandTp.Size = UDim2.new(0, 100, 0, 31)
IslandTp.Font = Enum.Font.SourceSansLight
IslandTp.Text = "TpTớiĐảo"
IslandTp.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
IslandTp.TextSize = 14
IslandTp.MouseButton1Click:connect(function()
    if IslandTpFrame.Visible == true then wait(.10)
                IslandTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true)
                wait(1) IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif WeaponTpFrame.Visible == true then wait(.10)
        WeaponTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) WeaponTpFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif HomeFrame.Visible == true then
        HomeFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) HomeFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif NpcTpFrame.Visible == true then
        NpcTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) NpcTpFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherScriptsFrame.Visible == true then
        OtherScriptsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif QuestTpFrame.Visible == true then
        QuestTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) QuestTpFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherTpFrame.Visible == true then
        OtherTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif TpPlayerFrame.Visible == true then
        TpPlayerFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) TpPlayerFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif SettingsFrame.Visible == true then
        SettingsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) SettingsFrame.Visible = false IslandTpFrame.Visible = true
        IslandTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    end
end)

IslandTpFrame.Name = "IslandTpFrame"
IslandTpFrame.Parent = IslandTp
IslandTpFrame.BackgroundColor3 = Color3.new(0.0235294, 0.0235294, 0.0235294)
IslandTpFrame.BorderColor3 = Color3.new(0.901961, 0.901961, 0.901961)
IslandTpFrame.BorderSizePixel = 0
IslandTpFrame.Position = UDim2.new(-1.96906745, 0, -0.839429379, 0)
IslandTpFrame.Size = UDim2.new(0, 191, 0, 269)
IslandTpFrame.Visible = false
IslandTpFrame.ScrollBarThickness = 12
IslandTpFrame.Active = true

IslandTpLabel.Name = "IslandTpLabel"
IslandTpLabel.Parent = IslandTpFrame
IslandTpLabel.BackgroundColor3 = Color3.new(0.666667, 0.333333, 1)
IslandTpLabel.Size = UDim2.new(0, 229, 0, 33)
IslandTpLabel.Font = Enum.Font.SourceSans
IslandTpLabel.Text = "TpTớiĐảo"
IslandTpLabel.TextColor3 = Color3.new(0, 0, 0)
IslandTpLabel.TextSize = 14

TPToLuffyIsland.Name = "TP Luffy Island"
TPToLuffyIsland.Parent = IslandTpFrame
TPToLuffyIsland.BackgroundColor3 = Color3.new(0.168627, 0.188235, 0.168627)
TPToLuffyIsland.Position = UDim2.new(-0.00373976142, 0, 0.165683508, 0)
TPToLuffyIsland.Size = UDim2.new(0, 187, 0, 32)
TPToLuffyIsland.Font = Enum.Font.SourceSans
TPToLuffyIsland.Text = "Tp Tới Đảo Luffy"
TPToLuffyIsland.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
TPToLuffyIsland.TextSize = 14
TPToLuffyIsland.MouseButton1Down:connect(function()
wait(1)
    game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "[Gui S.O.P]";
    Text = "Tp Tới Đảo Luffy Thành Công";
})
for _,v in pairs(game.Workspace:GetDescendants()) do
   if string.find(v.ClassName, "Model") and string.find(v.Name, 'That noob') then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v:FindFirstChild("Head").CFrame
  end
end
end)

WeaponTp.Name = "WeaponTp"
WeaponTp.Parent = ScriptsFrame
WeaponTp.BackgroundColor3 = Color3.new(0.14902, 0.14902, 0.14902)
WeaponTp.Position = UDim2.new(0.0476484038, 0, 0.336978644, 0)
WeaponTp.Size = UDim2.new(0, 100, 0, 31)
WeaponTp.Font = Enum.Font.SourceSansLight
WeaponTp.Text = "TpVũKhí"
WeaponTp.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
WeaponTp.TextSize = 14
WeaponTp.MouseButton1Click:connect(function()
    if WeaponTpFrame.Visible == true then wait(.10)
                WeaponTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true)
                wait(1) WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif IslandTpFrame.Visible == true then
wait(.10)
        IslandTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) IslandTpFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif HomeFrame.Visible == true then
        HomeFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) HomeFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif NpcTpFrame.Visible == true then
        NpcTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) NpcTpFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherScriptsFrame.Visible == true then
        OtherScriptsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif QuestTpFrame.Visible == true then
        QuestTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) QuestTpFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif OtherTpFrame.Visible == true then
        OtherTpFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) OtherScriptsFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif TpPlayerFrame.Visible == true then
        TpPlayerFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) TpPlayerFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    elseif SettingsFrame.Visible == true then
        SettingsFrame:TweenSize(UDim2.new(0, 7,0, 269),"In","Sine",1,true) wait(1) SettingsFrame.Visible = false WeaponTpFrame.Visible = true
        WeaponTpFrame:TweenSize(UDim2.new(0, 191,0, 269),"In","Sine",1,true)
    end
end)

WeaponTpFrame.Name = "WeaponTpFrame"
WeaponTpFrame.Parent = WeaponTp
WeaponTpFrame.BackgroundColor3 = Color3.new(0.0235294, 0.0235294, 0.0235294)
WeaponTpFrame.BorderColor3 = Color3.new(0.901961, 0.901961, 0.901961)
WeaponTpFrame.BorderSizePixel = 0
WeaponTpFrame.Position = UDim2.new(-1.96899998, 0, -2.80200005, 0)
WeaponTpFrame.Size = UDim2.new(0, 191, 0, 269)
WeaponTpFrame.Visible = false
WeaponTpFrame.ScrollBarThickness = 12
WeaponTpFrame.Active = true

WeaponTpLabel.Name = "WeaponTpLabel"
WeaponTpLabel.Parent = WeaponTpFrame
WeaponTpLabel.BackgroundColor3 = Color3.new(0.666667, 0.333333, 1)
WeaponTpLabel.Size = UDim2.new(0, 229, 0, 33)
WeaponTpLabel.Font = Enum.Font.SourceSans
WeaponTpLabel.Text = "TpVũKhí"
WeaponTpLabel.TextColor3 = Color3.new(0, 0, 0)
WeaponTpLabel.TextSize = 14

TpWoodenSword.Name = "TpWooden Sword"
TpWoodenSword.Parent = WeaponTpFrame
TpWoodenSword.BackgroundColor3 = Color3.new(0.168627, 0.188235, 0.168627)
TpWoodenSword.Position = UDim2.new(-0.00512295868, 0, 0.165683448, 0)
TpWoodenSword.Size = UDim2.new(0, 187, 0, 23)
TpWoodenSword.Font = Enum.Font.SourceSans
TpWoodenSword.Text = "Tp Wooden Sword"
TpWoodenSword.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
TpWoodenSword.TextSize = 14
TpWoodenSword.MouseButton1Down:connect(function()
wait(1)
    game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "[Gui S.O.P]";
    Text = "Tp Wooden Sword Thành Công ";
})
for _,v in pairs(game.Workspace:GetDescendants()) do
  if string.find(v.Name, "Wooden Sword") and string.find(v.ClassName, "Model") then
      v:FindFirstChild("Head").Anchored = true
      v:FindFirstChild("Head").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,-5)
 end
end
end)

TpBisento.Name = "TpBisento"
TpBisento.Parent = WeaponTpFrame
TpBisento.BackgroundColor3 = Color3.new(0.168627, 0.188235, 0.168627)
TpBisento.Position = UDim2.new(-0.00190455257, 0, 0.620859027, 0)
TpBisento.Size = UDim2.new(0, 187, 0, 24)
TpBisento.Font = Enum.Font.SourceSans
TpBisento.Text = "Tp Bisento"
TpBisento.TextColor3 = Color3.new(0.811765, 0.811765, 0.811765)
TpBisento.TextSize = 14
TpBisento.MouseButton1Down:connect(function()
wait(1)
    game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "[Gui S.O.P]";
    Text = "Tp Bisento Thành Công ";
})
for _,v in pairs(game.Workspace:GetDescendants()) do
  if string.find(v.Name, "Bisento") and string.find(v.ClassName, "Model") then
      v:FindFirstChild("Head").Anchored = true
      v:FindFirstChild("Head").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,0,-5)
 end
end
end)
