---
title: Satış sözleşmelerine genel bakış
description: Bu konu, satış sözleşmeleri hakkında bilgiler sağlar. Satış anlaşması, müşterinin özel fiyatlar ve iskontolar karşılığında ürünleri, belirli miktarda veya belirli bir zaman aralığında belirli bir tutarda almasını sağlayan bir sözleşmedir.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage, SalesAgreementInvoiceJournal, SalesAgreementInvoicePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "9554"
- intro-internal
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c36ace4fe61d4f3add7750c66594c0f1060f8127
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694382"
---
# <a name="sales-agreements-overview"></a>Satış sözleşmelerine genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, satış sözleşmeleri hakkında bilgiler sağlar. Satış anlaşması, müşterinin özel fiyatlar ve iskontolar karşılığında ürünleri, belirli miktarda veya belirli bir zaman aralığında belirli bir tutarda almasını sağlayan bir sözleşmedir.

Bir satış anlaşması,müşterinin belirli bir miktarda ya da belirli bir zaman zarfında ürün satın alması karşılığında özel fiyatlar, özel iskontolar ve ödeme ve teslimat koşulları gibi diğer özel koşullara hak kazanmasını sağlayan bir anlaşmadır. Mevcut herhangi bir ticaret anlaşmasındaki belirtilen fiyatlar ve iskontolar, satış anlaşmasındaki fiyatlar ve iskontolar tarafından geçersiz kılınır.  

Bir satış anlaşmasının geçerlilik süresi anlaşma satırındaki **Yürürlük tarihi** ve **Bitiş tarihi** alanları tarafından tanımlanır. Siparişin talep edilen sevk tarihi geçerlilik dönemi içindeyse, bir müşterinin satış siparişi anlaşma koşullarına uygundur. Bir satış anlaşmasına bağlı tüm satış siparişi satırları, satış anlaşmasının yerine getirilmesi için katkıda bulunmaktadır.  

Bir satış siparişini doğrudan satış anlaşmasından **Siparişi serbest bırak** işlemini kullanarak oluşturabilirsiniz. Alternatif olarak, siparişleri çekerken etkili bir satış anlaşması seçebilirsiniz (bu makalenin "Satış anlaşmalarını sipariş işlemlerinde uygulamak" bölümüne bakın).  

> [!NOTE] 
> Önceki sürümlerde, satış sözleşmeleri paket satış siparişleri şeklinde geçer.

## <a name="commitment-types"></a>Taahhüt türleri
Satış anlaşmasındaki her satır bir şeyi satmak için taahhüt niteliğindedir. Genel olarak, iki kategoride taahhüt vardır:

-   **Değer taahhüdü**– Müşteri belirli bir tutarda ürün satın almayı kabul eder.
-   **Miktar taahhüdü**– Müşteri belirli bir miktarda ürün satın almayı kabul eder.

Buna ek olarak, müşterinin belirli bir ürünü veya bir ürün kategorisindeki ürünleri satın almasını bir anlaşmayı onaylayabilirsiniz. Bu iki etken (miktar ile değer ve belirli ürünler ile ürün kategorileri) birleştirilerek dört türde taahhüt ortaya çıkar:

-   **Ürün miktarı taahhüdü** – Müşteri belirli bir miktarda ürün satın almayı kabul eder. Bu bağlılık türünü kullanan satırlar bir ürün numarasıyla ve üzerinde anlaşılan miktar ve birim ile tanımlanır. **Tutar** alanı kullanılamaz.
-   **Ürün değeri taahhüdü** – Müşteri belirli ürünleri belirli bir tutarda satın almayı kabul eder. Bu bağlılık türünü kullanan satırlar bir ürün numarasıyla ve üzerinde anlaşılan miktar ile tanımlanır. **Miktar** ve **Birim** alanları kullanılamaz.
-   **Ürün kategorisi değer taahhüdü** – Müşteri belirli satış kategorilerindeki ürünleri belirli bir tutarda satın almayı kabul eder. Bu bağlılık türünü kullanan satırlar, satış kategorileri hiyerarşisindeki bir satış kategorisiyle ve bir tutar ile tanımlanır. **Miktar** ve **Birim** alanları kullanılamaz.
-   **Değer taahhüdü** – Müşteri herhangi bir tedarik kategorisindeki herhangi bir ürünü veya ürünleri belirli bir tutarda satın almayı kabul eder. **Miktar** ve **Birim** alanları kullanılamaz.

Aynı satış anlaşmasındaki satırlarda farklı türde taahhütler olabilir.

