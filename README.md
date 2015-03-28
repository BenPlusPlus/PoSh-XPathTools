# XPathTools (PowerShell Module)

The XPathTools module makes it a breeze to edit your PC's PATH environment variables. Just a few simple cmdlets are all you need to read your existing PATH entries or to add and remove any folders you desire.

### How to use

As with any PoSh module, the first thing to do is to extract the module files to your personal or system Modules folder, ensuring the files are located in a subfolder named `XPathTools`. Next, you can import the module into your PowerShell session:

```powershell
Import-Module "XPathTools"
```

Here's the quick-and-dirty rundown on each of XPathTools' cmdlets in turn:

The `Get-Path` cmdlet, by default, returns the entire PATH variable (which one depends upon the use of the -UserEnvironment switch) as a single string. By including the -Itemized switch, however, each path in PATH (heh, heh) is a separate element in a string array.

`Add-Path` and `Remove-Path` do exactly what their names imply: add and remove a folder path to the PATH environment variable. Of course, these cmdlets accept pipeline input.

Perhaps the least useful cmdlet, but included for completion's sake, is `Set-Path`. This function simply replaces the current contents of the PATH variable with a new value.

As implied above, each of the four cmdlets observe the -UserEnvironment switch, which causes the user (rather than the system) PATH variable to be retrieved or modified.

Note: Any modification of the system PATH variable will, of course, require that your PowerShell session is running with administrative rights.

