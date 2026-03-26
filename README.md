-- Criar ScreenGui
local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Parent = game.CoreGui

-- Frame principal (menu)
local MainFrame = Instance.new("Frame")
MainFrame.Parent = ScreenGui
MainFrame.Size = UDim2.new(0, 400, 0, 300)
MainFrame.Position = UDim2.new(0.5, -200, 0.5, -150)
MainFrame.BackgroundColor3 = Color3.fromRGB(120, 0, 0) -- vermelho escuro
MainFrame.BorderSizePixel = 0

-- Borda estilo executor
local UIStroke = Instance.new("UIStroke")
UIStroke.Parent = MainFrame
UIStroke.Color = Color3.fromRGB(255, 0, 0)
UIStroke.Thickness = 2

-- Título
local Title = Instance.new("TextLabel")
Title.Parent = MainFrame
Title.Size = UDim2.new(1, 0, 0, 40)
Title.BackgroundColor3 = Color3.fromRGB(180, 0, 0)
Title.Text = "EXECUTOR MENU"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 24

-- Caixa de texto (script input)
local TextBox = Instance.new("TextBox")
TextBox.Parent = MainFrame
TextBox.Size = UDim2.new(1, -20, 0, 150)
TextBox.Position = UDim2.new(0, 10, 0, 50)
TextBox.BackgroundColor3 = Color3.fromRGB(60, 0, 0)
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.Text = "-- coloque seu script aqui"
TextBox.ClearTextOnFocus = false
TextBox.MultiLine = true

-- Botão executar
local ExecuteButton = Instance.new("TextButton")
ExecuteButton.Parent = MainFrame
ExecuteButton.Size = UDim2.new(0.45, 0, 0, 40)
ExecuteButton.Position = UDim2.new(0.05, 0, 1, -50)
ExecuteButton.BackgroundColor3 = Color3.fromRGB(200, 0, 0)
ExecuteButton.Text = "EXECUTAR"
ExecuteButton.TextColor3 = Color3.fromRGB(255, 255, 255)

-- Botão limpar
local ClearButton = Instance.new("TextButton")
ClearButton.Parent = MainFrame
ClearButton.Size = UDim2.new(0.45, 0, 0, 40)
ClearButton.Position = UDim2.new(0.5, 0, 1, -50)
ClearButton.BackgroundColor3 = Color3.fromRGB(150, 0, 0)
ClearButton.Text = "LIMPAR"
ClearButton.TextColor3 = Color3.fromRGB(255, 255, 255)

-- Funções
ExecuteButton.MouseButton1Click:Connect(function()
    local code = TextBox.Text
    loadstring(code)()
end)

ClearButton.MouseButton1Click:Connect(function()
    TextBox.Text = ""
end)# Gg-hub