## <a name="pricing-terms-for-sales-agreements"></a>Satış anlaşmaları için fiyatlandırma koşulları
Fiyatlandırma şartları taahhüdün türüne bağlı olarak değişebilir. Bir satış anlaşmasına bağlı bir satış siparişinde, satış anlaşmasındaki fiyatlandırma şartları ticari anlaşmalara dayalı geçerli tüm diğer fiyatlandırma şartlarını geçersiz kılar. Aşağıdaki tablo her bir taahhüt türü tarafından etkilenen fiyat ile ilgili alanları açıklar. Evet", alanın bir sipariş satırında güncellenebileceğini belirtir.

| Taahhüt türü                   | Birim fiyat | Fiyat birimi | İskonto yüzdesi | Nakit iskontosu tutarı |
|-----------------------------------|------------|------------|------------------|----------------------|
| Ürün miktarı taahhüdü       | Evet        | Evet        | Evet              | Evet                  |
| Ürün değeri taahhüdü          |            |            | Evet              |                      |
| Ürün kategorisi değer taahhüdü |            |            | Evet              |                      |
| Değer taahhüdü                  |            |            | Evet              |                      |

## <a name="policies-for-sales-agreements"></a>Satış anlaşması politikaları
Aşağıdaki ilkeler, satış anlaşması taahhüdü ve buna karşılık gelen satış siparişi satırlarının arasındaki bağlantının nasıl çalıştığını etkiler.

-   **Maksimum uygulanır** – tüm sipariş satırları için toplam miktar ya da tutar ilgili taahhütte belirtilen tutar ya da miktarı geçemez.
-   **Fiyat ve iskonto sabit** – Sipariş satırındaki fiyat ve ilgili taahhüt üzerindeki fiyat farklı olamaz. Sipariş satırındaki fiyat değişirse, taahhüde olan bağlantı bozulur. Bağlantı bozulursa, sipariş satırı taahhüdün yerine getirilmesine katkıda bulunmaz.
-   **En düşük serbest bırakma tutarı** ve **en yüksek serbest bırakma tutarı** – Bir miktar belirtilmişse, sipariş satırının ilgili taahhütten farklı olmasını sebep olacak herhangi bir sipariş satırı değişikliği yaparsanız, bir ileti görüntülenir.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Satış anlaşmaları için Karşılama hesaplamaları
**Satış anlaşmaları** sayfasında **Satır ayrıntıları** Hızlı Sekmesindeki **Karşılama** sekmesi karşılama miktarlarını ve tutarlarını gösterir.  

**Karşılama** alanında, belirtilen satış anlaşmasına bağlı tüm siparişlerin toplam miktarlarını ve tutarlarını görüntüleyebilirsiniz. Ayrıca, taahhüdün yerine getirilmesi için geriye kalan gerekli miktar ve tutar gösterilir.  

**Anlaşma** alanında, belirtilen satış anlaşmasındaki miktarları ve tutarları görüntüleyebilirsiniz. Bu miktarlar ve tutarlar taahhüt edilen toplam miktarlar ve tutarlardır.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Satış anlaşmaları için sürüm ve onay geçmişi
Bir satış anlaşmasını onayladığınızda, bu satış anlaşmasının geçerli sürümü geçmiş tablosunda saklanır. Satış anlaşmasını değiştirirseniz, geçmiş alanında satış anlaşmasının başka bir sürümünü saklamak için anlaşmayı yeniden onaylayabilirsiniz.  

Bir satış anlaşmasını onaylamazsanız, satış siparişleri oluşturmak için onu kullanmaya devam edebilirsiniz. Ancak, satış anlaşmasının geçmiş bilgileri saklanmaz.  

Onaylamaların tüm revizyonlarını yazdırabilir veya önizleyebilirsiniz. Daha sonra onay almak için düzeltmeleri müşterinizle paylaşabilirsiniz.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Satış anlaşmalarını sipariş işlemleri sırasında uygulamak
Bir satış sözleşmesi için satış siparişlerini doğrudan serbest bırakmazsanız, bir satış sözleşmesini sipariş girişi işlemi sırasında yine de bir siparişe bağlayabilirsiniz. Yeni bir satış siparişi oluşturuyorsanız ve bir satış anlaşmasını seçtiğinizde, bu anlaşmanın ödeme koşulları, teslimat koşulları ve teslimat adresi gibi şartları sipariş başlığına uygulanır ve anlaşmam ile sipariş arasında bir bağlantı oluşturulur. Sonra, sipariş satırlarında satış anlaşmasında belirtilen ürünleri ve kategorileri seçtiğinizde fiyat ve iskontolar ilgili anlaşmadan kopyalanır. Aynı satış siparişi hem bir satış anlaşmasıyla ilişkili olmayan satırları hem de satış anlaşmasında taahhüt edilen satırları içerebilir.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Satış anlaşmalarına bağlı satış siparişlerini değiştirme
Bir satış anlaşması üzerinden satış siparişi oluşturduysanız (yayınladıysanız), yalnızca ilişkili satış anlaşması satırlarına bağlantıyı kaldırırsanız ilgili satış siparişi satırlarındaki bazı alanlar değiştirilebilir. Aşağıdaki tabloda bu alanların bazıları listelenmiştir.

