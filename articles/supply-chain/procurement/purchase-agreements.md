---
title: Satınalma sözleşmeleri
description: Bu makalede, satınalma anlaşmalarıyla ilgili bilgiler verilmektedir. Bir satınalma anlaşması, kuruluşun belirli bir süre içinde birden fazla satınalma siparişi kullanarak, belirli bir miktarda veya tutarda alım yapacağını taahhüt eden bir sözleşmedir. Bu taahhüt karşılığında, alıcıya özel fiyatlar ve iskontolar verilir.
author: GalynaFedorova
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal, PurchLine, AgreementLines
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 188a71ec660787b0b942a3d3bf4967b747c4469f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335900"
---
# <a name="purchase-agreements"></a>Satınalma sözleşmeleri

[!include [banner](../includes/banner.md)]

Bu makalede, satınalma anlaşmalarıyla ilgili bilgiler verilmektedir. Bir satınalma anlaşması, kuruluşun belirli bir süre içinde birden fazla satınalma siparişi kullanarak, belirli bir miktarda veya tutarda alım yapacağını taahhüt eden bir sözleşmedir. Bu taahhüt karşılığında, alıcıya özel fiyatlar ve iskontolar verilir. 

Satınalma sözleşmesi bir belirli bir miktardaki ürüne, belirli bir para birimi tutarındaki ürüne, tedarik kategorisinde bulunan belirli bir para biri miktarındaki ürünlere uygulanabilir. Mevcut herhangi bir ticaret sözleşmesinde belirtilen fiyatlar ve indirimler, satınalma sözleşmesindeki fiyatlar ve indirimler tarafından geçersiz kılınır.  

**Satınalma sözleşmeleri** sayfası üzerinde kuruluşunuz ve satıcılarınız arasında satınalma sözleşmeleri oluşturabilir, uygulayabilir veya takibini yapabilirsiniz. Örneğin, bir satınalma sözleşmesi oluşturduktan sonra doğrudan bunu kullanarak sipariş verebilirsiniz. Her satınalma sözleşmesinin, bu satınalma sözleşmesini oluşturan kişi tarafından belirlenen bir geçerlilik süresi vardır. Satınalma sözleşmesinin teslimat tarihi, geçerlilik dönemine dahil etkili tarihlerde olmalıdır.  

Bir satın alma sözleşmesi oluşturduktan sonra etkili hale gelmeden önce etkinleştirmeniz gerekir. Bir satın alma sözleşmesini etkinleştirmek için set **Sözleşmeyi etkin olarak işaretle** seçeneğinde **Evet**'i seçin. 

Satın alma sözleşmenizin kullanılmasını ve onaylanmasını önlemek için, anlaşma durumunu **kapalı** olarak işaretleyin. Bu değişikliği yaptıktan sonra, durumu istediğiniz zaman **geçerli** olacak şekilde güncelleştirebilirsiniz.

## <a name="responsible-workers-on-purchase-agreements"></a>Satınalma anlaşmalarında sorumlu çalışanlar

Satınalma Sözleşmesi sınıflandırmasındaki birincil sorumlu çalışanını ve ikincil sorumlu çalışanını tanımlayabilirsiniz. Bu değerler, sonuçta elde edilen satın alma sözleşmesi tarafından devralınır. Sorumlu çalışanları satınalma anlaşmasına eklemeniz gerekmez ve satınalma sözleşmesinin kendisi için bir servis talebi bazında doğrudan değiştirilebilir. Birincil sorumlu çalışanı olmadan, ikincil sorumlu çalışanına sahip olmanız gerekmese de, bir sorumlu çalışanını belirtemezsiniz. Hem birincil, hem de ikincil sorumlu çalışanından aynı çalışanı belirtemezsiniz.

> [!IMPORTANT]
> Sorumlu taraf özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.25 itibarıyla özellik varsayılan olarak açıktır. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Satınalma sözleşmesi sorumlu taraf* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="commitment-types"></a>Taahhüt türleri
Satınalma sözleşmesindeki her satır bir şeyi satın almak için bir taahhüttür. Birden fazla satınalma siparişinden satırları taahhüdü yerine getirmek için kullanabilirsiniz. Dört tür taahhüt mevcuttur:

