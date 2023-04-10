# Printing

```
print("hello") - string
print(true) - boolean
print(3+3) (prints 6) - interger
```

# Variables

```
Local Name1 = 7 - (Name1 is the variable)
Print(Name1) - (will print 7)
```

# Wait

```Wait(2) - (waits 2 seconds)```

# Properites

```
local Part = game.Workspace.(name of part)
-------------------------------------------------
Part.Anchored = false - (anchored is a property) (true and false can enable and disable it) (example: Part.Anchored = ture will make it anchored)
-------------------------------------------------
Part.BrickColor = BrickColor.new("name of color") - (changes the brick color duh)
Part.BrickColor = BrickColor.Random() - (random brick color)
-------------------------------------------------
Part.Position = Vector3.new(-17, 0.5, 3) - (vector3.new is too add/change new x, y, z scales to the part)
Part.Size = Vector3.new(25, 7, 33) - (will change the original size to the x, y, z scale that you add)
-------------------------------------------------
```

# Functions

```
function ChangeColor()
	local Functionspart = game.Workspace.Fpart
	Functionspart.BrickColor = BrickColor.Random()
end

(nothing will happen if you run it like this)

wait(2)

ChangeColor()

- (After 2 seconds it will change color) (it will start after you wrote the line after function (this was ChangeColor())) (must add "()" after writing what will be a function starter example: function miau() now when you type "miau()" the function will start)
-------------------------------------------------
function Changecolor(Functionspart)
	Functionspart.BrickColor = BrickColor.Random()
end

wait(2)

Changecolor(game.Workspace.FPart)

wait(2)

Changecolor(game.Workspace.FPart2)

wait(2)

Changecolor(game.Workspace.FPart3) - will change the color of 3 individual blocks
-------------------------------------------------
function ChangecolorRed(Functionspart1)
	Functionspart1.BrickColor = BrickColor.new("Really red")
	function ChangecolorYellow (Functionspart2)
		Functionspart2.BrickColor = BrickColor.new("New Yeller")
		function ChangecolorGreen (Functionspart3)
			Functionspart3.BrickColor = BrickColor.new("Lime green")
		end
	end
end

wait(2)

ChangecolorRed(game.Workspace.FPart1)
print("Get Ready!")

wait(2)

ChangecolorYellow(game.Workspace.FPart2)
print("Steady!")

wait(2)

ChangecolorGreen(game.Workspace.FPart3)
print("Go!") 
(A countdown that changes each block red yellow green respectivley and prints ready steady go)
(FPart is a part that you have to create and rename to FPart)(make sure to number them)
```
# Events

```
game.Players.PlayerAdded:Connect(function(plr)
	print("Hello player!")
end) -Sends (a message when a player joins) (There are many more player events but the tutorial im watching says that they wont get into it)
```
# If statments

```
if 1 + 1 == 2 then
	print("Thoust statment 1 + 1 = 2 is indeed true")
end - (if its true then it will print) (it must be written as "==" so it doesnt get mistaken as a variable)
-------------------------------------------------
local Vari = "124"

if Vari == "124" then
	print("yes")
end - (yes it is 124 so it prints yes)
-------------------------------------------------
local Vari = "124"

if Vari == "123" then
	print("yes")
end -(since its not 123 it will not print)
-------------------------------------------------
local Vari = "124"

if Vari == "122" then
	print("yes")
elseif Vari == "123" then
	print("yes 123")
else
	print("No NO NOOO!")
end -(else means that if its any thing other than "123 or 122" it will print NOOOO)
--------------------------------------------------
if 1 + 1 == 2 and 2 + 2 == 4 then
	print("indeed")
end -("and" just means if you want to add more than 1 if statment but dont want to flood with if this if that)
--------------------------------------------------
local Vari = "122" or "126"

if Vari == "124" or "126" then
	print("This is true")
end -("or" would make it so that if its this or that then it would do the action)
--------------------------------------------------
local Vari = game.Workspace.IFPart

if 5 < 19 then
	wait(2)
	Vari.BrickColor = BrickColor.new("Really blue")
end -(i made a part and named it IFPart and did that if 5 is LESS THAN 19 then in 2 seconds the part would turn really blue)
```
# Tables

```
local STable = {"wow",2,64,true}

print(#STable)- (use {} for tables) (would print 4 since there are 4 objects/index seperated by commas in the brackets) ("#" would mean number of)
--------------------------------------------------
local STable = {"wow",2,64,true}

print(STable[3]) -(use [] for selecting objects in the table) (it would print 64 since its the third index in the table)
--------------------------------------------------
local STable = {"wow",2,64,true}

table.insert(STable, "This will be added to the table") -(now its the fifth index in the table)

print(STable[5]) -(would print the newly added fifth index thats in the table)
--------------------------------------------------
local STable = {"wow",2,64,true}

table.insert(STable, "This will be added to the table")

print(STable[5])

table.remove(STable,5)

print(STable[5]) -(initially would print index 5 but after removing the fifth index it will say nil since its no longer an index)
```
# Instancing

```
local CPart = Instance.new("Part")

CPart.Parent = game.Workspace -(parent will make it so that its in an area) (will place a part in the middle of the map) (the spawn point can cover it)
--------------------------------------------------
function spawnpart()
	local CPart = Instance.new("Part")
	CPart.Parent = game.Workspace
	CPart.BrickColor = BrickColor.Random()
end

spawnpart()

wait(1)

spawnpart()

wait(1)

spawnpart()

wait(1)

spawnpart() -(will add a random colored part every 1 second)
----------------------------------------------------
function spawnexplosion()
	local Iexplosion =Instance.new("Explosion")
	Iexplosion.Parent = game.Workspace
end

wait(1)

spawnexplosion() -(will spawn an explosion in 1 second)
-----------------------------------------------------
local Iexplosion = Instance.new("Explosion")
	Iexplosion.Parent = game.Workspace


wait(1)


Iexplosion:Destroy() -(will remove the explosion)
```
# Cloning

```
(Press ctrl + g to model a group of selected parts into one)
wait(2)
local CLPart = game.ReplicatedStorage.Parts:Clone()
CLPart.Parent = game.Workspace -(first drag and drop part into replicatedstorage) (it will spawn a clone in 2 seconds)
-------------------------------------------------------
wait(2)
local CLPart = game.ReplicatedStorage.Parts:Clone()
CLPart.Parent = game.Workspace

wait(3)

CLPart:Destroy() -(it will destroy the clone in 3 seconds)
```
# Loops

```
for Index = 1, 10, 1 do -(Index = 1, stops when Index = 10, increase Index by 1 every loop until 10)
	print(Index)
end -(will print from 1 to 10)
-------------------------------------------------------
for Index = 1, 300, 1 do
	wait(0.01)
	local cpart = Instance.new("Part")
	cpart.Parent = game.Workspace
	cpart.BrickColor = BrickColor.Random()
	cpart.Material = Enum.Material.Neon
end -(will place 300 random colored neon blocks every 0.01 seconds)
-------------------------------------------------------
local Ltable = {3,6,1,75,2}

for i,v in pairs(Ltable) do -(Loop through every part of Ltable) (i is index and v is value) (the forth index is 4 and the forth value is 75)
	
end
--------------------------------------------------------
while true do -(will loop if true)
	
end
--------------------------------------------------------
while true do
	wait(0.01)
	local cpart = Instance.new("Part")
	cpart.Parent = workspace
	cpart.BrickColor =BrickColor.Random()
	cpart.Material = Enum.Material.Neon
	cpart.Shape = Enum.PartType.Ball
end -(will flood the map with random neon color balls forever)
```
