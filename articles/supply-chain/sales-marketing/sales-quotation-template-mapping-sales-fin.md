---
title: "Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme"
description: "Bu konu, satış teklifi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales'den Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.contentlocale: tr-tr
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Sales'deki satış teklifi başlıklarını ve satırlarını doğrudan Finance and Operations'la eşitleme

[!include [banner](../includes/banner.md)]

Bu konu, satış teklifi başlıkları ve satırlarını doğrudan Microsoft Dynamics 365 for Sales'den Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için temel görevleri ve şablonları açıklar.

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Uygulamalar için Common Data Service'e veri tümleştirme](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmanız gerekir.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri tümleştirme özelliğiyle birlikte kullanılan Müşteri adayından nakde şablonları Finance and Operations ile Sales arasında hesaplar, ürünler, satışlar, satış teklifleri, satış siparişleri ve satış faturaları için veri akışı sağlar. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve altta yatan görevler, teklif başlıklarını ve satırlarını doğrudan Sales'tan Finance and Operations'a eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Satış Teklifleri (Sales'ten Fin and Ops'a) - Doğrudan
- **Veri tümleştirme projesindeki görevlerin adları:**

    - QuoteHeader
    - QuoteLine

Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Fin and Ops'tan Sales'a) - Doğrudan
- Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)
- İlgili kişilerden Müşterilere (Sales'tan Fin and Ops'a) - Doğrudan (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Satış        | Finance and Operations     |
|--------------|----------------------------|
| Alıntılar       | CDS satış teklifi başlığı |
| QuoteDetails | CDS satış teklifi satırları  |

## <a name="entity-flow"></a>Varlık akışı

Sales'ta oluşturulmuş ve Finance and Operations'a eşitlenmiş satış teklifleri.

Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:

- Satış teklifindeki tüm teklif ürünleri harici olarak tutuluyor.
- **Teklifi etkinleştir**'i tıkladıktan sonra, satış teklifi etkindir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yalnızca **Dışarıda Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için **Teklif** varlığına eklenmiştir. Bir satış teklifi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta tutulur. Bu davranış, Finance and Operations tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Satış teklifindeki tüm teklif ürünleri, satış teklifi başlığından **Yalnızca Dışarıda Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir. Bu bilgi, **QuoteDetails** varlığındaki **Teklif Yalnızca Dışarıda Tutulan Ürünlere Sahip** alanında bulunur.

Teklif ürününe bir iskonto eklenebilir ve Finance and Operations'a eşitlenir. Başlıktaki **İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'taki bir ayar tarafından denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları korunur ve Finance and Operations tarafından işlenir.

Sales'ta, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Finance and Operations'a eşitlenmez:

- Satış teklifi başlığındaki salt okunur alanlar: **İskonto %**, **İskonto** ve **Navlun Tutarı**
- Teklif ürünlerindeki salt okunur alanlar: **Vergi**

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış tekliflerini eşitlemeden önce, sistemlerde aşağıdaki ayarları güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- Kullanıcının atanmış olduğu (Sales'taki bağlantı kümenizden) ekip için izinlerin ayarlandığından emin olun. Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım yönetici erişimine sahip değildir. Projeyi veri tümleştirmeden çalıştırdığınızda ekip yönetici erişimine sahip değilse, Ana ekibin eksik olduğunu belirten bir hata iletisi alırsınız.

    Ekip için izinleri ayarlamak üzere **Ayarlar** &gt; **Güvenlik** &gt; **Ekipler**'e gidin ve ilgili ekibi seçin. **Rolleri Yönet**'i seçin ve ardından **Sistem Yöneticisi** gibi istenen izinlere sahip bir rol seçin.

- **Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Sales**'a gidin ve aşağıdaki ayarların kullanıldığından emin olun:

    - **Sistem fiyatlama hesaplama sistemini kullan** seçeneği **Evet** olarak ayarlanmalıdır.
    - **İndirim hesaplama yöntemi** alanı **Satır maddesi** olarak ayarlanmalıdır.

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="quoteheader"></a>QuoteHeader

- **Shipto\_country** ile **DeliveryAddressCountryRegionISOCode** arasında gerekli eşleştirmenin mevcut olduğundan emin olun. Değer eşlemesinde, değer boş bırakılırsa kullanılacak olan bir varsayılan değer tanımlayabilirsiniz. Sol tarafı boş bırakmanız ve sağ tarafı istenen ülkeye veya bölgeye ayarlamanız yeterlidir. Bu şekilde, ulusal siparişler için ülke veya bölge yazmanız gerekmez.

    Şablon değeri çeşitli ülkelerin veya bölgelerin eşleştirildiği bir değer eşlemesidir ve boş değer **ABD** değerine eşittir.

#### <a name="quoteline"></a>QuoteLine

- Finance and Operations'da **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.
- Gerekli birimlerin Sales'ta tanımlandığından emin olun.

    Bir değer eşlemesi bulunan şablon değeri **oumid.name** için **SalesUnitSymbol** olarak tanımlanır.

- İsteğe bağlı: Aşağıdaki eşleşmeleri satış teklifi satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Finance and Operations'a aktarılmasını garanti etmeye yardımcı olmak amacıyla ekleyebilirsiniz:

    - **SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. **SiteId** için varsayılan şablon değeri yoktur.
    - **WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. **WarehouseId** için varsayılan şablon değeri yoktur.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> - **İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Finance and Operations tarafından işlenir.
> - **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

### <a name="quoteheader"></a>QuoteHeader

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)