-   **Ürün miktarı taahhüdü** – bir ürünü belirli bir miktarda satın alırsınız.
-   **Ürün değer taahhüdü** – bir ürünü belirli bir para birimi tutarında satın alırsınız.
-   **Ürün kategorisi değer taahhüdü** – bir tedarik kategorisindeki bir ürünü, belirli bir para birimi tutarında satın alırsınız. Tutar bir katalog öğesi madde veya katalog dışı madde için olabilir.
-   **Değer taahhüdü** – herhangi bir tedarik kategorisindeki herhangi bir üründen belirli bir para biri miktarında satın alırsınız.

## <a name="pricing-terms-for-purchase-agreements"></a>Satınalma anlaşmaları için fiyatlandırma koşulları
Fiyatlandırma şartları taahhüdün türüne bağlı olarak değişebilir. Satınalma sözleşmesindeki fiyatlandırma şartları, ticaret sözleşmelerinde ayarlanan diğer tüm fiyatlandırma şartlarını geçersiz kılar. Aşağıdaki tablo her bir taahhüt türü tarafından etkilenen fiyat ile ilgili alanları açıklar. **Evet** ibaresini içeren alanlar bir sipariş satırında güncelleştirilebilirler.

| Taahhüt türü                   | Birim fiyat | Fiyat birimi | İskonto yüzdesi | Nakit iskontosu tutarı |
|-----------------------------------|------------|------------|------------------|----------------------|
| Ürün miktarı taahhüdü       | Evet        | Evet        | Evet              | Evet                  |
| Ürün değeri taahhüdü          |            |            | Evet              |                      |
| Ürün kategorisi değer taahhüdü |            |            | Evet              |                      |
| Değer taahhüdü                  |            |            | Evet              |                      |

## <a name="policies-for-purchase-agreements"></a>Satınalma sözleşmeler için ilkeler
Aşağıdaki ilkeler, satınalma sözleşmesi taahhüdü ve buna karşılık gelen satınalma siparişi satırlarının arasındaki bağlantının nasıl çalıştığını etkiler.

-   **Maksimum uygulanır** – tüm sipariş satırları için toplam miktar ya da tutar ilgili taahhütte belirtilen tutar ya da miktarı geçemez.
-   **Fiyat ve iskonto sabit** – sipariş satırındaki fiyat ve ilgili taahhüt üzerindeki fiyatın aynı olması gerekir. Sipariş satırındaki fiyat değişirse, taahhüde olan bağlantı bozulur. Bağlantı bozulursa, sipariş satırı taahhüdün yerine getirilmesine katkıda bulunmaz.
-   **En düşük ve en yüksek tutar serbest bırakma tutarı** – bir miktar belirtilmişse, sipariş satırının ilgili taahhütten farklı olmasını sebep olacak herhangi bir sipariş satırı değişikliği yaparsanız, bir ileti alırsınız.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Satınalma sözleşmeleri için Karşılama hesaplamaları
Karşılama miktarları ve tutarları **Satınalma anlaşmaları** sayfasının **Karşılama** sekmesi üzerindeki **Satır ayrıntıları** hızlı sekmesinde gösterilir.  

**Karşılama** alanı, taahhüdün yerine getirilmesi için geriye kalan gerekli miktarı ve tutarı gösterir.  

**Anlaşma** alanı, satış anlaşması satırının geçerli olduğu toplam miktarı veya toplam tutarı gösterir.  

Satınalma siparişi satırlarına ve karşılama hesaplamasına katkıda bulunan fatura satırlarına, satırlarda bulunan **İlgili bilgi** eyleminden veya bir satınalma sözleşmesinin başlığından erişebilirsiniz.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Satınalma sözleşmeleri için sürüm ve onay geçmişi
Bir satınalma sözleşmesini teyit ettiğinizde bu satınalma sözleşmenin geçerli sürümü, geçmiş tablosunda depolanır. Satın alma sözleşmesini değiştirirseniz, geçmişini satınalma sözleşmesinin başka bir sürümünde saklamak için yeniden onaylayabilirsiniz. Bir satınalma anlaşmasını onaylamazsanız, satınalma siparişleri oluşturmak için kullanmaya devam edebilirsiniz. Ancak, satınalma anlaşmasının geçmiş bilgileri saklanmaz. Sözleşmenin tüm sürümlerini yazdırabilir veya önizleyebilirsiniz. Daha sonra onay almak için düzeltmeleri satıcınızla paylaşabilirsiniz.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Satınalma sözleşmelerini sipariş işlemlerinde uygulamak
Bir satınalma siparişi oluşturduğunuzda buna bir satın alma sözleşmesi uygulayabilirsiniz. Ödeme koşulları, teslim koşulları ve teslim adresi gibi anlaşmadan koşullarından gelen bilgiler sonra satınalma siparişi başlığına kopyalanır. Satınalma siparişi, ürünler veya anlaşma kapsamında olan kategoriler için bir veya daha fazla satır içeriyorsa, satınalma sözleşmesindeki fiyatlar ve iskontolar bu satırlar için kullanılır. Sipariş satırı üzerindeki miktar ya da tutar, satınalma sözleşmesindeki taahhüdün yerine getirilmesine katkıda bulunur. Aynı satınalma siparişi hem bir satın alma sözleşmesi için ilişkili olmayan satırlar hem de satın alma sözleşmesi için bir taahhüdü olan satırları içerebilir.  

