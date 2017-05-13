## Mongoclient, Electron Packaging Scaffold
Scaffold for electron packaging of [Mongoclient](https://github.com/mongoclient/mongoclient), can be used with the [MeteorJS](https://github.com/meteor/meteor) applications

### Steps
1. Bundle mongoclient with command: `meteor build --server --directory <output>` and put contents into `app` folder
2. Copy contents of `C:\Users\Sercan\AppData\Local\.meteor\packages\meteor-tool\<version>\mt-os.windows.x86_32\dev_bundle\server-lib\node_modules` to `app\programs\server\node_modules`
3. Copy `Node (4.7.3)` to `bin` folder
4. Copy `Mongod (>= 3.2.6)` to `bin` folder
5. Run `npm install` on scaffold directory

### Steps to RUN directly
- Run: `npm install -g electron`
- Run: `electron .`

### Steps to PACKAGE
- Run: `npm install -g electron-packager`
- Run: `electron-packager . Mongoclient --appVersion=2.0.0 --buildVersion=2.0.0 --icon=D:\git\mongoclient_packaged\app\programs\web.browser\app\logo\head.ico --overwrite --out=D:\git\mongoclient_packaged\packaged --electronVersion=1.6.2`

### Steps to AFTER-PACKAGE - Optional for short and clean paths, especially on Windows build)
- Run: `npm install -g modclean@1.2.7`
- Run: cd `my/app/path/resources/app` 
- Run: `modclean -n default:safe,default:caution`

### License
Licensed under AGPL v3.0
