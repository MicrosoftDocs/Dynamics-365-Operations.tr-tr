--- 
title: "Satış teklifleri oluşturma ve düzenleme"
description: "Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5dcf7d2b5e5d5397c51c51223abe95f9d4911b4f
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-edit-sales-quotations"></a>Satış teklifleri oluşturma ve düzenleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir. Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.


## <a name="create-a-sales-quotation"></a>Satış teklifi oluşturma
1. Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Hesap türü alanında Aday müşteri'yi seçin.
4. Aday müşteri alanında bir değer girin veya bir değer seçin.
5. Genel bölümünü genişletin.
    * Satış ve Pazarlama alanında bir teklif oluşturmayı seçtiğinizden, tür otomatik olarak Satış teklifi olarak ayarlanır. Bir projeye ilişkin teklif oluşturmak için Proje yönetimi ve muhasebe modülünden projeye erişmeniz gerekir.   
6. Tamam'a tıklayın.
    * Teklif satırlarındaki alanlar ve eylemler satış siparişi satırlarındakilere çok benzerdir.   Satış siparişleri gibi teklifler de belirli bir ürün için oluşturulabilir. Ayrıca, ürün kodu bilinmiyorsa veya teklif oluşturma sırasında yoksa, teklifler bir satış kategorisi için de oluşturulabilir.  
7. Ürün alanında bir değer girin veya bir değer seçin.
8. Ürün alanında bir değer yazın.
9. Sayfayı kapatın.
10. Miktar alanına bir sayı girin.
    * Satırda seçilen ürüne ilişkin geçerli ticari anlaşmalar varsa, uygun fiyat ve iskontolar teklif satırına otomatik olarak kopyalanır. Birim fiyat alanında bir değer bulunduğundan emin olun ve istiyorsanız iskonto değerleri girin.  
11. Kaydet'e tıklayın.
12. Eylem Bölmesinde, Satış teklifi öğesine tıklayın.
13. Toplamlar öğesine tıklayın.
14. Tamam'a tıklayın.
15. Satış teklifi satırına tıklayın.
16. Fiyatlar öğesine tıklayın.
    * Fiyat benzetimi çalıştır sayfasında istenen birim fiyatı, iskonto tutarı, iskonto yüzdesi, toplam tutarı, marjı veya katkı oranı temelinde teklifin beklenen gelirini ve kârlılığını ayarlayarak deneme yapabilirsiniz.   Hedef rakamlar istediğiniz seviyeye geldiğinde öneriyi teklif satırına uygulayın, ardından fiyat ile ilgili alanları buna göre güncelleştirilir.  
    * İstediğiniz sayıda fiyat benzetimi oluşturabilirsiniz. Yeni'yi tıklattığınızda, geçerli teklif satırındaki fiyat koşulları sayfaya kopyalanır. Daha sonra fiyat ile ilgili herhangi bir alanda değerleri değiştirebilirsiniz. Alanlardan birinde yapılan değişiklik tüm diğer alanlarda yeniden hesaplama yapılmasını tetikler. Sistemin satış marjının ve katkı oranının hesaplanabilmesi için ürünün birim maliyeti bilinmelidir. Orijinal fiyatların, önerilen fiyatların ve teklif toplamlarına etkisinin ayrıntılı bir görünümü için Benzetimli fiyatlar sekmesini kullanın.   Genel bir kural olarak, yeni bir tutar ayarlayan bir benzetim teklif satırına uygulandığında sistem yeniden hesaplama yapar ve Birim fiyat alanında yeni bir değer girer. Benzetim yeni bir marjı veya katkı oranını esas alıyorsa, yalnızca Net Tutar alanı güncelleştirilir ve Birim fiyat boş bırakılır. Her iki durumda da, benzetimden önce teklif satırında bulunan tüm iskontolar silinir.  
17. Sayfayı kapatın.
18. Eylem Bölmesinde Teklif öğesine tıklayın.
19. Teklifi gönder öğesine tıklayın.
20. Teklifi yazdır alanında Evet'i seçin.
21. Tamam'a tıklayın.
    * Raporun oluşturulması bir dakika kadar sürebilir. Oluşturulana kadar sayfayı kapatmayın.  
22. Sayfayı kapatın.

## <a name="update-a-sales-quotation"></a>Satış teklifini güncelleştirme
1. Eylem Bölmesinde İzle öğesine tıklayın.
2. Müşteriye dönüştür'ü tıklatın.
3. Müşteri hesabı alanına bir değer girin.
4. Denetle'yi tıklatın.
    * Yazdığınız hesap numarasının kullanılabileceğini belirten bir ileti gördüğünüzden emin olun.  
5. Tamam'a tıklayın.
    * Sistem, teklifteki aday müşteri için yeni bir müşteri hesabı oluşturmuştur.  
6. Sayfayı kapatın.
7. Eylem Bölmesinde İzle öğesine tıklayın.
8. Onayla seçeneğine tıklayın.
9. Neden alanında bir değer girin veya bir değer seçin.
10. Tamam'a tıklayın.
11. Eylem Bölmesinde, Genel öğesine tıklayın.
12. Satış siparişleri öğesine tıklayın.
13. Sayfayı kapatın.