| Alan                                                             | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Talep edilen sevk tarihi                                               | Talep edilen sevk tarihini satış anlaşması satırındaki **Yürürlük tarihi** değerinden önceki bir tarihe değiştirirseniz, değiştirilen sevk tarihini kaydedebilmek için önce satış anlaşması satırına bağlantıyı kaldırmanız gerekir. Talep edilen sevk tarihini satış anlaşması satırındaki **Bitiş tarihi** değerinden sonraki bir tarihe değiştirirseniz, değiştirilen sevk tarihini kaydedebilmek için önce satış anlaşması satırına bağlantıyı kaldırmanız gerekir. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet amount | Bu alanların herhangi birindeki değeri değiştirirseniz ve ilişkili bir satış anlaşması satırında **Fiyat ve iskonto sabittir** onay kutusu işaretliyse, bir ileti kutusu değişiklikleri kaydetmek isteyip istemediğinizi sorar. Satış sözleşmesi satırına bağlantıyı kaldırmak ve fiyatı yeniden hesaplamak için **Evet**'e tıklayın. Fiyatı yeniden hesaplamanız gerekmeden satış sözleşmesi satırına bağlantıyı kaldırmak için **Hayır**'a tıklayın.                                                                   |
| Net tutar                                                        | **Maksimum uygulanır** onay kutusu seçiliyken bir satış anlaşması satırında belirtilen tutarı aşan bir tutar belirtirseniz, bir ileti kutusu değişen tutarı kaydetmek isteyip istemediğinizi sorar. Satış sözleşmesi satırına bağlantıyı kaldırmak ve fiyatı yeniden hesaplamak için **Evet**'e tıklayın. Fiyatı yeniden hesaplamanız gerekmeden satış sözleşmesi satırına bağlantıyı kaldırmak için **Hayır**'a tıklayın.                                                                 |
| Miktar                                                          | **Maksimum uygulanır** onay kutusu seçiliyken bir satış anlaşması satırında belirtilen miktarı aşan bir miktar belirtirseniz, bir ileti kutusu değişen miktarı kaydetmek isteyip istemediğinizi sorar. Satış sözleşmesi satırına bağlantıyı kaldırmak ve fiyatı yeniden hesaplamak için **Evet**'e tıklayın. Fiyatı yeniden hesaplamanız gerekmeden satış sözleşmesi satırına bağlantıyı kaldırmak için **Hayır**'a tıklayın.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Satış anlaşmasıyla sipariş edilen bir ürünü iade etme
Bir müşteri, bir satış anlaşmasıyla sipariş edilen bir ürünü iade ettiğinde, Supply Chain Management tutar veya miktar değişikliğini yansıtmak üzere ilgili satış anlaşması taahhüdünü bulabilir ve otomatik olarak güncelleyebilir. Bir satış anlaşmasına bağlanmış orijinal satış siparişini temel alan bir iade emri oluşturarak, satış anlaşması taahhüdü, satış siparişi satırı ve iade emri faturası arasında bir ilişki kurarsınız.  

İade edilen ürün miktarını satış anlaşması taahhüdünden düşmek istemiyorsanız, iade emri ve satış anlaşması taahhüdü arasındaki bağlantıyı kaldırmak için **Siparişi iade et** sayfasında **Bağlantıyı kaldır** denetimini kullanabilirsiniz. Bağlantıyı daha sonra yeniden oluşturmak isterseniz, **Bağlantı oluştur**'u tıklatın.  

**Not:** Bir iade emri yalnızca tek bir satış anlaşmasına bağlanabilir. Bir müşteri birden fazla satış anlaşmasından sipariş edilmiş birden çok ürün iade ederse, her bir ürün için yeni bir iade emri oluşturmanız ve ilgili satış anlaşmasına bir bağlantı oluşturmanız gerekir.

## <a name="automatic-search-for-sales-agreements"></a>Satış anlaşmalarını otomatik olarak arama
Bir alacak dekontu veya şirketlerarası satış siparişi oluşturduğunuzdaki gibi satış siparişlerinin dolaylı olarak oluşturulduğu bazı durumlarda sistemi otomatik olarak uygun satış anlaşmalarını arayacak şekilde kontrol edebilirsiniz.

## <a name="financial-dimensions-on-sales-agreements"></a>Satış anlaşmaları üzerindeki finansal boyutlar
Finansal boyutları belge başlıklarına ya da satış anlaşmalarının tekil satırlarına kopyalayabilirsiniz. Herhangi bir zamanda bir anlaşma başlığındaki veya anlaşma satırındaki boyutları değiştirebilirsiniz. Bu durumda, boyutlar otomatik olarak sevk başlığına veya sevk emirlerinin sevk satırlarına kopyalanır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]