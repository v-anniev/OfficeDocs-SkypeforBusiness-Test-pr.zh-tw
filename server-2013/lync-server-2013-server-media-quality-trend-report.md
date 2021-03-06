﻿---
title: 伺服器媒體品質趨勢報告
TOCTitle: 伺服器媒體品質趨勢報告
ms:assetid: 8a51fd13-1487-4632-b5ec-f7ae2abe8ed4
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ205071(v=OCS.15)
ms:contentKeyID: 49291594
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 伺服器媒體品質趨勢報告

 

_**上次修改主題的時間：** 2015-03-09_

伺服器媒體品質趨勢報告可供您以圖形方式最多比較 5 個伺服器的經驗品質計量，例如通話數、通話不良率、封包遺失和抖動。這有助於找出效能不彰的伺服器、使用率偏低的伺服器，或過度使用的伺服器。

## 存取伺服器媒體品質趨勢報告

從下列其中一個報告可存取伺服器媒體品質趨勢報告：

  - [Lync Server 2013 中的伺服器效能報告](lync-server-2013-server-performance-report.md) (按一下趨勢計量)

  - [Lync Server 2013 中的詳細通話報告](lync-server-2013-call-detail-report.md) (按一下 A/V Edge 伺服器計量。如果發話方或受話方是伺服器，您也可以按一下端點名稱，開啟伺服器品質媒體趨勢報告。)

## 善用伺服器媒體品質趨勢報告

對於特定伺服器，按一下[Lync Server 2013 中的伺服器效能報告](lync-server-2013-server-performance-report.md)上的趨勢計量，伺服器媒體品質趨勢報告將開啟。不過，您只會看見空白的報告；您在伺服器效能報告上選取的伺服器將不會出現在畫面上。您需要另外從 \[伺服器\] 下拉式清單選取該伺服器。而且，必須注意的是，\[伺服器\] 下拉式清單包含 \[全選\] 選項。如果您有 5 個以上的伺服器，這個選項不會有作用；伺服器媒體品質趨勢報告一次只能顯示最多 5 個伺服器的資料。

在伺服器媒體品質趨勢報告顯示的圖形中，標記為「通話數」和「通話不良率」的點是重要連結；按一下圖上的點將開啟一份[Lync Server 2013 中的通話清單報告](lync-server-2013-call-list-report.md)，其中顯示特定時段的通話數 (或不良通話數) 總計。

## 篩選

篩選器可以讓您傳回更精確的資料集或者以不同方法檢視傳回的資料。下表列出您可以搭配伺服器媒體品質趨勢報告的篩選。

### 伺服器媒體品質趨勢報告篩選

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[從]</p></td>
<td><p>時間範圍的開始日期/時間。若要按照小時檢視資料，請輸入開始日期和時間，如下所示：</p>
<p>7/7/2012 1:00 PM</p>
<p>如果您未輸入開始時間，報告會自動從指定日期凌晨 12 點開始。若要按照日期檢視資料，只要輸入日期即可：</p>
<p>7/7/2012</p>
<p>若要按星期或月份查看，請輸入當週或該月您想查看的日期 (您不必輸入當週或該月的第一天)：</p>
<p>7/3/2012</p>
<p>星期永遠是從星期日開始星期六結束。</p></td>
</tr>
<tr class="even">
<td><p>[到]</p></td>
<td><p>時間範圍的結束日期/時間。若要按照小時檢視資料，請輸入結束日期和時間，如下所示：</p>
<p>7/7/2012 1:00 PM</p>
<p>如果您未輸入結束時間，報告會自動在指定日期凌晨 12 點結束。若要按照日期檢視資料，只要輸入日期即可：</p>
<p>7/7/2012</p>
<p>若要按星期或月份查看，請輸入當週或該月您想查看的日期 (您不必輸入當週或該月的第一天)：</p>
<p>7/3/2012</p>
<p>星期永遠是從星期日開始星期六結束。</p></td>
</tr>
<tr class="odd">
<td><p>[間隔]</p></td>
<td><p>時間間隔。請選取下列其中一項：</p>
<ul>
<li><p>每小時 (最多可以顯示 25 個小時)</p></li>
<li><p>每日 (最多可以顯示 31 天)</p></li>
<li><p>每週 (最多可以顯示 12 週)</p></li>
</ul>
<p>若開始與結束日期超出所選間隔允許的上限值，將只會顯示上限值 (從開始日期開始顯示)。例如，若您選取 [每日] 間隔，並將開始與結束日期分別設為 7/7/2012 及 2/28/2012，將只會顯示 8/7/2012 上午 12 點至 9/7/2012 上午 12 點這段期間的資料 (亦即只會顯示 31 天的資料)。</p></td>
</tr>
<tr class="even">
<td><p>[伺服器類型]</p></td>
<td><p>通話所用的伺服器類型。允許的值為：</p>
<ul>
<li><p>中繼伺服器</p></li>
<li><p>A/V 會議伺服器</p></li>
<li><p>A/V Edge Server</p></li>
<li><p>閘道 (中繼伺服器)</p></li>
<li><p>閘道 (中繼伺服器旁路)</p></li>
<li><p>AS 會議伺服器</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>[伺服器]</p></td>
<td><p>工作階段中所用的伺服器名稱；這個下拉式清單會按照伺服器類型篩選的值自動連入。編譯報告時，您最多可選取 5 個不同的伺服器。</p></td>
</tr>
<tr class="even">
<td><p>[存取類型]</p></td>
<td><p>指出參與者登入內部網路或從外部網路登入。允許的值為：</p>
<ul>
<li><p>[全部]</p></li>
<li><p>內部</p></li>
<li><p>外部</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>[網路類型]</p></td>
<td><p>指出參與者連線的網路類型。允許的值為：</p>
<ul>
<li><p>[全部]</p></li>
<li><p>有線</p></li>
<li><p>無線</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>[VPN]</p></td>
<td><p>指出外部參與者是否在工作階段中使用虛擬私人網路 (VPN) 連線。允許的值為：</p>
<ul>
<li><p>[全部]</p></li>
<li><p>VPN</p></li>
<li><p>非 VPN</p></li>
</ul></td>
</tr>
</tbody>
</table>


