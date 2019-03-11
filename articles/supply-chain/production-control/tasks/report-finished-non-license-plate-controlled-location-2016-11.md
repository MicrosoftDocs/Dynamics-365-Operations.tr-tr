---
title: Plaka kontrollü olmayan bir konuma tamamlandı olarak rapor etme (Uygulama, Mayıs 2016)
description: Bu görev kılavuzunda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344559"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a>Plaka kontrollü olmayan bir konuma tamamlandı olarak rapor etme (Uygulama, Mayıs 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir. Geçerli bir iş politikasının olması bu görev için bir ön koşuldur. Önceki görev kılavuzunda iş politikasının kurulumu gösterilmiştir. Bu görev kılavuzu Dynamics AX uygulama 7.0.1 veya sonrasını gerektirir.




## <a name="set-up-an-output-location"></a>Bir çıkış konumu ayarlama
1. Organizasyon yönetimi > Kaynaklar > Kaynak grupları öğesine gidin.
2. Listeden '5102' kaynak grubunu seçin.
3. Düzenle'yi tıklatın.
4. Çıkış ambarı alanına '51' girin.
5. Çıkış konumu alanına '001' girin.
    * Konum 001, plaka kontrollü bir konum değildir. Konum için geçerli bir çalışma politikası bulunuyorsa sadece, plaka dışı bir çıkış konumu ayarlayabilirsiniz.  

## <a name="create-a-production-order-and-report-it-as-finished"></a>Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin
1. Sayfayı kapatın.
2. Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.
3. Yeni üretim emri'ne tıklayın.
4. Madde numarası alanına 'L0101' girin.
5. Oluştur öğesine tıklayın.
6. Eylem Bölmesinde Üretime emri'ne tıklayın.
7. Tahmin seçeneğine tıklayın.
8. Tamam'ı tıklatın.
9. Başlat'a tıklayın.
10. Genel sekmesini tıklatın.
11. Otomatik malzeme listesi tüketimi alanında, 'Hiçbir zaman' seçin.
12. Tamam'ı tıklatın.
13. Tamamlandı olarak bildir'i tıklatın.
14. Genel sekmesini tıklatın.
15. Kabul hatası alanında Evet'i seçin.
16. Tamam'ı tıklatın.
17. Eylem Bölmesinde, Ambar öğesine tıklayın.
18. İş ayrıntıları öğesine tıklayın.
    * Üretim emri, tamamlandı olarak rapor edilmişse, hiçbir iş üretilmez. Bu durum, Ürün L0101, konum 001'e bitirildi olarak rapor edildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş politikası bulunmasından kaynaklanır.  

