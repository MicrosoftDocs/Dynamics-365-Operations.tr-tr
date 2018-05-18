---
title: "Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme"
description: "Bu konu, İlgili Kişiler (İlgili Kişiler) ve İlgili Kişiler (Müşteriler) varlıklarını Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 021a43c78cec83b23aff5dcc40db1a4be81aefc3
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.

Bu konu, İlgili Kişiler (İlgili Kişiler) ve İlgili Kişiler (Müşteriler) varlıklarını doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablonlar ve altta yatan görevler, İlgili Kişi (Kişiler) varlıklarını Sales'tan Finance to Operations'daki İlgili Kişi (Müşteriler) varlıklarına eşitlemekte kullanılır:

- **Veri tümleştirmesindeki şablonların adları:**

    - İlgili Kişiler (Sales'tan Fin and Ops'a) - Doğrudan
    - İlgili Kişilerden Müşteriye (Sales'tan Fin and Ops'a) - Doğrudan

- **Veri tümleştirme projesindeki görevlerin adları:**

    - İlgili kişiler
    - ContactToCustomer

Aşağıdaki eşitleme görevi ilgili kişi eşitlemesi gerçekleşemeden önce gereklidir: Hesaplar (Sales'tan Fin and Ops'a)

## <a name="entity-sets"></a>Varlık kümeleri

| Satış    | Finance and Operations |
|----------|------------------------|
| İlgili kişiler | CDS İlgili Kişileri           |
| İlgili kişiler | Müşteriler V2           |

## <a name="entity-flow"></a>Varlık akışı

İlgili kişiler Sales içinde yönetilir ve Finance and Operations'a eşitlenir.

Sales'daki bir ilgili kişi, Finance and Operations'taki bir ilgili kişi veya müşteri olabilir. Sales'deki bir ilgili kişinin Finance and Operations'a bir ilgili kişi veya müşteri olarak eşitlenip eşitlenmeyeceğini belirlemek için sistem Sales'de ilgili kişinin aşağıdaki özelliklerine bakar:

- **Finance and Operations içinde bir müşteriye eşitleme:** **Etkin Müşteri** seçeneğinin **Evet** olarak ayarlandığı ilgili kişiler
- **Finance and Operations'da bir ilgili kişiye eşitleme:** **Etkin Müşteri**'nin **Hayır** olarak ayarlandığı ve **Şirket**'in (Ana Firma/İlgili Kişi) bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Yeni bir **Etkin Müşteri** alanı ilgili kişiye eklendi. Bu alan satış etkinliğine sahip ilgili kişileri ve satış etkinliğine sahip olmayan ilgili kişileri ayırmak için kullanılır. **Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip ilgili kişiler için **Evet** olarak ayarlanır. Yalnızca bu ilgili kişiler Finance and Operations'ta müşteriler olarak eşitlenir.

Yeni bir **IsCompanyAnAccount** alanı ilgili kişiye eklendi. Bu alan, bir ilgili kişinin bir **Hesap** türündeki şirkete (ana hesap/ilgili kişi) bağlı olup olmadığını belirtmek için kullanılır. Bu bilgi Finance and Operations'a ilgili kişiler olarak eşitlenecek ilgili kişileri belirlemek için kullanılır.

**İlgili Kişi Numarası** alanı, tümleştirme için doğal ve benzersiz anahtarın ilgili kişiye eklendiğinden emin olmak için eklenmiştir. Yeni bir ilgili kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur. Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**

Sales için tümleştirme çözümü uygulandığında, bir yükseltme komut dosyası **İlgili Kişi Numarası** alanını tüm mevcut ilgili kişiler için daha önce belirtilen numara serisini kullanarak ayarlar. Bir güncelleştirme kodu ayrıca **Etkin Müşteri** alanını, satış etkinliğine sahip tüm ilgili kişiler için **Evet** olarak ayarlar.

## <a name="in-finance-and-operations"></a>Finance and Operations'ta

İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir. Bu özellik, belirli bir ilgili kişinin dışarıda tutulduğunu gösterir. Bu durumda, dışarıda tutulan ilgili kişiler, Sales içerisinde tutulur.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="contact-to-customer"></a>İlgili kişiden müşteriye

- **CustomerGroup**, Finance and Operations içerisinde gereklidir. Eşitleme hatalarının önüne geçmek için, eşlemede bir varsayılan değer belirtebilirsiniz. Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.

    Varsayılan şablon değeri **10**'dur.

- Aşağıdaki eşleşmeleri ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** – Bir varsayılan site, Finance and Operations'taki ürünlerde de tanımlanabilir. Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir.

        **SiteId** için bir şablon değeri tanımlanmamıştır.

    - **WarehouseId** – Bir varsayılan ambar, Finance and Operations'taki ürünlerde de tanımlanabilir. Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir.

        **WarehouseId** için bir şablon değeri tanımlanmamıştır.

    - **LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir.
    
        Varsayılan şablon değeri **tr-tr**'dir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.

### <a name="contact-to-contact"></a>İlgili kişiden ilgili kişiye

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>İlgili kişiden müşteriye

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)

[Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme](products-template-mapping-direct.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)



