## 💡 說明
本模塊基於 [Box For Magisk](https://github.com/taamarin/box_for_magisk/tree/master) 修改，讓其更符合我的個人使用習慣，修改內容：
- 默認使用 Clash.Meta 內核
- 內置了 Releases 發佈時的最新內核、geox、Web UI
- 修改 Clash 的訂閱文件默認名稱爲`config.yaml`，以便啓動
- 每次啓動時先更新訂閱

## 📀 刷入
1. 在 [Releases](https://github.com/ChiesiMario/box_for_magisk/releases) 下載最新版本
2. 使用 Magisk 或者 KernelSu 刷入
3. 刷入過程會提示是否更新「內核和 Geox」，模塊已經內置了可以不更新直接使用。如果覺得內置的過時了，可以挂代理後更新。
4. 刷入完畢後，前往 `data/adb/box/settings.ini` 中，在 `subscription_url_xxxx` 中填寫你的訂閱鏈接
5. 重啓後查看 `data/adb/box/run` 下面的日誌，如無問題可以訪問 `http://127.0.0.1:9090/ui` 訪問 Web UI （9090 端口取決於你的配置文件，`external-ui: /data/adb/box/clash/dashboard` 要存在於配置文件內。）
6. Enjoy it.

## 📑 其他
更多用法請查看 [Box for Magisk](https://github.com/taamarin/box_for_magisk/blob/master/docs/index_cn.md) 的文檔 
- 更新所有內核和其他
  ```
  su -c /data/adb/box/scripts/box.tool all
  ```
- 啓動或停止
  ```
  su -c /data/adb/box/scripts/box.service start
  ```
- 更新訂閱
  ```
  su -c /data/adb/box/scripts/box.tool subs
  ```
## 🙏🏻 Credits
- [Box For Magisk](https://github.com/taamarin/box_for_magisk/tree/master)
- [box4magisk](https://github.com/CHIZI-0618/box4magisk)
