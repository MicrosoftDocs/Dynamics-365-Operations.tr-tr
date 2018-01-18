---
title: "Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme"
description: "Bu konu, satış siparişi başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme

[!include[banner](../includes/banner.md)]

Bu konu, satış siparişi başlıkları ve satırlarını Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan Microsoft Dynamics 365 for Sales'a eşitlemek için altta yatan görevleri ve şablonları açıklar. 

## <a name="template-and-tasks"></a>Şablon ve görevler

Aşağıdaki şablonlar ve altta yatan görevler, satış siparişi başlıklarını ve satırlarını Finance to Operations'tan Sales'a eşitlemekte kullanılır:

- **Veri tümleştirmesindeki şablonun adı** 

    - Satış Siparişleri (Fin and Ops'tan Sales'a)
    
- **Veri tümleştirme projesindeki görevlerin adları**

    - OrderHeader
    - OrderLine

Satış faturası başlığı ve satırları eşitlemesinden önce gerekli eşitleme görevleri:

- Ürünler (Fin and Ops'tan Sales'a)
- Hesaplar (Sales'tan Fin and Ops'a) (kullanılıyorsa)
- İlgili kişiden Müşterilere (Sales'tan Fin and Ops'a) (kullanılıyorsa)

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations |    Ortak Veri Servisi (CDS)         |     Satış      |
|------------------------|----------------|----------------|
| CDS satışları sipariş başlıkları| SalesOrder     | SalesOrders |
| CDS satış siparişi satırları  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Varlık akışı

Finance and Operations'ta oluşturulmuş ve Sales'a eşitlenmiş satış siparişleri.

Şablondaki filtreler yalnızca ilgili satış siparişlerinin eşitlemeye dahil edilmesini sağlar:

- Satış siparişinde, Sales'tan gelen hem sipariş hem de faturalama müşterisi eşitlemeye dahil edilecektir. Finance and Operations içerisinde **OrderingCustomerIsExternallyMaintained** ve **InvoiceCustomerIsExternallyMaintained** alanları veri varlıkları içindeki eşitlemeyi izlemek için kullanılır.

- Finance and Operations içindeki **Satış siparişi**'nin onaylanması gerekir. Yalnızca onaylanmış satış siparişleri veya daha yüksek işleme durumuna sahip satış siparişler, örneğin Sevk edilen veya Faturalanan durumlar, Sales'a eşitlenir.

- Bir satış siparişi oluşturduktan veya değiştirdikten sonra, Finance and Operations'daki **Satış toplamlarını hesapla** toplu işinin yürütülmesi gerekir. Yalnızca satış toplamları hesaplanmış satış siparişleri CDS ve Sales'a eşitlenecektir.

> [!NOTE]
> **Satış siparişi başlığı** üzerindeki masraflarla ilişkili vergiler, şu anda Finance and Operations'tan Sales'a eşitlemeye dahil değildir. Bu, Sales vergi bilgisini başlık düzeyinde desteklemediği içindir. Satır düzeyi giderleri ile ilgili vergiler dahildir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yeni alanlar **Sipariş** varlığına eklenir ve sayfada görüntülenir:

- **Harici olarak tutuluyor** - Sipariş Finance and Operations'tan geliyorsa **Evet** olarak ayarlanmıştır.

- **İşleme durumu** - Siparişin Finance and Operations içerisinde işleme durumunu göstermek için kullanılır. Değerler şunlardır:

    - Etkin
    - Onaylandı
    - Sevk İrsaliyesi
    - Faturalanan
    - Malzeme çekildi
    - Kısmen Çekildi
    - Kısmen Paketlendi
    - Sevk Edildi
    - Kısmen Sevk Edildi
    - Kısmen Faturalandı
    - İptal edildi

**Yalnızca Dışarıda Tutulan Ürünlere Sahip** ayarı, diğer satış siparişi senaryolarında (Sales'tan Finance and Operations'a eşitleme), satış siparişinin tümüyle **Dışarıda Tutulan Ürünler**'den mi oluştuğunu izlemek için kullanılır; bu durumda ürünler Finance and Operations'ta tutulur. Bu Finance and Operations tarafından bilenmeyen ürünlerin satış siparişi satırlarını eşitlemeye çalışmamanızı garanti etmeye yardımcı olur.
 
**Satış siparişi** sayfasındaki **Fatura Oluştur**, **Siparişi İptal Et**, **Yeniden hesapla**, **Ürünleri Al** ve **Arama Adresi** düğmeleri, dışarıda tutulan siparişler için gizlenmiştir çünkü faturalar Finance and Operations içerisinde oluşturulacak ve Sales'a eşitlenecektir. Sipariş sayfası düzenlenemez çünkü satış siparişi bilgisi Finance and Operations'tan eşitlenecektir.
 
