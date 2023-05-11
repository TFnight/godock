# Godock

## 搭配 Laradock 其他服務使用，Godock 僅啟動 golang 環境
* 預設開啟 `libsodium`、`go module`
* 網路配置連結至外部 container 網路 `laradock_backend`
* 同步檔案 `APP_PATH_HOST` 至 `APP_PATH_CONTAINER`