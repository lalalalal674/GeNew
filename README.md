GeNew
A tiny programming language for people who say when instead of if.

GeNew is written in plain, readable words on purpose — no curly braces, no semicolons, nothing scary. If you can read this sentence, you can read GeNew code.

Try it live: lalalalal674.github.io/GeNew

Installing GeNew as an app
You don't need to download or install anything to run GeNew — it works straight in your browser. But you can also install it as a standalone app on your computer, so it opens in its own window instead of a browser tab.

On a computer (Chrome or Edge)
Go to lalalalal674.github.io/GeNew
Look at the right side of the address bar for a small install icon — it looks like a little monitor with a down arrow, or a + inside a box
Click it, then click Install in the popup
GeNew now opens as its own app, with its own icon you can pin to your taskbar or desktop
If you don't see that icon, open the browser's ⋮ menu (top right) and look for "Install GeNew…" or "Save and share" → "Install page as app."

Firefox and Safari don't support this kind of install — Chrome or Edge only.

On phone or tablet
Open the site in your browser
Tap the share icon (iOS) or the ⋮ menu (Android)
Choose "Add to Home Screen"
That's it — no app store, no download, no account needed.

Writing your first program
Open the editor on the left side of the page and type:

write "hello world"
Click run, and you'll see hello world appear on the right.

The whole language, in one page
Comments
Anything after %NOTE% on a line is ignored — use it to leave yourself notes.

%NOTE% this line does nothing when the code runs
Variables
Set a value with =.

x = 10
name = "Bob"
Output
Use write to print something to the screen.

write "hello"
write x
Conditionals
Use when ... do ... end instead of if.

when x is 10 do
    write "x is ten"
end
Comparisons you can use:

Symbol	Meaning
is	equals
>	is higher than
<	is lower than
>=	is higher than or equal to
<=	is lower than or equal to
Combine conditions with AND / OR:

when x > 5 AND x < 20 do
    write "x is in range"
end
Loops
for every step(n) do ... end runs the code n times. step holds the current loop count (1, 2, 3…).

for every step(5) do
    write step
end
Use stop to break out of a loop early:

for every step(100) do
    when step is 10 do
        stop
    end
end
Functions
Define a reusable block with define, and call it by name.

define greet(name) do
    write "hello, "
    write name
end

greet("Bob")
Use return to send a value back out of a function.

define double(n) do
    return n * 2
end

write double(21)    %NOTE% prints 42
Arrays
A list of values, in square brackets.

nums = [10, 20, 30]
write nums[0]         %NOTE% prints 10

nums[0] = 99           %NOTE% change a value
write nums             %NOTE% prints [99, 20, 30]
Built-in array tools:

Function	What it does
length(x)	how many items in an array (or characters in a string)
push(arr, val)	adds val to the end of the array
pop(arr)	removes and returns the last item
push(nums, 40)
write length(nums)     %NOTE% prints 4
Math
GeNew supports normal arithmetic: + - * /

total = 5 + 3 * 2
write total            %NOTE% prints 11
Working with .gnw files
GeNew programs can be saved and reopened as .gnw files, right from the page:

save .gnw — downloads your current code as a file you can keep or share
open .gnw — loads a .gnw file from your computer back into the editor
A complete example
%NOTE% adds up every number from 1 to 10, and shows progress
total = 0

for every step(10) do
    total = total + step
    when step is 5 do
        write "halfway there"
    end
end

write "the total is:"
write total
Built with GeNew v1.
