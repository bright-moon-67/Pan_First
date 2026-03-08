# 在服务器上ssh使用codex
1.找到系统代理端口地址（例如127.0.0.1:7897）  
2.打开本地的C:\Users\{Your_User_Name}\.ssh\config，添加一行：   
`RemoteForward 7897 127.0.0.1:7897`  
3.使用Vscode远程连接至服务器  
4.使用Ctrl+Shift+P或者F1打开命令面板，搜索并打开Preference: Open Remote Settings(JSON)(Your_Server_Name)，输入：    
`{
    "http.proxy": "http://127.0.0.1:7897",
    "https.proxy": "http://127.0.0.1:7897",
}
`    
5.重新远程连接即可正常使用codex
