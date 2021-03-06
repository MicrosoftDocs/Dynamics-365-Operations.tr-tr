---
title: Kısıtlanmış plan oluşturma
description: Bu konu, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını açıklar.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808028"
---
# <a name="generate-a-constrained-plan"></a>Kısıtlanmış plan oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını açıklar. Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar. 

Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam için üretim planlayıcısına yöneliktir.


## <a name="set-up-a-constrained-plan"></a>Kısıtlı bir plan ayarlayın
1. Giriş sayfasında, **Master planlama** çalışma alanını seçin.
2. Çalışma alanının en sağ ucundaki bağlantı listesinde **Master planlar**'ı seçin.
3. Listede, istenen kaydı bulun ve seçin. Örnek: **StaticPlan**  
4. **Sınırlı kapasite** alanında **Evet**'i seçin.
5. **Sınırlı kapasite zaman dilimi** alanına `30` girin.
6. **Gün cinsinden zaman dilimleri** bölümünü genişletin.
7. **Kapasite** alanında **Evet**'i seçin.
8. **Kapasite planlama zaman dilimi (gün)** alanına bir sayı girin. Örnek: `60`  
9. **Hesaplanan gecikmeler** alanında **Evet**'i seçin.
10. **Gecikme zaman dilimini (gün)** hesapla alanına bir sayı girin. Örnek: `60` 
11. **Hesaplanan gecikmeler** bölümünü genişletin.
12. **Hesaplanan gecikmeyi gereksinim tarihine ekle** alanlarında **Evet**'i seçin.
13. Sayfayı kapatın.

## <a name="create-a-constrained-plan"></a>Sınırlandırılmış bir plan oluşturma
1. **Çalıştır**'ı seçin.
2. **Master plan** alanında, sınırlamalarını ayarladığınız planı girin veya seçin.  
3. **Tamam**'ı seçin.
4. **Planlı siparişler**'i seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]