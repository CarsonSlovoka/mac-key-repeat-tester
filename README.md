# mac-key-repeat-tester

在瀏覽器裡試 macOS 的 key repeat，不必為了對一次系統設定就登出

滑桿對應 `InitialKeyRepeat` 與 `KeyRepeat`（單位是 15 ms），頁面會產生可直接貼進終端機的 `defaults write` 指令

這是單檔靜態站，正式網址由 GitHub Pages 提供

## 線上嘗試

> https://carsonslovoka.github.io/mac-key-repeat-tester/

## 本地預覽

```bash
git clone https://github.com/CarsonSlovoka/mac-key-repeat-tester
cd mac-key-repeat-tester/src
python3 -m http.server 8080
```

打開 <http://127.0.0.1:8080>


## config

```sh
defaults write -g InitialKeyRepeat -float 8.0  # Initial delay       # mac 26可以低於10, 用3太快會沒辦法用, 建議不要低於6
defaults write -g KeyRepeat        -float 1    # Key repeat interval # 能設定的比1還低，但目前最低還是只能到1的效果。希望之後mac可以改進
defaults write -g ApplePressAndHoldEnabled -bool false # 按住時是否會顯示特殊符號。例如按住a會顯示: à、á、â、ä.
```

