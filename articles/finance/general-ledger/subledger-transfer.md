---
title: Yardımcı defterden Genel muhasebeye transfer
description: Bu konu, Microsoft Dynamics 365 Finance içindeki genel muhasebe transfer işlemiyle ilgili olan yetenekleri açıklar.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de9328f69938151c5558d41263d36b873d117e4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975495"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Yardımcı defterden Genel muhasebeye transfer

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Finance'un, alt genel muhasebe günlük girişleri toplu işleri aktarma kurallarıyla ilişkili özellikleri açıklanmaktadır.

Sürüm 8.1'de kuralların aktarılmasına izin vermek için değişiklikler yapıldı ve **Zaman Uyumlu** seçeneği kullanım dışı bırakıldı. Daha fazla bilgi için bkz. [Finance and Operations için kaldırılan veya artık kullanılmayan özellikler](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Alt genel muhasebe toplu işlemlerine transfer için aşağıdaki seçenekler kullanılabilir. 

 - Zaman uyumsuz – Bu seçenek, hemen, genel muhasebe hesap girişlerinin transfer zamanlamasını General muhasebeye nakleder. Kaynaklar bu isteği sunucuda işlemek için serbest bırakılır bırakılmaz, genel muhasebe fişi kaydedilecektir. 

- Planlanan toplu iş-bu seçenek, girişlerin teslim alındığı sırada işleneceği genel muhasebede işleme sırasına aktarılan alt genel muhasebe hesap girişlerini ekler. Kaynaklar bu isteği sunucuda işlemek için serbest bırakılır bırakılmaz, genel muhasebe fişi kaydedilecektir. 
 
Sürüm 10.0.8'de Zaman uyumsuz seçeneğinin performansını artırmak için iyileştirmeler yapılmıştır. Bu özellik, performansın en iyi duruma getirilmesi **Genel muhasebe Özellik adı alt genel muhasebe aktarımı** altında etkinleştirilir. 
 
Bu işlevsellik, alt iş defterindeki verilerin genel muhasebeye aktarılmasını geliştirir. Sürecin daha etkili olmasını sağlar ve transfer için birlikte daha küçük hareket kümeleri gruplandırır. Bu, toplu iş sunucusunun daha etkili bir şekilde kullanılmasına olanak sağlar. Bu işlevsellik, Zaman Uyumsuz transfer seçeneğinin çalışması için toplu iş sunucusunun ayarlanmış, çevrimiçi ve çalışır durumda olmasını gerektirir. 
