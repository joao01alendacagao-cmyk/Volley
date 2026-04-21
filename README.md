local Rayfield = loadstring(game:HttpGet("https://sirius.menu/rayfield"))()

local Window = Rayfield:CreateWindow({
   Name = "KZIN HUB",
   LoadingTitle = "KZIN HUB",
   LoadingSubtitle = "by você",
   ConfigurationSaving = {
      Enabled = false
   }
})

local MainTab = Window:CreateTab("Main", 4483362458)

local Toggle = MainTab:CreateToggle({
   Name = "Ativar Reward",
   CurrentValue = false,
   Flag = "RewardToggle",
   Callback = function(Value)
      if Value then
         local remote = game:GetService("ReplicatedStorage")
            :WaitForChild("Packages")
            :WaitForChild("_Index")
            :WaitForChild("sleitnick_knit@1.7.0")
            :WaitForChild("knit")
            :WaitForChild("Services")
            :WaitForChild("SeasonService")
            :WaitForChild("RF")
            :WaitForChild("RequestRankedReward")

         pcall(function()
            remote:InvokeServer(1)
         end)
      end
   end,
})
