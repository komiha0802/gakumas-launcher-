# 學園偶像大師 啟動器

這是一個不需要 DMM GAME PLAYER 與 VPN 就能執行《學園偶像大師》（DMM 版）的 Windows 啟動器。

請至 [Releases](../../releases) 下載 `GakumasLauncher.exe` 並執行。遊戲必須先前已透過 DMM GAME PLAYER 安裝完成。

## 日本連線方式

| 方式 | 說明 |
|---|---|
| VPN Gate | 預設值。僅在啟動器內連線至築波大學的 VPN Gate 公開伺服器，無需額外設定。 |
| VPN 檔案 | 使用您正在使用的 VPN 服務設定檔在啟動器內連線。支援 OpenVPN (`.ovpn`) 與 WireGuard (`.conf`)。 |
| 一般連線 | 直接使用 PC 的網際網路而不使用 VPN。若身處日本境外，請先透過 VPN 應用程式連線至日本。 |

VPN Gate 與 VPN 檔案不會更改 Windows 的網路設定，僅會讓啟動器的通訊透過 VPN。

### VPN 檔案使用方式

1. 從 VPN 服務的帳號頁面下載**日本伺服器**的手動設定檔（OpenVPN 或 WireGuard）。
2. 在啟動器中點選 **VPN 檔案** → **選擇檔案**來選取下載好的檔案。
3. 若為需要帳號與密碼的 OpenVPN 檔案，請輸入至**帳號**欄位中。這通常是手動設定用（OpenVPN）的帳號，而非服務登入密碼。

設定檔與帳號會經過加密儲存，僅限此 PC 的 Windows 帳號能夠解密。

## 建置 (Build)

```
cargo build --release --bin GakumasLauncher
```

## 注意事項

DMM 不支援日本以外地區的存取。使用相關服務產生的風險須由使用者自行承擔。
