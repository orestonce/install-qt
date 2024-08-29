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
    	<td>arch</td>
		<td>编译主机</td>
    	<td>特点</td>
    </tr>
    <tr>
        <td rowspan="9">windows</td>
	    <td>Qt4.8.7-Windows-x86-MinGW4.9.4-20200104</td>
    	<td>x86</td>
		<td>Windows XP SP3</td>
    	<td>编译生成的二进制支持windows xp</td>
    </tr>
    <tr>
        <td>Qt5.6.3-Windows-x86-MinGW4.9.4-staticFull-20200104</td>
		<td>x86</td>
		<td>Windows XP SP3</td>
    </tr>
    <tr>
        <td>Qt5.15.7-Windows-x86-MinGW8.1.0-staticFull-20221104</td>
		<td>x86</td>
		<td></td>
    </tr>
    <tr>
        <td>Qt5.15.7-Windows-x86_64-MinGW8.1.0-staticFull-20221104</td>
		<td>amd64</td>
		<td></td>
    </tr>
    <tr>
        <td>Qt5.15.14-Windows-x86-MinGW8.1.0-staticFull-20240527</td>
		<td>x86</td>
		<td>Windows 11 10.0.22631</td>
		<td>macos版和windows版</td>
    </tr>
    <tr>
        <td>Qt5.15.14-Windows-x86_64-MinGW8.1.0-staticFull-20240527</td>
		<td>amd64</td>
		<td>Windows 11 10.0.22631</td>
        <td>macos版和windows版</td>
    </tr>
    <tr>
        <td>Qt6.5.3-Windows-x86_64-MinGW13.2.0-ucrt-staticFull-20240527</td>
		<td>amd64</td>
		<td>Windows 11 10.0.22631</td>
    </tr>
    <tr>
    <tr>
        <td>Qt6.7.2-Windows-x86_64-MinGW13.2.0-ucrt-20240621</td>
		<td>amd64</td>
		<td>Windows 11 10.0.22631</td>
		<td>最新版本Qt</td>
    </tr>
    <tr>
	<td rowspan="3">macos</td>
		<td>Qt5.6.3-macOS-x86_64-AppleClang6.1.0-noFramework-20191202</td>
		<td>amd64</td>
		<td>OS X 10.10</td>
    </tr>
	<tr>
		<td>Qt5.15.14-macOS-Universal-AppleClang15.0.0-noFramework-20240527</td>
		<td>arm64/amd64</td>
		<td>macOS 14.5</td>
		<td>macos版和windows版；<br> 此编译器在macos-13、macos-14上分别输出amd64和arm64二进制</td>
	</tr>
    <tr>
        <td>Qt6.7.2-macOS-Universal-AppleClang15.0.0-noFramework-20240621</td>
		<td>arm64/amd64</td>
		<td>macOS 14.5</td>
		<td>最新版本Qt；<br> 此编译器在macos-13、macos-14上分别输出amd64和arm64二进制</td>
    </tr>
