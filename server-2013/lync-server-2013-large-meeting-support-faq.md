﻿---
title: Lync Server 2013 大型會議支援常見問題集
TOCTitle: Lync Server 2013 大型會議支援常見問題集
ms:assetid: 34b4fb6a-e35c-47e8-8ab1-f8331741fed2
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ204804(v=OCS.15)
ms:contentKeyID: 49290549
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 大型會議支援常見問題集

 

_**上次修改主題的時間：** 2012-10-22_

下列各節提供建立與舉行大型會議的常見問題解答。

## 問：大型會議中可以有多少使用者參與？

Lync Server 使用者模型在共用集區中指定的限制為 250 位使用者，在大型會議專屬的集區中指定的限制則為 1000 位使用者，但是，這些數字僅表示我們測試的使用者數目，而且僅適用於我們測試中所使用的一組特定硬體。我們是根據測試來建議這些大小上限的限制。但是，您可以藉由設定一或多個會議原則 (您可以使用 Lync Server 管理命令介面中的 Windows PowerShell Cmdlet 或使用 Lync Server 控制台 來設定 )，以控制組織中允許參與會議的實際人數。您在會議原則中指定的數目可以是介於 1 和 4,294,967,295 之間的任一個 32 位元整數，但建議的人數為 2 到 250 (含) 位參與者；預設值為 250。

## 問：在大型會議專屬的集區中可以有多少個會議或其他工作負載？

若要在最多 1000 位參與者的大型會議中確保最佳使用者經驗，建議在大型會議專屬的集區中一次僅舉行單一大型會議。同時建議當大型會議正在進行時，不要允許任何其他工作負載於該集區上執行。

## 問：大型會議的召集人應該位於專屬集區中嗎？

否。除了專門管理大型會議排程的員工之外，建議不要讓任何其他使用者位於專屬集區中。這樣可以防止其他即時通訊流量導致集區中所舉行的大型會議發生問題。您應該使用大型會議排程員工的使用者帳戶，在專屬集區中排程大型會議。您應該將會議召集人 (申請大型會議的使用者) 的使用者帳戶新增為大型會議的主持人。

## 問：我可以在大型會議中使用哪些媒體形式？

最多含有 1000 位使用者的大型會議可以包含音訊、視訊、PowerPoint 共用、 白板及目前狀態輪詢。

## 問：我可以在大型會議中使用群組立即訊息 (IM) 嗎？

可以。但是，大量的立即訊息 (特別是在大量與會者進行傳送時) 會因為在 IM 視窗中快速捲動文字的問題而影響到使用者經驗。將大量立即訊息傳遞給最多 1000 位使用者也會引發顯著的伺服器負載，這會影響到效能。IM 通常只有在進行問題與解答 (Q\&A) 時才需使用。

## 使用者可以從電話撥入來加入大型會議嗎？

可以。如果 Lync Server 2013 集區已正確部署並針對電話撥入式會議加以啟用，使用者將能透過撥入來加入大型會議。我們的測試顯示 1000 位使用者中最多有 15% 的使用者可以在 10 分鐘內加入大型會議。

## 問：我可以在虛擬拓撲中舉行大型會議嗎？

我們尚未在虛擬拓撲中測試過大型會議，因此，不支援使用虛擬機器來裝載適用於大型會議的專屬集區。
