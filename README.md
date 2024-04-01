# Laravel 10 管理和追蹤日誌檔案

引入 arcanedev 的 log-viewer 套件來擴增管理和追蹤每個日誌檔案，為了能有效的利用各種來源的日誌資訊，日誌的收集、分析歸類並將其集中儲存是不可或缺的。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 對 `config/logging.php` 設定檔做變更，使用 `daily` 日誌模式以便進行日誌觀察。
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/log-viewer` 來進行管理和追蹤日誌檔案。

----

## 畫面截圖
![](https://i.imgur.com/sDLmUsJ.png)
> 全部日誌檔的各級別錯誤數量以圖表方式顯示

![](https://i.imgur.com/96AOoSe.png)
> 每天日誌檔的各級別錯誤數量以清單方式顯示
