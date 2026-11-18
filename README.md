# Open Fishing 资产

`Game/GameAssembly.dll` 适用于 RF4 `4.0.25034`。该版本默认使用 CN，账户入口使用 `http://127.0.0.1:7515`。

## 接入项目

```powershell
git clone --depth 1 --branch rf4-4.0.25034-r1 https://github.com/real-uangi/open-fishing.git
git -C open-fishing rev-parse HEAD
Get-FileHash -Algorithm SHA256 -LiteralPath ./open-fishing/Game/GameAssembly.dll
```

在项目中记录返回的完整提交 SHA 以固定依赖版本。对照 [manifest.json](manifest.json) 核验 SHA-256 后，将 DLL 复制到对应版本的游戏工作副本根目录。

在已配置为独立启动的工作副本中，直接启动 `rf4_x64.exe`。省略 `-region` 时默认使用 CN。