## 計量

下表列出伺服器媒體品質趨勢報告提供的資訊。

### 伺服器媒體品質趨勢報告計量

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名稱</th>
<th>可以排序這個項目嗎？</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[通話數]</p></td>
<td><p>無</p></td>
<td><p>通話總數。</p></td>
</tr>
<tr class="even">
<td><p>[降低 (MOS)]</p></td>
<td><p>無</p></td>
<td><p>通話時經歷的 MOS (平均意見分數) 降級平均總時間。降級值的範圍可以從 0.0 (低) 到 5.0 (高)；值為 0.5 或更少的時間表示可接受的降級。根據歷史經驗，平均意見分數的計算方式就是讓使用者為通話品質打上 1 到 5 的分數。Lync Server 使用一組演算法來預告使用者如何為通話打分數。</p>
<p>網路堵塞、頻寬不足、無線網路堵塞或受到干援，或者媒體伺服器或端點超過負載，都會造成降級值變得相當高。降級太高會造成音訊扭曲或遺漏。</p></td>
</tr>
<tr class="odd">
<td><p>[通話不良百分比]</p></td>
<td><p>無</p></td>
<td><p>歸類為通話不良的次數。通話不良是指至少一項測量的計量超過允許的值 (例如，通話時斷斷續續聽不清楚)。</p></td>
</tr>
<tr class="even">
<td><p>[來回時間 (ms)]</p></td>
<td><p>無</p></td>
<td><p>即時傳輸通訊協定封包傳送至另一個端點再返回，平均所需的時間 (毫秒)。來回時間為 200 毫秒或更少被視為可接受的品質。</p>
<p>國際電話路由、路由設定錯誤，或者媒體伺服器超過負載時，會造成來回時間值變得相當大。來回時間太長會使得雙向、即時的音訊通話變得難以進行。</p></td>
</tr>
<tr class="odd">
<td><p>[封包遺漏]</p></td>
<td><p>無</p></td>
<td><p>即時傳輸通訊協定 (RTP) 封包遺漏的平均速率 (當 RTP 封包 (在網際網路傳輸音訊和視訊使用的通訊協定) 無法抵達目的地時，就會發生封包遺漏)。高遺漏值通常是由下列幾種狀況造成：壅塞、頻寬不足、無線網路壅塞或干擾，或是媒體伺服器超載。封包遺漏一般會導致聲音扭曲或遺失音訊。</p></td>
</tr>
<tr class="even">
<td><p>[抖動 (ms)]</p></td>
<td><p>無</p></td>
<td><p>RTP 封包之間抵達時間的平均抖動 (抖動是估算通話「不穩定」的方法)。高抖動值通常是由下列幾種狀況造成：壅塞，或是媒體伺服器超載，導致聲音扭曲或遺失音訊。</p></td>
</tr>
<tr class="odd">
<td><p>[修復隱藏比率]</p></td>
<td><p>無</p></td>
<td><p>隱藏音訊樣本與樣本總數的平均比率 (隱藏音訊樣本是一種用於平滑音訊因一般網路封包遺漏而造成突然轉變的技術)。高比值表示因為封包遺漏或抖動而運用了大量的遺失隱藏技術，導致聲音扭曲或遺失音訊。</p></td>
</tr>
<tr class="even">
<td><p>[修復延伸比率]</p></td>
<td><p>無</p></td>
<td><p>延伸音訊樣本與樣本總數的平均比率 (延伸音訊是指當偵測到網路封包遺漏時，為了維持通話品質而延展的音訊)。高比值表示有大量因抖動產生的樣本延伸，導致音訊聽起來像機器人或扭曲。</p></td>
</tr>
<tr class="odd">
<td><p>[修復壓縮比率]</p></td>
<td><p>無</p></td>
<td><p>壓縮音訊樣本與樣本總數的平均比率 (壓縮音訊是指當偵測到網路封包遺漏時，為了維持通話品質而壓縮的音訊)。高比值表示有大量因抖動產生的樣本壓縮，導致音訊聽起來變快或扭曲。</p></td>
</tr>
</tbody>
</table>

