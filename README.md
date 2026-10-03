# mac-key-repeat-tester

在瀏覽器裡試 macOS 的 key repeat，不必為了對一次系統設定就登出

滑桿對應 `InitialKeyRepeat` 與 `KeyRepeat`（單位是 15 ms），頁面會產生可直接貼進終端機的 `defaults write` 指令

這是單檔靜態站，正式網址由 GitHub Pages 提供

## 本地預覽

```bash
cd src
python3 -m http.server 8080
```

打開 <http://127.0.0.1:8080>

