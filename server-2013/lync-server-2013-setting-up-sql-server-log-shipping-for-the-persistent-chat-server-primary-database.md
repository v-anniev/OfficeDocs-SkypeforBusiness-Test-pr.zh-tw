﻿---
title: Lync Server 2013：針對常設聊天室伺服器主要資料庫設定 SQL Server 記錄傳送
TOCTitle: 針對常設聊天室伺服器主要資料庫設定 SQL Server 記錄傳送
ms:assetid: 088ea1c2-d592-4a11-b3b8-f1e2f8beae93
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ204653(v=OCS.15)
ms:contentKeyID: 49290012
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 在 Lync Server 2013 中針對常設聊天室伺服器主要資料庫設定 SQL Server 記錄傳送

 

_**上次修改主題的時間：** 2012-11-12_

使用 SQL Server Management Studio，連線至 常設聊天室伺服器 次要記錄傳送資料庫執行個體，並確定 SQL Server Agent 執行中。

使用連線至 常設聊天室主要資料庫執行個體的 SQL Server Management Studio，執行下列步驟：

1.  確定 SQL Server Agent 執行中。

2.  以滑鼠右鍵按一下 mgc 資料庫，然後按一下 \[內容\] 。

3.  在 \[選取頁面\] 底下，按一下 \[交易記錄傳送\] 。

4.  選取 \[將此啟用為記錄傳送組態的主要資料庫\] 核取方塊。

5.  在 \[交易記錄備份\] 底下，按一下 \[備份設定\] 。

6.  在 \[備份資料夾的網路路徑\] 方塊中，輸入您為交易記錄備份資料夾建立之共用的網路路徑。

7.  如果備份資料夾位在主要伺服器上，請在 \[如果備份資料夾位於主要伺服器上，請輸入至該資料夾的本機路徑 (範例: c:\\backup):\] 方塊中輸入備份資料夾的本機路徑。(如果備份資料夾不在主要伺服器上，可將此方塊保留空白。)
    
    > [!IMPORTANT]  
    > 如果主要伺服器上的 SQL Server 服務帳戶是在本機系統帳戶之下執行，則必須在主要伺服器上建立備份資料夾，並指定該資料夾的本機路徑。
    


8.  設定 \[指定刪除檔案的時限\] 及 \[如果未在此時間內進行備份，則發出警示\] 參數。

9.  在 \[備份工作\] 底下，查看列示在 \[排程\] 方塊中的備份排程。若要自訂安裝的排程，請按一下 \[排程\] ，並依需要調整 SQL Server Agent 排程。

10. 在 \[壓縮\] 底下選取 \[使用預設伺服器設定\] ，然後按一下 \[確定\] 。

11. 在 \[次要伺服器執行個體與資料庫\] 底下，按一下 \[新增\] 。

12. 按一下 \[連線\] ，並連線至您已設定為次要伺服器的 SQL Server 執行個體。

13. 在 \[次要資料庫\] 方塊中，從清單選取 \[mgc\] 資料庫。

14. 在 \[初始化次要資料庫\] 索引標籤上，選擇 \[是，產生主要資料庫的完整備份，並將其還原到次要資料庫 (若次要資料庫不存在則另行建立)\] 選項。

15. 在 \[複製檔案\] 索引標籤上的 \[複製之檔案的目的資料夾\] 方塊中，輸入複製交易記錄備份的目的資料夾路徑。此資料夾通常位在次要伺服器上。

16. 在 \[複製工作\] 底下，注意列示在 \[排程\] 方塊中的複製排程。若要自訂安裝的排程，請按一下 \[排程\] ，並依需要調整 SQL Server Agent 排程。此排程應與備份排程大致相同。

17. 在 \[還原\] 索引標籤上的 \[還原備份時的資料庫狀態\] 底下，選擇 \[不復原模式\] 選項。

18. 在 \[延遲還原備份至少:\] 底下，選取 \[0 分鐘\] 。

19. 在 \[如果未在此時間內進行還原，則發出警示\] 底下，選擇警示臨界值。

20. 在 \[還原工作\] 底下，查看列示在 \[排程\] 方塊中的還原排程。若要自訂安裝的排程，請按一下 \[排程\] ，依需要調整 SQL Server Agent 排程，然後按一下 \[確定\] 。此排程應與備份排程大致相同。

21. 在 \[資料庫內容\] 對話方塊上按一下 \[確定\] ，即開始設定程序。