Bir satınalma sözleşmesini sadece bir satınalma siparişi oluştururken seçebilirsiniz. Satınalma siparişi oluşturulduktan sonra bir satınalma sözleşmesi seçemezsiniz.  
Satınalma siparişlerinin dolaylı olarak oluşturulduğu bazı durumlarda, Supply Chain Management'ın uygun satınalma sözleşmelerini otomatik olarak arayıp aramayacağını kontrol edebilirsiniz. Örneğin bunu planlanan satınalma siparişlerinin kesinleştirmesini yaptığınızda ya da satış siparişlerine dayanan satınalma siparişleri oluşturduğunuzda yapabilirsiniz.

## <a name="matching-policy-on-purchase-agreements"></a>Satınalma sözleşmeleriyle ilgili eşleştirme ilkesi
Satınalma sözleşmesinin başlığında bir satır eşleştirme ilkesi tanımlayabilirsiniz. Bu satır eşleştirme ilkesi, **Borç hesapları parametreleri** sayfasında (**Fiyat ve miktar eşleştirme** hızlı sekmesindeki) **Eşleştirme ilkesini geçersiz kılmaya izin ver** alanı **Şirket ilkesinden daha fazla** olarak ayarlandığında borç hesapları parametrelerini satır eşleştirme ilkesiyle ilişkilendirir. Satınalma sözleşmesine başvuran belgeler; ilgili madde, madde ve satıcı veya kategori satınalma ilkesinde farklı şekilde tanımlanmadıkça satınalma sözleşmesi başlığında tanımlanan satır eşleştirme ilkesini kullanır.

## <a name="purchase-agreements-and-intercompany-trade"></a>Satınalma sözleşmeleri ve şirketlererası ticaret
Şirketlerarası ticaret ilişkileri, farklı tüzel kişilikler arasında olan satıcı hesapları ve müşteri hesapları arasında oluşturulabilir. Taraflardan biri için bir satış siparişi ya da satınalma siparişi oluşturulduğunda, bir şirketlerarası sipariş zinciri oluşturulur. Sipariş zinciri içinde satış siparişi ve satınalma siparişleri uygun tüzel kişilikler içinde oluşturulur.  

Şirketlerarası ticaret taraflarından birisi için bir satınalma sözleşmesi ya da bir satış sözleşmesi oluşturabilirsiniz. Daha sonra diğer tüzel kişilikteki ticaret tarafı için karşılık gelen bir satış sözleşmesi ya da satınalma sözleşmesi oluşturabilirsiniz.  

Şirketlerarası bir satınalma sözleşmesini tek bir tüzel kişilikte kullanan bir şirketlerarası alış satınalma emri oluşturursanız, karşılık gelen şirketlerarası satış sipariş, diğer tüzel kişilikteki karşılık gelen şirketlerarası satış sözleşmesini kullanır. Satış sözleşmesi taahhütlerinin ve satınalma sözleşmelerinin karşılanmaları eşzamanlıdır, aynı şirketlerarası satış siparişleri ve şirketler arası satınalma siparişlerinin eşzamanlı olduğu gibi.

## <a name="financial-dimensions-on-purchase-agreements"></a>Satınalma sözleşmeleri üzerindeki finansal boyutlar
Finansal boyutları belge başlıklarına ve satınalma sözleşmelerinin tekil satırlarına kopyalayabilirsiniz. Sözleşme başlığındaki veya sözleşme satırındaki boyutları değiştirirseniz, bu değişiklik serbest bırakılmış siparişlerin hiçbirini etkilemez fakat yeni siparişlerin tümünü etkiler.

## <a name="additional-resources"></a>Ek kaynaklar

- [Satın alma sözleşmesi oluşturma](tasks/create-purchase-agreement.md)
- [Satın alma siparişi oluştururken satın alma sözleşmesini uygulama](tasks/create-purchase-release-order-purchase-agreement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]