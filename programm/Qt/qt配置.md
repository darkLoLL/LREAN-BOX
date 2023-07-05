## 在clion中配置qt5工具

### 配置desiger

```sh
# desiger
program: C:\Qt\Qt5.14.2\5.14.2\mingw73_64\bin\designer.exe
Argument: $FileNameWithoutExtension$.ui
Working directory: $FileDir$
```



### 配置pyuic

```sh
# pyuic
program: C:\Qt\Qt5.14.2\5.14.2\mingw73_64\bin\uic.exe
Argument: $FileName$ -o $FileNameWithoutExtension$.py -x 
Working directory: $FileDir$
```



## 在pycharm中配置qt5工具

### 配置desiger

```sh
# desiger
program: $ProjectFileDir$/venv/Lib/site-packages/qt5_applications/Qt/bin/designer.exe
Argument: $FileNameWithoutExtension$.ui
Working directory: $FileDir$
```

### 配置pyuic

```sh
# pyuic
program: $ProjectFileDir$\venv\Scripts\pyuic5.exe
Argument: $FileName$ -o $FileNameWithoutExtension$.py -x 
Working directory: $FileDir$
```

