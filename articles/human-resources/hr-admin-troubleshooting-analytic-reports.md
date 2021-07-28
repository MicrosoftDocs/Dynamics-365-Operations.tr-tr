---
title: Sorun giderme Analitik raporları
description: Bu konu, müşterinin verisindeki değişiklikler müşterinin herhangi bir çalışma alanında görüntülenmediğinde ne yapılacağını açıklar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 382780405b2496cc655451790ef4a99ef60ba129
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354264"
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