---
title: Sorun giderme Analitik raporları
description: Bu konuda, bir müşterinin veri değişiklikleri müşterinin çalışma alanlarının hiçbirinde görünmüyorsa sorunların nasıl giderileceği ve tanılanacağı açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2d085c041c1d12eef1271fd3f78262be19fd0629
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413447"
---
# <a name="troubleshoot-analytic-reports"></a>Sorun giderme Analitik raporları

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Çıkış**

Bir müşterinin verisi, müşterinin herhangi bir çalışma alanındaki **Analitik** sekmesinde görüntülenmiyor.

**Nedeni**

Varsayılan olarak Microsoft Power BI raporları, her dört saatte bir yenilenir, Dağıtım ölçüm toplu işine uygun olarak.

**Çözünürlük**

Bu sorun, zamanlama nedeniyle olabilir. Bu adımları izleyerek toplu işi başlatın ve analitik çalışma alanlarını güncelleştirin.

1. **Toplu işler** sayfasını **Sistem yönetimi \> Bağlantılar \> Toplu işler \> Toplu işler**'i açın. Alternatif olarak, aramayı kullanın ve **Toplu işler**'e girin.
1. **Ölçümü dağıt** işini listede bulun.
1. Sayfanın üstünde **Düzenle**'yi seçin ve zamanlanan başlangıç tarihini/saatini, analitikleri geçerli tarihe daha yakın bir zamanda yenileyecek değere ayarlayın.

![Toplu İşler.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
