# Installations

https://docs.godotengine.org/en/latest/contributing/development/compiling/compiling_for_windows.html

## [scons](https://scons.org/)
pyenv is used

scons installation
```
PS C:\Users\simon\github\godot> python -m pip install scons
Requirement already satisfied: setuptools in c:\users\simon\.pyenv\pyenv-win\versions\3.11.8\lib\site-packages
PS C:\Users\simon\github\godot> where.exe scons
C:\Users\simon\.pyenv\pyenv-win\shims\scons
C:\Users\simon\.pyenv\pyenv-win\shims\scons.bat
```
C:\Users\simon\.pyenv\pyenv-win\versions\3.11.8\Scripts\scons.exe

Build exe
```
PS C:\Users\simon\github\godot> python -m SCons
..
[Initial build] Linking Static Library core\core.windows.editor.x86_64.lib ...
[Initial build] Linking Program bin\godot.windows.editor.x86_64.exe ...
   Creating library bin\godot.windows.editor.x86_64.lib and object bin\godot.windows.editor.x86_64.exp
[Initial build] Linking Program bin\godot.windows.editor.x86_64.console.exe ...
[Initial build] scons: done building targets.
[Time elapsed: 00:25:46.808]
```

generate visual studion solution
```
PS C:\Users\simon\github\godot> python -m SCons vsproj=yes
PS C:\Users\simon\github\godot> start godot.sln
```

### Build options (SConstruct)
```
PS C:\Users\simon\github\godot> python -m SCons dev_build=true
[100%] Linking Program bin\godot.windows.editor.dev.x86_64.exe ...
   Creating library bin\godot.windows.editor.dev.x86_64.lib and object bin\godot.windows.editor.dev.x86_64.exp
[100%] Linking Program bin\godot.windows.editor.dev.x86_64.console.exe ...
[100%] scons: done building targets.
[Time elapsed: 00:11:11.468]
```
