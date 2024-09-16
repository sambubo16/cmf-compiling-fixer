# CMF compiling fixer. Fix errors easier.
Hi. Are you seen error of CMF compiling in Minglium?
I provided it on images. So, right now i coded a compiling - fixer of CMF, to replace the errors with directly going to this fixer.
Its so angry error for me. Now you can just add this - you will be able fix this error much easier, than you think.
Source code:
```bat
:CMFCompilingFixer
rem CMF Compiling Fixer for Minglium. v3.1
cd cmf
set "files=sysm-main.cmf bgsys-m.cmf"
set "tempFiles=TEMP_1.cmd TEMP2.cmd"
set "index=0"
for %%f in (%files%) do (
    if exist %%f (
        set "fchk!index!=0"
    ) else (
        set "fchk!index!=1"
    )
    set /a index+=1
)
set "check=!fchk0!!fchk1!"
if !fchk0!=="1" (
    ren TEMP_1.cmd sysm-main.CMF
) else (
    rem
)
if !fchk1!=="1" (
    ren TEMP2.cmd bgsys-m.CMF
) else (
    rem
)
cd..
goto start
```
![image](https://github.com/user-attachments/assets/bc28a099-0fcf-4ff4-a36b-812f0b3b11ae)
