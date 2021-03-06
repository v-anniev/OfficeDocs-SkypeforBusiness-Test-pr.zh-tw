﻿---
title: Lync Server 2013：媒體旁路概觀
TOCTitle: 媒體旁路概觀
ms:assetid: 9ea090b3-f607-46f7-97dd-2510052524e5
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Gg412740(v=OCS.15)
ms:contentKeyID: 49291820
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 中的媒體旁路概觀

 

_**上次修改主題的時間：** 2012-09-21_

當您想要將部署的中繼伺服器數目降到最低時，媒體旁路會很實用。中繼伺服器集區通常會部署在中央網站，而且它會控制分支網站的閘道。啟用媒體旁路時，可讓來自分支網站用戶端的公用交換電話網路 (PSTN) 通話媒體直接流經這些網站的閘道。 Lync Server 2013 撥出電話路由和 企業語音原則必須正確設定，以便來自分支網站用戶端的 PSTN 通話可以路由傳送至適當的閘道。

Wi-Fi 網路通常會比有線網路遇到更多封包遺失問題。從此封包遺失中復原通常不是閘道可以配合進行的事。因此，我們建議您先評估 Wi-Fi 網路的品質，再確定是否應啟用無線子網路的旁路。此外，還要考慮在延遲減少與封包遺失復原之間取捨。RTAudio 是可用於不會略過中繼伺服器之通話的轉碼器，較適合用來處理封包遺失。

在您的 企業語音結構就緒後，規劃媒體旁路便相當簡單。

  - 如果您有集中式拓撲，但沒有連至分支網站的 WAN 連結，您可以啟用全域媒體旁路，因為不需要精細的控制。

  - 如果您有分散式拓撲，且其中包含一或多個網路地區及其附屬的分支網站，請確定下列幾項：
    
      - 您的中繼伺服器對等端是否可以支援媒體旁路所需的功能。
    
      - 每個網路地區中的哪些網站已妥善連接。
    
      - 哪種媒體旁路和通話許可控制的組合適合您的網路。

啟用媒體旁路時，系統會自動為網路地區和該地區內沒有頻寬限制的所有網路網站產生唯一的旁路 ID。至於地區內具有頻寬限制的網站，以及透過 WAN 連結連接至地區且具有頻寬限制的網站，系統則會分別指派網站專屬的唯一旁路 ID。

當使用者撥打電話到 PSTN 時， 中繼伺服器會比較用戶端子網路的旁路 ID 和閘道子網路的旁路 ID。如果這兩個旁路 ID 相符，系統會將媒體旁路用於通話。如果旁路 ID 不符，通話的媒體就必須流經 中繼伺服器。

當使用者接聽來自 PSTN 的通話時，使用者的用戶端會比較自身的旁路 ID 和 PSTN 閘道的旁路 ID。如果這兩個旁路 ID 相符，媒體會略過 中繼伺服器直接從閘道流向用戶端。

只有 Lync 2010 或更新版本的用戶端和裝置才支援與 中繼伺服器進行媒體旁路互動。

> [!IMPORTANT]  
> 除了在全域啟用媒體旁路外，您還必須個別在每個 PSTN 主幹上啟用媒體旁路。如果在全域啟用旁路，但沒有為特定 PSTN 主幹啟用，則不會針對任何牽涉該 PSTN 主幹的通話叫用媒體旁路。此外，當媒體旁路設為 [使用網站和地區資訊] 時，必須將所有可路由傳送的子網路與其所在網站產生關聯。如果在不需要旁路的網站中有可路由傳送的子網路，這些子網路應該先在新網站中組成群組，您再啟用媒體旁路。這麼做可確保為無法路由傳送的子網路指派不同的旁路 ID。



## 請參閱

#### 概念

[Lync Server 2013 中的媒體旁路模式](lync-server-2013-media-bypass-modes.md)  
[Lync Server 2013 中的媒體旁路和通話許可控制](lync-server-2013-media-bypass-and-call-admission-control.md)  
[Lync Server 2013 中媒體旁路的技術需求](lync-server-2013-technical-requirements-for-media-bypass.md)

