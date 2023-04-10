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
