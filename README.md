# paoKuProject
EndlessRunner  
该程序适用于Windows 10 (x64)操作系统；  

编程语言：C++，编译器：gcc；  

项目构建需安装MSYS2开发环境（https://www.msys2.org/#installation）。安装完成后，程序会提示是否立即打开MSYS2。若选择同意，请确保使用UCRT64环境；  

安装完成后，首先执行以下命令更新系统：  
`pacman -Suy`  

接着为UCRT64环境安装gcc编译器：  
`pacman -S mingw-w64-ucrt-x86_64-gcc`  

安装make工具：  
`pacman -S mingw-w64-ucrt-x86_64-make`  

在UCRT64环境中构建项目需依次执行以下命令：  
`mingw32-make init`  
`mingw32-make`  

注：`mingw32-make init`命令会创建用于存放中间文件的obj目录。  

若需在VS Code中构建项目，需完成以下步骤：  
1. 将UCRT64的bin目录路径（默认安装路径为C:\msys64\ucrt64\bin）添加到系统环境变量PATH中  
2. 在终端执行：  
`mingw32-make init`  
`mingw32-make`  

