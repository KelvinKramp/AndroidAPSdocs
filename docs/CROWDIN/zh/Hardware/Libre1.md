# Freestyle Libre 1

要將您的 Libre 用作 CGM，每 5 分鐘獲取一次新的血糖值，而無需掃描傳感器，您需要購買一個 NFC 到藍牙橋接器（基於已過時的[LimiTTer](https://github.com/JoernL/LimiTTer) 項目的商用設備）。

:::{admonition} Libre 2、Libre 1 US 和 Libre Pro :class: warning 確認您要使用的橋接器和應用程式與您的傳感器相容。  
:::

市場上有幾款橋接器可供選擇：

-   [MiaoMiao 讀取器](https://www.miaomiao.cool/)（版本 1、2 或 3），也可在 AliExpress 上購買。
-   [Blucon Nightrider](https://www.ambrosiasys.com/our-products/blucon/)（請注意，最新的韌體版本可能與所有應用程式不相容，供應商應用程式不會向 AAPS 廣播資料）。
-   [Bubble（或 Bubble Mini）](https://www.bubblesmartreader.com/)，來自歐洲供應商（[Bubblan](https://www.bubblan.org/)，[BubbleShop](https://bubbleshop.eu/)），或適用於俄羅斯用戶[點擊此處](https://vk.com/saharmonitor/)。 也可在 AliExpress 上購買。
-   適用於俄羅斯用戶的 Atom。

歷史上，使用特定手錶 Sony Smartwatch 3（SWR50），其中具有 NFC 晶片，可啟用並用作 NFC 收集器是可能的。 然而，上述列出的定制 NFC 到藍牙橋提供了一個不那麼複雜的解決方案，並且將被大多數希望將其 Libre 1（非 US）用作 CGM 的人使用。

-   Sony Smartwatch 3（SWR50）<https://github.com/pimpimmi/LibreAlarm/wiki/>

目前來看，使用 Libre 1 作為血糖來源時，無法在 SMB 算法中啟用「始終啟用 SMB」和「在用餐後啟用 SMB」。 Libre 1 的血糖值不夠平滑，無法安全使用。 有關更多詳細資訊，請參閱[平滑血糖資料](../Usage/Smoothing-Blood-Glucose-Data-in-xDrip.md)。

## 1. 使用 xDrip+

-   xDrip+ 支援 MiaoMiao、Bubble、Blucon、Atom 和 LibreAlarm。
-   除非您需要最新功能，否則可以安全下載[最新 APK（穩定版）](https://xdrip-plus-updates.appspot.com/stable/xdrip-plus-latest.apk)，在這種情況下，您應該使用最新的[Nightly Snapshot](https://github.com/NightscoutFoundation/xDrip/releases)。
-   按照[xDrip+ 設定頁面](../Configuration/xdrip.md)上的設置說明進行操作。
-    您還需要適用於 Libre 1 US（和 Libre 2 EU）的[OOP2](https://drive.google.com/file/d/1f1VHW2I8w7Xe3kSQqdaY3kihPLs47ILS/view)。
-   在[ConfigBuilder 的血糖來源](../Configuration/Config-Builder.md#bg-source)中選擇 xDrip+。

## 2. 使用 Glimp

-   Glimp 支援 Miaomiao、Blucon 和 Bubble 用於 Libre 1 和 Libre 2 EU。
-   您需要 Glimp 版本 4.15.57 或更新版本。 舊版本不支援。
-   安裝 [Glimp](https://play.google.com/store/apps/details?id=it.ct.glicemia)。
-   在 [ConfigBuilder 的血糖來源](../Configuration/Config-Builder.md#bg-source) 中選擇 Glimp。

## 3. 使用 Tomato

- Tomato 是 Miaomiao 的官方應用程式。
- 安裝 [Tomato](http://tomato.cool/#download_page) 並按照廠商的[說明](http://tomato.cool/how-to-broadcast-data-to-android-aps/tips/)操作。
- 在 [ConfigBuilder 的血糖來源](../Configuration/Config-Builder.md#bg-source) 中選擇 Tomato。

## 4. 使用 Diabox

- Diabox 是 Bubble 的官方應用程式。
- 安裝 [Diabox](https://t.me/s/DiaboxApp)。 在設定中，進入「整合」，啟用「與其他應用程式共享資料」。

![Diabox](../images/Diabox.png)

- 在[ConfigBuilder 的血糖來源](../Configuration/Config-Builder.md#bg-source)中選擇 xDrip+。
