---
title: Satış teklifleri oluşturma ve düzenleme
description: Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir.
author: Henrikan
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable, CustQuotationConfirmationJournal, CustQuotationJournal, CustSalesLines, SalesQuotationCopying, SalesQuotationDeleteQuotations, SalesQuotationListPagePreviewPane, SalesQuotationTypeGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c409d294565f89eac95e42f6207573d22859100
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578956"
---
# <a name="create-and-edit-sales-quotations"></a>Satış teklifleri oluşturma ve düzenleme

[!include [banner](../../includes/banner.md)]

Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir. Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.


## <a name="create-a-sales-quotation"></a>Satış teklifi oluşturma
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış teklifleri > Tüm teklifler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **Hesap türü** alanında 'Aday müşteri' seçeneğini seçin.
4. **Aday müşteri** alanında bir değer girin veya bir değer seçin.
5. **Genel** bölümünü genişletin. Satış ve Pazarlama alanında bir teklif oluşturmayı seçtiğinizden, tür otomatik olarak 'Satış teklifi' olarak ayarlanır. Bir projeye ilişkin teklif oluşturmak için **Proje yönetimi ve muhasebe** modülünden projeye erişmeniz gerekir.
6. **Tamam**'a tıklayın. Teklif satırlarındaki alanlar ve eylemler satış siparişi satırlarındakilere çok benzerdir.   Satış siparişleri gibi teklifler de belirli bir ürün için oluşturulabilir. Ayrıca, ürün kodu bilinmiyorsa veya teklif oluşturma sırasında yoksa, teklifler bir satış kategorisi için de oluşturulabilir.     
7. **Madde** alanında bir değer girin veya bir değer seçin.
8. **Tesis** alanına bir değer yazın.
9. **Miktar** alanına bir sayı girin. Satırda seçilen ürüne ilişkin geçerli ticari anlaşmalar varsa, uygun fiyat ve iskontolar teklif satırına otomatik olarak kopyalanır. Birim fiyat alanında bir değer bulunduğundan emin olun ve istiyorsanız iskonto değerleri girin. 
10. **Kaydet**'e tıklayın.
11. **Eylem Bölmesinde**, **Satış teklifi** öğesine tıklayın.
12. **Toplamlar** öğesine tıklayın.
13. **Tamam**'a tıklayın.
14. Satış teklifi satırını seçin.
15. **Eylem Bölmesinde**, **Teklif** öğesine tıklayın.
16. **Fiyat benzetimi**'ne tıklayın.
    - **Fiyat benzetimi çalıştır** sayfasında istenen birim fiyatı, iskonto tutarı, iskonto yüzdesi, toplam tutarı, marjı veya katkı oranı temelinde teklifin beklenen gelirini ve kârlılığını ayarlayarak deneme yapabilirsiniz. Hedef rakamlar istediğiniz seviyeye geldiğinde öneriyi teklif satırına uygulayın, ardından fiyat ile ilgili alanları buna göre güncelleştirilir.  
    - İstediğiniz sayıda fiyat benzetimi oluşturabilirsiniz. **Yeni**'yi tıklattığınızda, geçerli teklif satırındaki fiyat koşulları sayfaya kopyalanır. Daha sonra fiyat ile ilgili herhangi bir alanda değerleri değiştirebilirsiniz. Alanlardan birinde yapılan değişiklik tüm diğer alanlarda yeniden hesaplama yapılmasını tetikler. Sistemin satış marjının ve katkı oranının hesaplanabilmesi için ürünün birim maliyeti bilinmelidir. Orijinal fiyatların, önerilen fiyatların ve teklif toplamlarına etkisinin ayrıntılı bir görünümü için Benzetimli fiyatlar sekmesini kullanın. Genel bir kural olarak, yeni bir tutar ayarlayan bir benzetim teklif satırına uygulandığında sistem yeniden hesaplama yapar ve Birim fiyat alanında yeni bir değer girer. Benzetim yeni bir marjı veya katkı oranını esas alıyorsa, yalnızca Net Tutar alanı güncelleştirilir ve Birim fiyat boş bırakılır. Her iki durumda da, benzetimden önce teklif satırında bulunan tüm iskontolar silinir.
17. **Eylem Bölmesinde**, **Teklif** öğesine tıklayın.
18. **Teklif gönder** öğesine tıklayın.
19. **Teklifi yazdır** alanında 'Evet'i seçin.
20. **Tamam**'a tıklayın. Raporun oluşturulması bir dakika kadar sürebilir. Oluşturulana kadar sayfayı kapatmayın.

## <a name="update-a-sales-quotation"></a>Satış teklifini güncelleştirme
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış teklifleri > Tüm teklifler**'e gidin.
2. **Eylem Bölmesinde** **İzle** öğesine tıklayın.
3. **Müşteriye dönüştür** öğesine tıklayın.
4. **Müşteri hesabı** alanına bir değer girin.
5. **Denetle** öğesine tıklayın. Yazdığınız hesap numarasının kullanılabileceğini belirten bir ileti gördüğünüzden emin olun.  
6. **Tamam**'a tıklayın. Sistem, teklifteki aday müşteri için yeni bir müşteri hesabı oluşturmuştur.  
7. Sayfayı kapatın.
8. **Eylem Bölmesinde** **İzle** öğesine tıklayın.
9. **Onayla**'yı tıklatın.
10. **Neden** alanında bir değer girin veya bir değer seçin.
11. **Tamam**'a tıklayın.
12. **Eylem Bölmesi**'nde, **Genel** öğesine tıklayın.
13. **Satış siparişleri** öğesini tıklayın.
14. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]