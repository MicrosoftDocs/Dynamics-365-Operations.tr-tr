---
title: Satış teklifi başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitleme
description: Bu makale, satış teklifi başlıklarını ve satırlarını Dynamics 365 Sales'ten Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 440b0a6fd2d297027cf3cab548c611544450269a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854137"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Satış teklifi başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitleme

[!include [banner](../includes/banner.md)]



Bu makale, satış teklifi başlıklarını ve satırlarını Dynamics 365 Sales'ten Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan temel görevleri ve şablonları açıklamaktadır.

> [!NOTE]
> Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliğiyle kullanılabilecek Aday müşteriden nakde şablonları; hesaplar, ilgili kişiler, ürünler, satış teklifleri, satış siparişleri ve satış faturaları için Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablon ve temel görevler, teklif başlıklarını ve satırlarını Sales'ten Supply Chain Management'a doğrudan eşitlemede kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Satış Teklifleri (Sales'ten Supply Chain Management'a) - Doğrudan
- **Veri tümleştirme projesindeki görevlerin adları:**

    - QuoteHeader
    - QuoteLine

Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Supply Chain Management'tan Sales'e) - Doğrudan
- Hesaplar (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)
- İlgili kişilerden Müşterilere (Sales'ten Supply Chain Management'a) - Doğrudan (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Satışlar        | Supply Chain Management     |
|--------------|----------------------------|
| Alıntılar       | Dataverse satış teklifi başlığı |
| QuoteDetails | Dataverse satış teklifi satırları  |

## <a name="entity-flow"></a>Varlık akışı

Satış teklifleri Sales'te oluşturulur ve Supply Chain Management'a eşitlenir.

Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:

- Satış teklifindeki tüm teklif ürünleri harici olarak tutuluyor.
- **Teklifi etkinleştir**'i tıkladıktan sonra, satış teklifi etkindir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yalnızca **Dışarıda Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için **Teklif** varlığına eklenmiştir. Bir satış teklifinde yalnızca harici tutulan ürünler varsa ürünler Supply Chain Management'ta tutulur. Bu davranış, Supply Chain Management tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Satış teklifindeki tüm teklif ürünleri, satış teklifi başlığından **Yalnızca Dışarıda Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir. Bu bilgi, **QuoteDetails** varlığındaki **Teklif Yalnızca Dışarıda Tutulan Ürünlere Sahip** alanında bulunur.

Teklif ürününe bir iskonto eklenebilir ve Supply Chain Management'a eşitlenir. Başlıktaki **İskonto**, **Masraflar** ve **Vergi** alanları Supply Chain Management'taki bir ayar tarafından denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları korunur ve Supply Chain Management'ta işlenir.

Sales'te, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Supply Chain Management'a eşitlenmez:

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

- Supply Chain Management'ta **SalesUnitSymbol** için gerekli değer eşlemesinin mevcut olduğundan emin olun.
- Gerekli birimlerin Sales'ta tanımlandığından emin olun.

    Bir değer eşlemesi bulunan şablon değeri **oumid.name** için **SalesUnitSymbol** olarak tanımlanır.

- İsteğe bağlı: Aşağıdaki eşleşmeleri satış teklifi satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Supply Chain Management'a aktarılmasını garanti etmeye yardımcı olmak amacıyla ekleyebilirsiniz:

    - **SiteId** - Supply Chain Management'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. **SiteId** için varsayılan şablon değeri yoktur.
    - **WarehouseId** - Supply Chain Management'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. **WarehouseId** için varsayılan şablon değeri yoktur.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> - **İskonto**, **Masraflar** ve **Vergi** alanları Supply Chain Management'taki karmaşık bir ayar tarafından denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Supply Chain Management tarafından işlenir.
> - **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

### <a name="quoteheader"></a>QuoteHeader

![Veri tümleştirici içerisinde şablon eşleme, QuoteHeader.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Veri tümleştirici içerisinde şablon eşleme, QuoteLine.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-articles"></a>İlgili makaleler

[Aday müşteriden nakde](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]