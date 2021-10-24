# SimpleHttpServer

This is simple & unsecure HTTP server in C#, it should serve fine if you don't have Python installed instead of [http.server](https://docs.python.org/3/library/http.server.html). 

Download from built exe from [releases](https://github.com/malacupa/SimpleHttpServer.cs).

## Usage

Start server as:
```powershell
.\simplehttpserver.exe <listen host/IP> <listen port>
```

Download from the server:
```powershell
# Powershell 3.0+
iwr -Uri http://<listenhost>:<port>/filename.dll -OutFile filename.dll
```

Upload to the server:
```powershell
# Powershell 3.0+
Invoke-RestMethod -Method POST -Body ([System.IO.File]::ReadAllBytes('c:\filename.dll)) http://<listenhost>:<port>/?fn=filename.dll
```

or use web browser


## Compile

```powershell
c:\windows\microsoft.net\framework64\v4.0.30319\csc.exe /out:.\httpserver.exe .\SimpleHttpServer.cs

# or

c:\windows\microsoft.net\framework64\v4.0.30319\MSBuild.exe .\SimpleHttpServer.csproj
```

## License
[unlicense](https://unlicense.org/)
