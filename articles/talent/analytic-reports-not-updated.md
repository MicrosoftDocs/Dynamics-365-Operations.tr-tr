---
title: Analitik raporları güncelleştirilmedi
description: Bu konu, müşterinin verisindeki değişiklikler müşterinin herhangi bir çalışma alanında görüntülenmediğinde ne yapılacağını açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898585"
---
# <a name="analytic-reports-are-not-updated"></a>Analitik raporları güncelleştirilmedi

**Stok çıkışı**

Bir müşterinin verisi, müşterinin herhangi bir çalışma alanındaki **Analitik** sekmesinde görüntülenmiyor.

**Nedeni**

Varsayılan olarak Microsoft Power BI raporları, her dört saatte bir yenilenir, Dağıtım ölçüm toplu işine uygun olarak.

**Çözünürlük**

Bu sorun, zamanlama nedeniyle olabilir. Bu adımları izleyerek toplu işi başlatın ve analitik çalışma alanlarını güncelleştirin.

1. **Toplu işler** sayfasını **Sistem yönetimi \> Bağlantılar \> Toplu işler \> Toplu işler**'i açın. Alternatif olarak, aramayı kullanın ve **Toplu işler**'e girin.
1. **Ölçümü dağıt** işini listede bulun.
1. Sayfanın üstünde **Düzenle**'yi seçin ve zamanlanan başlangıç tarihini/saatini, analitikleri geçerli tarihe daha yakın bir zamanda yenileyecek değere ayarlayın.

![Toplu işler](media/batch-jobs.png)