**Satış siparişi durumu**, Finance and Operations'tan gelen değişikliklerin Sales içerisinde **Satış siparişi** içine aktığından emin olunması için etkin kalacaktır. Bu, varsayılan **Statecode [Durum]**'u Veri tümleştirme projesinde **Etkin** olarak ayarlayarak denetlenir.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu 

Satış siparişlerini eşitlemeden önce, sistemleri aşağıdaki ayarla güncelleştirmek önemlidir:

### <a name="setup-in-sales"></a>Sales içinde kurulum

- Kullanıcının atanmış olduğu (Sales **Bağlantı kümesi**'nizden) ekip için izinlerden emin olun. Demo verisi kullanıyorsanız genellikle kullanıcı yönetici erişimine sahiptir, ancak takım değil. Bu olmadan, projeyi Veri tümleştiriciden çalıştırırken Asıl ekibin eksik olduğu hatası alırsınız. 

    - **Ayarlar** > **Güvenlik** > **Ekipler** altında, ilgili ekibi seçin **Rolleri Yönet**'e tıklayın ve istenilen izinlere sahip bir rolü seçin; örn. Sistem Yöneticisi.

- **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **Sistem fiyatlama hesaplama sistemini kullan**'ın **Evet** olarak ayarlandığından emin olun. 

- **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altında, **İndirim hesaplama yöntemi**'nin **Satır maddesi** olarak ayarlandığından emin olun. 

### <a name="setup-in-finance-and-operations"></a>Finance and Operations'ta kurulum

**Satış ve pazarlama** > **Periyodik görevler** > **Satış toplamlarını hesapla**'yı bir toplu iş olarak çalışmak üzere, **Satış siparişleri için toplamları hesapla**'yı **Evet** olarak ayarlamış şekilde ayarlayın. Bu, yalnızca satış toplamları hesaplanmış satış siparişleri CDS ve Sales'a eşitleneceği için önemlidir. Toplu işin sıklığı, satış siparişi eşitlemesinin sıklığı ile uyumlu hale getirilmiş olmalıdır.

### <a name="setup-in-the-data-integration-project"></a>Veri tümleştirme projesinde kurulum

#### <a name="salesheader-task"></a>SalesHeader görevi

- **Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir.

    - **Account_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    - **InvoiceAccount_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    - **Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.

- İhtiyaç duyulan eşleşmenin **Kaynak** > **InvoiceCountryRegionId üzerinden BillingAddress_Country üzerine için CDS** ve **DeliveryCountryRegionId üzerinden DeliveryAddress_Country üzerine** için mevcut olduğundan emin olun.

    - Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.

- **Fiyat listesi** Sales içerisinde siparişleri oluşturmak için gereklidir. **ValueMap**'i **CDS** > **Hedef**'i **pricelevelid.name [Fiyat Listesi Adı]** için **Fiyat listesi**'ne, Sales'ta para birimi başına kullanılmak üzere güncelleştirin. İster varsayılan **Fiyat listesi**'ni tek bir para birimi için kullanabilir veya birden fazla para biriminde **Fiyat listeleri** mevcutsa **ValueMap** kullanabilirsiniz.
    
    - **pricelevelid.name [Fiyat Listesi Adı]** için varsayılan şablon CRM Service USA (örnek)'tir. 

#### <a name="salesline-task"></a>SalesLine görevi

- **Kaynakta CDS Kuruluş Kodu** > **CDS** için eşleşmeyi güncelleştir. 
    
    - **SalesOrder_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.
    - **Product_Organization_OrganizationId** için varsayılan şablon değeri ORG001'dir.

- Gerekli eşleşmenin **Kaynak** > **CDS** içerisinde, **DeliveryCountryRegionId** üzerinden **DeliveryAddress_Country** üzerine için mevcut olduğundan emin olun.

    - Şablon değeri, eşlenmiş ülkelerin sayısı ile **ValueMap**'dir.
    
- Finance and Operations içerisinde **SalesUnitSymbol** için gereken **ValueMap**'in **Kaynak** > **CDS eşleme** içinde mevcut olduğundan emin olun.

    - **ValueMap** ile şablon değeri **SalesUnitSymbol to Quantity_UOM** için tanımlanmıştır.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerin parçası değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

### <a name="orderheader"></a>OrderHeader

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki şablon eşleme](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>İlgili konular

[Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme](products-template-mapping.md)

[Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping.md)

[Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping.md)

[Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme](sales-quotation-template-mapping.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme](sales-invoice-template-mapping.md)


