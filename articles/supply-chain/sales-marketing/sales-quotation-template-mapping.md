---
title: "Sales'teki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme"
description: "Bu konu, satış teklif başlıkları ve satırlarını Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Sales'teki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun. 

Bu konu, satış teklif başlıkları ve satırlarını Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar. 

## <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablonlar ve altta yatan görevler, teklif başlıklarını ve satırlarını Sales'tan Finance to Operations'a eşitlemekte kullanılır:

- **Şablonun adı:** Satış Teklifleri (Sales'tan Fin and Ops'a)
- **Projedeki görevlerin adları:**

    - QuoteHeader
    - QuoteLine

Aşağıdaki eşitleme görevleri, satış teklifi başlıkları ve satırlarının eşitlemesi gerçekleşebilmeden önce gereklidir.

- Ürünler (Fin and Ops'tan Sales'a)
- Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)
- İlgili kişiden Müşterilere (Sales'tan Fin and Ops'a) (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Satış        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Alıntılar       | Teklif     | Satış teklifi başlıkları   |
| QuoteDetails | QuotationLine | CDS satış teklifi satırları |

## <a name="entity-flow"></a>Varlık akışı

Sales'ta oluşturulmuş ve Finance and Operations'a eşitlenmiş satış teklifleri.

Sales'taki satış teklifleri, yalnızca aşağıdaki koşullar gerçekleşirse eşitlenir:

- Satış teklifi satırlarındaki tüm ürünler harici olarak yönetiliyor.
- Satış teklifi etkin veya devre dışı.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

**Yalnızca Harici Tutulan Ürünleri Var** alanı, satış teklifinin tümüyle harici tutulan ürünlerden oluşup oluşmadığını istikrarlı bir şekilde izlemek için Teklif varlığına eklenmiştir. Bir satış teklifi yalnızca harici tutulan ürünlere sahipse, ürünler Finance and Operations'ta tutulur. Bu davranış, Finance and Operations tarafından bilenmeyen ürünlerin satış teklifi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.

Teklif üzerindeki tüm satırlar ve ürünler, teklif başlığından **Yalnızca Harici Tutulan Ürünlere Sahip** bilgisi ile güncelleştirilir. Bu bilgi, Teklif satırı varlığındaki **Teklif Yalnızca Harici Olarak Tutulan Ürünlere Sahip** alanında bulunabilir.

**İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları ana kaydı üretilen ve Finance and Operations tarafından işlenendir.

Sales'ta, çözüm aşağıdaki alanları salt okunur yapar çünkü değerler Finance and Operations'a eşitlenmez:

- **Satış teklifi başlığındaki okunur alanlar:** İskonto % İskonto, Navlun Tutarı
- **Satış teklifi satırlarındaki salt okunur alanlar:** Vergi

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

Satış siparişlerini eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- **Ayarlar** &gt; **Yönetim** &gt; **Sistem ayarları** &gt; **Satışlar**'a gidin ve **İskonto hesaplama yöntemi** alanının **Birim başına** olduğundan emin olun. Bu ayar, Sales'taki satır madde iskontosunun, Finance and Operations'taki ayarla eşleştiğini garanti etmeye yardımcı olur. Aksi taktirde, iskonto Finance and Operations'ta doğru olmayacaktır çünkü Finance and Operations iskontoyu, satır Sales'ta satır başına iskonto olsa da bir birim başına iskonto olarak okuyacaktır.

### <a name="setup-in-finance-and-operations"></a>Finance and Operations'ta kurulum

- **Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri**'ne gidin. **Numara serisi** sekmesinde, satış teklifleri için numara serisini seçin ve **Ayrıntıları görüntüle** üzerine tıklayın. **Genel Kurulum** altında, **El ile** alanını **Evet** olarak ayarlayın.
- **Alacak hesapları** &gt; **Kurulum** &gt; **Alacak hesapları parametreleri**'ne gidin. **Sevkiyatlar** sekmesinde, **Teslimat tarih denetimi** alanına **Hiçbir** olarak ayarlayın. Bu ayar, eşitlemenin satış teklifleri için başarısız olmasını engellemeye yardımcı olur.

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="quoteheader"></a>QuoteHeader

- **İstenen teslimat tarihi** alanı Finance and Operations içinde gereklidir ve eşitleme, bu alan boş bırakılırsa başarısız olacaktır. Bu sorunu önlemek için alan boşsa, **Kaynak &gt; CDS**'den bir varsayılan veri alınır. Tarih, tercih edilen bir değere güncelleştirilmelidir. Şu anda, bugünün tarihini temsil etmek için **Bugün** gibi bir değer giremezsiniz. Belirli bir tarih girmelisiniz. **İstenen teslimat tarihi** için varsayılan şablon değeri **1/1/2020**'dir.
- **Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir. Eşitleme hatalarını önlemek için, Sales'ta bir alan boş bırakılırsa kullanılacak bir varsayılan değer belirtebilirsiniz. Bu varsayılan değer, yerel adresler için **Ülke bölgesi** alanına el ile bir değer girmenize gerek kalmayacağı için yararlıdır. **DeliveryAddressCountryRegionISOCode** için varsayılan bir şablon değeri yoktur.
- **CDS Kuruluş Kodu** için eşleşmeyi **Kaynak &gt; CDS** içerisinde, Kuruluş varlığında **CDS kuruluşu** ile eşleşmesi için güncelleştir:

    - **Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.
    - **Account_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.
    - **InvoiceAccount_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.

#### <a name="quoteline"></a>QuoteLine

- **CDS Kuruluş Kodu** için eşleşmeyi **Kaynak &gt; CDS** içerisinde, Kuruluş varlığında **CDS kuruluşu** ile eşleşmesi için güncelleştir:

    - **Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.
    - **Product_Organization_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.
    - **Quotation_Organization_Organization_OrganizationId** için varsayılan şablon değeri **ORG001**'dir.

- **İstenen teslimat tarihi** alanı Finance and Operations içinde gereklidir ve eşitleme, bu alan boş bırakılırsa başarısız olacaktır. Bu sorunu önlemek için alan boşsa, **Kaynak &gt; CDS**'den bir varsayılan veri alınır. Tarih, tercih edilen bir değere güncelleştirilmelidir. Şu anda, bugünün tarihini temsil etmek için **Bugün** gibi bir değer giremezsiniz. Belirli bir tarih girmelisiniz. **İstenen teslimat tarihi** için varsayılan şablon değeri **1/1/2020**'dir.
- Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten aşağıdaki eşleşmeleri ekleyerek, teklif satırlarının müşteriden veya üründen gelen varsayılan bilgi yoksa Finance and Operations'a içe aktarılmasını garanti etmeye yardımcı olabilirsiniz:

    - **SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. **SiteId** için varsayılan şablon değeri yoktur.
    - **WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. **WarehouseId** için varsayılan şablon değeri yoktur.

- Satış ölçü birimi (UOM) için gerekli değer eşlemesinin Finance and Operations içinde, **Quantity_UOM**'dan **SALESUNITSYMBOL**'a **CDS &gt; Hedef** eşlemesinde mevcut olduğundan emin olun.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> - **İskonto**, **Masraflar** ve **Vergi** alanları Finance and Operations'ta karmaşık bir kurulumda denetlenir. Bu kurulum şu anda hiçbir tümleştirme eşlemesini desteklemiyor. Geçerli tasarımda, **Fiyat**, **İskonto**, **Masraf** ve **Vergi** alanları Finance and Operations tarafından işlenir.
> - **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

### <a name="quoteheader"></a>QuoteHeader

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>İlgili konular

[Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme](products-template-mapping.md)

[Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping.md)

[Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping.md)



