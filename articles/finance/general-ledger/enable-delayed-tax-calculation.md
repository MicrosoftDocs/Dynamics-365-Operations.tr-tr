---
title: Günlükte ertelenen vergi hesaplamasını etkinleştirme
description: Bu konu, günlük satırlarının hacmi çok büyük olduğunda vergi hesaplama performansını artırmak için **Günlükte ertlenen vergi hesaplamasını etkinleştir** özelliğinin nasıl kullanılacağını açıklamaktadır.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180302"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a>Günlükte ertelenen vergi hesaplamasını etkinleştirme
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, günlük satırlarının hacmi çok büyük olduğunda vergi hesaplama performansını artırmak için **Günlükte ertlenen vergi hesaplamasını etkinleştir** özelliğinin nasıl kullanılacağını açıklamaktadır.

Günlükteki geçerli satış vergisi hesaplama, kullanıcı vergiyle ilgili alanları güncelleştirdiğinde (satış vergisi grubu/madde satış vergisi grubu gibi) gerçek zamanlı olarak tetiklenen bir davranıştır. Günlük satırı düzeyindeki her güncelleştirme, tüm günlük satırlarındaki vergi tutarını yeniden hesaplar. Kullanıcının gerçek zamanlı hesaplanan vergi tutarını görebilmesine yardımcı olur, ancak günlük satırları hacmi çok büyük olduğunda performans sorununa neden olabilir.

Bu özellik, performans sorununu çözmek için vergi hesaplamasını erteleme seçeneği sunar. Bu özellik açık ise, vergi tutarı yalnızca Kullanıcı "Satış Vergisi" komutunu tıklattığında veya günlüğü deftere naklederken hesaplanır.

Kullanıcı, parametreyi üç düzeyde açıp kapatabilir:
- Tüzel kişiliğe göre
- Günlük adına göre
- Günlük başlığına göre

Sistem, günlük başlığındaki parametre değerini son değer olarak alacaktır. Günlük başlığındaki parametre değeri varsayılan olarak günlük adından alınır. Günlük adı oluşturulduğunda, günlük adının parametre değeri varsayılan olarak genel muhasebe parametresi içinden alınır.

Bu parametre açıksa, günlükteki "Gerçek satış vergisi tutarı" ve "Hesaplanan satış vergisi tutarı" alanları gizlenir. Amaç, kullanıcının vergi hesaplamasını tetiklemeye başlamadan önce bu iki alanın değeri her zaman 0 olarak gösterileceği için kullanıcının kafasını karıştırmamaktır.

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a>Tüzel kişiliğe göre ertelenen vergi hesaplamasını etkinleştir

1. **Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri**'ne gidin.
2. **Satış vergisi** sekmesine tıklayın
3. **Genel** hızlı sekmesi altında **Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a>Günlük adına göre ertelenen vergi hesaplamasını etkinleştirme

1. **Genel muhasebe > Günlük ayarı > Günlük adları**'na gidin.
2. **Genel** hızlı sekmesi altında **Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a>Günlüğe göre ertelenen vergi hesaplamasını etkinleştirme

1. **Genel muhasebe > Günlük girişleri > Genel günlükler**'e gidin
2. **Yeni**'ye tıklayın
3. Bir günlük adı seçin
4. **Kurulum**’a tıklayın
5. **Ertlenen vergi hesaplaması** parametresini bulun, açın/kapatın

![](media/delayed-tax-calculation-journal-header.png)
