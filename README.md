-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local UICorner_2 = Instance.new("UICorner")
local TextLabel_2 = Instance.new("TextLabel")
local UICorner_3 = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local TextButton_2 = Instance.new("TextButton") -- Botón de cerrar
local UICorner_5 = Instance.new("UICorner")
local MinimizeButton = Instance.new("TextButton") -- Botón de minimizar
local UICorner_6 = Instance.new("UICorner")
local RestoreButton = Instance.new("TextButton") -- Botón de restaurar

-- Pantalla de bienvenida:

local WelcomeScreen = Instance.new("ScreenGui")
local WelcomeLabel = Instance.new("TextLabel")

WelcomeScreen.Parent = game.CoreGui

WelcomeLabel.Parent = WelcomeScreen
WelcomeLabel.Size = UDim2.new(1, 0, 1, 0) -- Ocupar toda la pantalla
WelcomeLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fondo negro
WelcomeLabel.TextColor3 = Color3.fromRGB(255, 255, 255) -- Texto blanco
WelcomeLabel.Font = Enum.Font.LuckiestGuy
WelcomeLabel.Text = "MADE BY: YANSER_EXPLOIT\nHELPER: ELOSO"
WelcomeLabel.TextScaled = true
WelcomeLabel.TextWrapped = true

-- Mostrar el mensaje durante 3 segundos antes de continuar

task.wait(3)
WelcomeScreen:Destroy()

-- Configuración de la GUI principal:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.ResetOnSpawn = false

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Size = UDim2.new(0, 181, 0, 204)
Frame.Active = true
Frame.Draggable = true

UICorner.Parent = Frame

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(104, 104, 104)
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Size = UDim2.new(0, 181, 0, 23)
TextLabel.Font = Enum.Font.LuckiestGuy
TextLabel.Text = "snowboard simuleitor"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

UICorner_2.Parent = TextLabel

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(104, 104, 104)
TextLabel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(0, 0, 0.828431368, 0)
TextLabel_2.Size = UDim2.new(0, 181, 0, 35)
TextLabel_2.Font = Enum.Font.LuckiestGuy
TextLabel_2.Text = "Made BY: YANSER_EXPLOIT HELPER: ELOSO"
TextLabel_2.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.TextScaled = true
TextLabel_2.TextSize = 14.000
TextLabel_2.TextWrapped = true

UICorner_3.Parent = TextLabel_2

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(109, 109, 109)
TextButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0, 0, 0.205882356, 0)
TextButton.Size = UDim2.new(0, 181, 0, 41)
TextButton.Font = Enum.Font.LuckiestGuy
TextButton.Text = "Infinito spin \"op\""
TextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextWrapped = true
TextButton.MouseButton1Click:Connect(function()
	loadstring(game:HttpGet("https://pastebin.com/raw/FLAJRkHY"))()
end)

UICorner_4.Parent = TextButton

-- Botón de cerrar script
TextButton_2.Parent = Frame
TextButton_2.BackgroundColor3 = Color3.fromRGB(109, 0, 0)
TextButton_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton_2.BorderSizePixel = 0
TextButton_2.Position = UDim2.new(1, 0, 0, 0)
TextButton_2.Size = UDim2.new(0, 62, 0, 31)
TextButton_2.Font = Enum.Font.LuckiestGuy
TextButton_2.Text = "✖"
TextButton_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_2.TextScaled = true
TextButton_2.TextSize = 14.000
TextButton_2.TextWrapped = true

UICorner_5.Parent = TextButton_2

-- Botón de minimizar
MinimizeButton.Parent = Frame
MinimizeButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
MinimizeButton.Position = UDim2.new(0.7, 0, 0, 0)
MinimizeButton.Size = UDim2.new(0, 50, 0, 31)
MinimizeButton.Font = Enum.Font.LuckiestGuy
MinimizeButton.Text = "-"
MinimizeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
MinimizeButton.TextScaled = true

UICorner_6.Parent = MinimizeButton

-- Botón de restaurar (oculto al inicio)
RestoreButton.Parent = ScreenGui
RestoreButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
RestoreButton.Position = UDim2.new(0.9, 0, 0, 0) -- Esquina superior derecha
RestoreButton.Size = UDim2.new(0, 50, 0, 31)
RestoreButton.Font = Enum.Font.LuckiestGuy
RestoreButton.Text = "+"
RestoreButton.TextColor3 = Color3.fromRGB(255, 255, 255)
RestoreButton.TextScaled = true
RestoreButton.Visible = false -- Se oculta al inicio

-- Funciones de minimizar y restaurar
MinimizeButton.MouseButton1Click:Connect(function()
	Frame.Visible = false
	RestoreButton.Visible = true
end)

RestoreButton.MouseButton1Click:Connect(function()
	Frame.Visible = true
	RestoreButton.Visible = false
end)

-- Función para cerrar la GUI
TextButton_2.MouseButton1Click:Connect(function()
	ScreenGui:Destroy()
end)
