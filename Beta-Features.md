# Beta v0.4.0
All of the content listed here is subject for change.
<br /><br /><br /><br />

# Editor Instance
- ## Methods
- - :Select(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance), Index: [Index](), Color: [Color3?](https://create.roblox.com/docs/reference/engine/datatypes/Color3)) -> [Frame](https://create.roblox.com/docs/ui/frames) <br />
Makes a new selection frame. <br />
![image](https://github.com/user-attachments/assets/b6de409f-38bc-4974-9a9c-d39bf066e1b0)
<br /><br /><br />
- - :AutoFill(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance)) -> [string](https://create.roblox.com/docs/luau/strings) <br />
Autofills word on which cursorposition currently is.
<br /><br /><br />
- - :Fill(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance), Index: [Index](), Word: [string](https://create.roblox.com/docs/luau/strings)) -> [string](https://create.roblox.com/docs/luau/strings) <br />
Inserts word, cutting symbols from Index.Start to Index.End from line.
<br /><br /><br />
- - :GetAutoFill(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance), GetData: [bool?](https://create.roblox.com/docs/luau/booleans)) -> { [string](https://create.roblox.com/docs/luau/strings) } <br />
Returns table of strings that can possibly fit the word, on which cursorposition currently is. <br />
Also returns [Index]() and word itself. If `GetData` is set to `true`, will only return them.
<br /><br /><br />
- - :VisualiseWord(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance), Word: [string](https://create.roblox.com/docs/luau/strings)) -> () <br />
Creates [Selector Instance]() on every word position in every line.
<br /><br /><br />
- - :GetWord(self: [Editor Instance](https://github.com/gdr1461/GEditor/wiki/Editor-Instance)) -> [string](https://create.roblox.com/docs/luau/strings) <br />
Returns word, on which cursor position is currently on.
<br /><br /><br />
- ## Variables
- - AutoFillEnabled: [bool](https://create.roblox.com/docs/luau/booleans) <br />
> [!IMPORTANT]
> AutoFill doesn't work automaticly at the moment, this variable will only disable AutoFill methods. <br />

If set to `true`, will enable AutoFill.
<br /><br /><br />
- - SelectionEnabled: [bool](https://create.roblox.com/docs/luau/booleans) <br />
> [!IMPORTANT]
> Selection doesn't work automaticly at the moment, this variable will only disable Select methods. <br />

If set to `true`, will enable selections.
<br /><br /><br />
- - Colors.Selector: [table](https://create.roblox.com/docs/luau/tables) <br />
Contains selector's `Default` and `WordSelector` colors.

# Line Instance
- ## Methods
- - :FindWord(Keyword: string) <br />
Returns [indices]() of found word in given line.
<br /><br /><br />
- - :GetIndexPosition(Index: number, GetRaw: bool?) <br />
Returns UDim2 position of symbol index in line.
<br /><br /><br />
- - :GetSelectionPosition(Index: Index) <br />
Returns position of given index in line.
<br /><br /><br />
- - :GetSelectionSize(Index: Index) <br />
Returns size of given index in line.
<br /><br /><br />
- - :GetAutoFill(GetData: bool?) <br />
Just like `Editor:GetAutoFill()`, but for specific line instead of focused one.
