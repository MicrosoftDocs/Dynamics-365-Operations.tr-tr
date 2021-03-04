---
title: Satış sözleşmelerini girme
description: Bu konu, müşterilerinizden birini üzerinde anlaşılan belirli bir zaman zarfı içinde ürün satın alması karşılığında özel indirimlere hak kazanmasını sağlayacak bir satış sözleşmesini nasıl yaratacağınızı açıklar.
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d69f3eaacea641460b407c1456ee50600262fee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439101"
---
# <a name="enter-sales-agreements"></a>Satış sözleşmelerini girme

[!include [banner](../../includes/banner.md)]

Bu konu, müşterilerinizden birini üzerinde anlaşılan belirli bir zaman zarfı içinde ürün satın alması karşılığında özel indirimlere hak kazanmasını sağlayacak bir satış sözleşmesini nasıl yaratacağınızı açıklar. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-sales-agreement-header"></a>Satış sözleşmesi üstbilgisi ayarla
1. Gezinti bölmesinde **Modüller > Satış ve pazarlama > Satış sözleşmeleri > Satış sözleşmeleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Müşteri numarası** alanında, açılır menüden istediğiniz kaydı seçin.
4. **Satış sözleşmesi sınıflandırması** alanında, açılır menüden istediğiniz kaydı seçin.
5. **Genel** bölümünü genişletin.
6. **Varsayılan taahhüt** alanında **Ürün değeri taahhüdü** seçeneğini seçin. Bağlılık türü, anlaşma sözleşmesinin nasıl karşılanacağını tanımlamak için anlaşmaya atanması zorunlu bir ölçüttür. Önceden tanımlanmış bu dört tür, müşteri bağlılık hedefini, bir miktar veya değer olarak ifade edilecek şekilde ayarlamanıza olanak sağlar. Miktar bağlılık türü belirli yalnızca belirli bir ürüne uygulanabilir, ancak değer temelindeki türler belirli ve belirsiz ürünlerin satışında uygulanabilir.  
7. **Bitiş tarihi** alanında, sözleşme süresinin dolmasını istediğiniz ileri bir tarihe ayarlayın.
8. **Tamam**'ı seçin.

## <a name="set-up-product-value-commitment-lines"></a>Ürün değeri taahhüt satırları ayarla
1. **Satır ekle**'yi seçin.
2. **Madde numarası** alanında, açılır menüden istediğiniz kaydı seçin. Anlaşma için seçmiş olduğunuz bağlılık türü, anlaşmanın satırlarına girebileceğiniz bilginin türünü etkiler. Örneğin, değer temelli bir anlaşmada, müşterinin sizden satın alma taahhüdünde bulunduğu malların toplam net tutarını (anlaşılmış olan para biriminde) belirtmeniz gerekir. Bu örnekte, satırdaki **Miktar** ve **Birim** alanları, müşterinin sözleşmede belirli bir değerdeki ürünü satın alması üzerine oluşturmakta olduğunuz için kullanılamaz.   
3. **Net tutar** alanında, müşterinin satın alma taahhüdünde bulunduğu parasal tutarı girin.
4. **İskonto yüzdesi** alanında müşterinin bu sözleşmeye bağlı satış siparişi satırlarında geçerli olacak bir yüzdelik değer girin.
5. **Satır ayrıntıları** bölümünü genişletin.
6. **Maksimum zorunlu** alanında **Evet** seçeneğini seçin.
    - **Maksimum zorunlu** seçimi, taahhüdün tüm satış emri satırlarının toplam tutarının taahhüdün özel fiyatlarının, iskontolarının ve/veya ödeme şartlarının, taahhüt üzerinde belirtilen tutarı aşmaması gerektiği anlamına gelir.  
    - Minimum ve maksimum satış tutarları, seçilen anlaşmayı kullanan her satış emrinde satılması gereken değerlerin aralığını belirler.   
7. **Satış sözleşmesi başlığı** bölümünü genişletin. Sözleşmenin durumu **Yürürlükte** olarak ayarlanmadığı sürece, satış siparişleri sözleşme ile ilişkilendirilemez ve dolayısıyla o anlaşmanın yerine getirilmesine katkıda bulunamaz. Bu aşamada durumu manüel olarak değiştirebilirsiniz. Fakat durum genellikle, anlaşmayı müşteri için onaylamakta olduğunuzda değiştirilir.  
8. Eylem Bölmesinde, **Satış sözleşmesi** öğesine tıklayın.
9. **Onay**'ı seçin. **Sözleşmeyi yürürlükte olarak işaretle** seçeneğinin **Evet** olarak ayarlandığına emin olun.  
10. **Raporu yazdır** alanında **Evet** seçeneğini seçin.
11. **Tamam**'ı seçin.
12. Sayfayı kapatın. Sözleşme şimdi etkindir. Müşterinin siparişlerini, taahhüt edilen hedefe göre mahsup etmek için sözleşmeye bağlamaya başlayabilirsiniz.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]