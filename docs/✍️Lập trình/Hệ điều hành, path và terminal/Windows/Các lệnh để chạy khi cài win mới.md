---
share: true
created: 2023-10-24T18:26
updated: 2024-12-18T15:37
---
PowerShell

## Cho phép PowerShell chạy script 
```PowerShell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned
```

"C:\Program Files\PowerShell\7\pwsh.exe" D:\Dropbox\Config\Startup.ps1

## Đảm bảo script được chạy với quyền quản trị
```PowerShell
param([switch]$Elevated)
function Test-Admin {
    $currentUser = New-Object Security.Principal.WindowsPrincipal $([Security.Principal.WindowsIdentity]::GetCurrent())
    $currentUser.IsInRole([Security.Principal.WindowsBuiltinRole]::Administrator)

}

if ((Test-Admin) -eq $false)  {
    if ($elevated) {
        # tried to elevate, did not work, aborting
    } else {
        Start-Process powershell.exe -Verb RunAs -ArgumentList ('-noprofile -noexit -file "{0}" -elevated' -f ($myinvocation.MyCommand.Definition))

    }
    exit
}
## Running with full privileges
```

## Run
`control userpasswords2`

## Tắt Defender
- Search for `gpedit.msc` and click the top result to open the Local Group Policy Editor.
- Browse the following path:  
    Computer Configuration > Administrative Templates > Windows Components > Microsoft Defender Antivirus

## Sửa lỗi boot
```
bootsect/nt60 sys
bootrec /fixmbr
bootrec /fixboot
```

<iframe width="560" height="315" src="https://www.youtube.com/embed/watch?reload=9&v=lRCyb7FzWFY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
