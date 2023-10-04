# batch-scripts

To make the most out of windows command prompt, you can:
- create a new folder named environ (or whatever you like) in your `C:\Users\USERNAME` folder.
- put the batch scripts you want inside of it.
- put the C:\Users\USERNAME\environ folder to the path.
- run your batch scripts from anywhere.

Here's how to create the folder and add it to path:
- open cmd
- type this:

```bat
mkdir %userprofile%\environ && echo created environ folder.
echo changing into the created directory: && cd %userprofile%\environ
for /f %a in ('cd') do echo setx PATH "%path%;%a" && echo adding %cd% to path.
```

and you are done with it. you can now put your batch scripts in the environ folder.

# If you want to put shortcuts into that environ folder, and run them via ⊞ + r, you can do so by:
```bat
setx PATHEXT "%PATHEXT%;.LNK"
```
