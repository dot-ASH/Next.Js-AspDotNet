*Next.js app on .NET 6.0 application*

### Requirements

---

- .NET 6 SDK
- Node 16 LTS (including npm)

### Usage

---

- Create React App first

```
dotnet new react
```

- Initialize Next.js

```
yarn create next-app
```

-  Replace all files of ClientApp folder with next.js files 

```
rm -r ClientApp
mkdir ClientApp
shopt -s dotglob
mv  -v my-app/* ClientApp/
rm -r my-app/
```

- Replace `npm` with `yarn` in nextApp.csproj file and replace lines-

```
<SpaProxyServerUrl>http://localhost:3000</SpaProxyServerUrl>
<SpaProxyLaunchCommand>yarn dev</SpaProxyLaunchCommand>

```
nextApp.csproj and also SpaProxyServerUrl to http://localhost:3000 

- Start the server

```
dotnet run 
```

Reload after successfully compiled

