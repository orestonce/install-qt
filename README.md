* 静态编译Qt/MinGW来源于: https://build-qt.fsu0413.me/ , 仓库地址 https://github.com/Fsu0413/QtCompile

使用方法:

	- name: install qt static
	  uses: orestonce/install-qt@main
	  with:
		version: Qt5.15.7-Windows-x86_64-MinGW8.1.0-staticFull-20221104

	- name: build  
	  run: |
		cd image2pdf-qt && qmake && mingw32-make release && cd ..
		dir image2pdf-qt\release\image2pdf-qt.exe

支持的runner.os和version
<table><tbody>
    <tr>
        <td>runner.os</td>
        <td>version</td>
    </tr>
    <tr>
        <td rowspan="3">windows</td>
	<td>Qt5.6.3-Windows-x86-MinGW4.9.4-staticFull-20200104</td>
    </tr>
    <tr>
        <td>Qt5.15.7-Windows-x86-MinGW8.1.0-staticFull-20221104</td>
    </tr>
    <tr>
        <td>Qt5.15.7-Windows-x86_64-MinGW8.1.0-staticFull-20221104</td>
    </tr>
    <tr>
	<td rowspan="1">macos</td>
    	<td>Qt5.15.14-macOS-Universal-AppleClang15.0.0-noFramework-20240527</td>
    </tr>
