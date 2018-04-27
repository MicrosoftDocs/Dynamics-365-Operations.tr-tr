--- 
title: "Plaka denetimli bir yerleşime tamamlandı olarak raporlama "
description: "Bu görev kılavuzunda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir."
author: ChristianRytt
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 34fac03a0ff3d71a2349b66f8f85e4e124dcd708
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="report-as-finished-to-a-plate-controlled-location"></a>Plaka denetimli bir yerleşime tamamlandı olarak raporlama  

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


