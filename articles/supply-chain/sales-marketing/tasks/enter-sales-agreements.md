--- 
title: "Satış sözleşmelerini girme"
description: "Bu yöntem, müşterilerinizden birini üzerinde anlaşılan belirli bir zaman zarfı içinde ürün satın alması karşılığında özel indirimlere hak kazanmasını sağlayacak bir satış anlaşmasını nasıl yaratacağınızı gösterir."
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
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a1c4b7623f3409d4474adcd04fb1331b944b9fbb
ms.openlocfilehash: a0d49068d2c6a62bf7912c2fd7cccd53308bd196
ms.contentlocale: tr-tr
ms.lasthandoff: 02/13/2018

---
# <a name="enter-sales-agreements"></a>Satış sözleşmelerini girme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yöntem, müşterilerinizden birini üzerinde anlaşılan belirli bir zaman zarfı içinde ürün satın alması karşılığında özel indirimlere hak kazanmasını sağlayacak bir satış anlaşmasını nasıl yaratacağınızı gösterir. Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.


## <a name="set-up-sales-agreement-header"></a>Satış sözleşmesi üstbilgisi ayarla
1. Sales and marketing > Sales agreements > Sales agreements (Satış ve pazarlama > Satış anlaşmaları > Satış anlaşmaları) menüsüne gidin
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Satış sözleşmeleri sınıflandırması alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Genel bölümünü genişletin.
9. 'Ürün değeri taahhüdü' seçeneğini varsayılan taahhüt alanında seçin.
    * Bağlılık türü, anlaşma sözleşmesinin nasıl karşılanacağını tanımlamak için anlaşmaya atanması zorunlu bir ölçüttür. Önceden tanımlanmış bu dört tür, müşteri bağlılık hedefini, bir miktar veya değer olarak ifade edilecek şekilde ayarlamanıza olanak sağlar. Miktar bağlılık türü belirli yalnızca belirli bir ürüne uygulanabilir, ancak değer temelindeki türler belirli ve belirsiz ürünlerin satışında uygulanabilir.  
10. Sona erme tarihi alanında, Anlaşma süresinin dolmasını istediğiniz ileri bir tarihe ayarlayın.
11. Tamam'a tıklayın.

## <a name="set-up-product-value-commitment-lines"></a>Ürün değeri taahhüt satırları ayarla
1. Satır ekle'ye tıklayın.
2. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
    * Anlaşma için seçmiş olduğunuz bağlılık türü, anlaşmanın satırlarına girebileceğiniz bilginin türünü etkiler. Örneğin, değer temelli bir anlaşmada, müşterinin sizden satın alma taahhüdünde bulunduğu malların toplam net tutarını (anlaşılmış olan para biriminde) belirtmeniz gerekir. Bu örnekte, satırdaki Miktar ve Birim alanları, müşterinin anlaşmada belirli bir değerdeki ürünü satın alması üzerine oluşturmakta olduğunuz için kullanılamaz.   
5. Net tutar alanında, müşterinin satın alma taahhüdünde bulunduğu parasal tutarı girin.
6. İskonto yüzdesi alanında müşterinin bu anlaşmaya bağlı satış siparişi satırlarında geçerli olacak bir yüzdelik değer girin.
7. Satır ayrıntıları bölümünü genişletin.
8. Maksimum zorunlu alanda Evet'i seçin.
    * Maksimum'un Zorlanması seçimi, taahhüdün tüm satış emri satırlarının toplam tutarının taahhüdün özel fiyatlarının, iskontolarının ve/veya ödeme şartlarının, taahhüt üzerinde belirtilen tutarı aşmaması gerektiği anlamına gelir.  
    * Minimum ve maksimum satış tutarları, seçilen anlaşmayı kullanan her satış emrinde satılması gereken değerlerin aralığını belirler.   
9. Satış sözleşmesi üstbilgi bölümünü genişletin.
    * Sözleşmenin durumu Etkili'ye ayarlanmadığı sürece satış emirleri, anlaşma ile ilişkili olamaz ve dolayısıyla bu sözleşmenin yerine getirilmesinde katkıda bulunamaz. Bu aşamada durumu manüel olarak değiştirebilirsiniz. Fakat durum genellikle, anlaşmayı müşteri için onaylamakta olduğunuzda değiştirilir.  
10. Eylem Bölmesinde, Satış anlaşması'nı tıklatın.
11. Onay'a tıklayın
    * Anlaşmanın etkin olması seçeneğinin Evet olarak ayarlandığından emin olun.  
12. Baskı rapor alanında Evet'i seçin.
13. Tamam'a tıklayın.
14. Sayfayı kapatın.
    * Anlaşma şimdi etkindir ve müşterinin siparişlerini, taahhüt edilen hedefe göre mahsup etmek için anlaşmaya bağlamaya başlayabilirsiniz.  


