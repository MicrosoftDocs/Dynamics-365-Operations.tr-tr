---
title: Sorun giderme Analitik raporları
description: Bu konu, müşterinin verisindeki değişiklikler müşterinin herhangi bir çalışma alanında görüntülenmediğinde ne yapılacağını açıklar.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114596"
---
# <a name="troubleshoot-analytic-reports"></a>Sorun giderme Analitik raporları

**Çıkış**

Bir müşterinin verisi, müşterinin herhangi bir çalışma alanındaki **Analitik** sekmesinde görüntülenmiyor.

**Nedeni**

Varsayılan olarak Microsoft Power BI raporları, her dört saatte bir yenilenir, Dağıtım ölçüm toplu işine uygun olarak.

**Çözünürlük**

Bu sorun, zamanlama nedeniyle olabilir. Bu adımları izleyerek toplu işi başlatın ve analitik çalışma alanlarını güncelleştirin.

1. **Toplu işler** sayfasını **Sistem yönetimi \> Bağlantılar \> Toplu işler \> Toplu işler**'i açın. Alternatif olarak, aramayı kullanın ve **Toplu işler**'e girin.
1. **Ölçümü dağıt** işini listede bulun.
1. Sayfanın üstünde **Düzenle**'yi seçin ve zamanlanan başlangıç tarihini/saatini, analitikleri geçerli tarihe daha yakın bir zamanda yenileyecek değere ayarlayın.

![Toplu işler](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]