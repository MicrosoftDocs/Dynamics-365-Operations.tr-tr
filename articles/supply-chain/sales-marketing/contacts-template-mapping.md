---
title: "Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme"
description: "Bu konu, İlgili Kişileri (İlgili Kişiler) ve İlgili Kişileri (Müşteriler) Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun. 

Bu konu, İlgili Kişi (İlgili Kişiler) ve İlgili Kişi (Müşteriler) Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Aşağıdaki şablonlar ve altta yatan görevler, İlgili Kişi (Kişiler) ve İlgili Kişiyi (Müşterileri) Sales'tan Finance to Operations'a eşitlemekte kullanılır:

- **Şablonların adları:**

    - İlgili Kişiler (Sales'tan Fin and Ops'a)
    - İlgili kişiden Müşteriye (Sales'tan Fin and Ops'a)

- **Projedeki görevlerin adları:**

    - İlgili kişiler
    - ContactToCustomer

Aşağıdaki eşitleme görevi İlgili kişi eşitlemesinden önce gereklidir: Hesaplar (Sales'tan Fin and Ops'a)

## <a name="entity-sets"></a>Varlık kümeleri

| Satış    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| İlgili kişiler | Başvur | CDS İlgili Kişileri           |
| İlgili kişiler | Hesap | Müşteriler V2           |

## <a name="entity-flow"></a>Varlık akışı

İlgili kişiler Sales'ta yönetilir ve Ortak Veri Hizmeti (CDS) ve Finance and Operations'a eşitlenir.

Sales'daki bir İlgili Kişi, CDS ve Finance and Operations'taki bir İlgili Kişi olabilir. Alternatif olarak, CDS içerisinde bir Hesap ve Finance and Operations'ta bir Müşteri olabilir. Bir ilgili kişinin Sales içinde CDS'ye ve Finance and Operations'a eşitlenmek üzere seçilip seçilmeyeceğini belirlemek için (örneğin, Sales'daki İlgili Kişiler &gt; CDS'de İlgili Kişi &gt; Finance and Operations'daki İlgili Kişiler) sistem Sales'daki İlgili Kişilerde aşağıdaki özelliklere bakar:

- **CDS içinde Hesap'a ve Finance and Operations içinde Müşteri'ye eşitle:** **Etkin Müşteri** **Evet** olarak ayarlandığı İlgili Kişileri
- **CDS içinde İlgili Kişiye ve Finance and Operations'da İlgili Kişiye eşitle:** **Etkin Müşteri**'nin **Hayır** ve **Şirket**'in (Ana Firma/İlgili Kişi) noktalarının bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü 

Yeni bir **Etkin Müşteri** alanı İlgili Kişiye eklendi. Bu alan satış etkinliğine sahip İlgili Kişileri ve satış etkinliğine sahip olmayan İlgili Kişileri ayırmak için kullanılır. **Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip İlgili Kişiler için **Evet** olarak ayarlanır. Yalnızca bu İlgili Kişiler Finance and Operations'ta Müşteriler olarak eşitlenir.

Yeni bir **IsCompanyAnAccount** alanı İlgili Kişiye eklendi. Bu alan, bir İlgili Kişinin bir **Hesap** türündeki Şirkete (Ana Firma/İlgili Kişi) bağlı olup olmadığını belirtmek için kullanılır. Bu bilgi Finance and Operations'a İlgili Kişiler olarak eşitlenecek İlgili Kişileri belirlemek için kullanılır.

**İlgili Kişi Numarası** alanı, tümleştirme için doğal ve benzersiz anahtarın İlgili Kişiye eklendiğinden emin olmak için eklenmiştir. Yeni bir İlgili Kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur. Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**

Sales için tümleştirme çözümü Sales'a eklendiğinde, bir güncelleştirme komut dosyası **İlgili Kişi Numarası** alanını tüm mevcut İlgili Kişiler için daha önce belirtilen numara serisini kullanarak ayarlar. Bir güncelleştirme kodu ayrıca **Etkin Müşteri** alanını, satış etkinliğine sahip tüm İlgili Kişiler için **Evet** olarak ayarlar.

## <a name="in-finance-and-operations"></a>Finance and Operations'ta 

İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir. Bu özellik, belirli bir İlgili Kişinin dışarıda tutulduğunu gösterir. Bu durumda, dışarıda tutulan İlgili Kişiler, Sales içerisinde tutulur.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

### <a name="contact-to-contact"></a>İlgili Kişi'den İlgili Kişi'ye

- **Kaynak &gt; CDS** eşlemesi içindeki **CDS Kuruluş Kodu**'nu güncelleştir.

    - **Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.
    - **PrimaryAccount_Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.

- **Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir. Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; İşlemler** eşlemesinde belirtebilirsiniz. Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır. **PrimaryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.
- Aşağıdaki alanlar için bir değerin Finance and Operations'ta bulunduğundan emin olun. Bilgi Finance and Operations içinde gerekli değilse, eşlemeyi **CDS &gt; Hedef** eşlemesinden kaldırabilirsiniz.

    - **Finance and Operations içinde alan adı** Karar
    - **Eşleme:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>İlgili Kişi'den Müşteri'ye

- **Kaynak &gt; CDS** eşlemesi içindeki **CDS Kuruluş Kodu**'nu güncelleştir. **Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.
- **Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir. Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinde belirtebilirsiniz. Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır. **PrimaryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.
- **CustomerGroup**, Finance and Operations içerisinde gereklidir. Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinde belirtebilirsiniz. Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır. **CustomerGroupId** için varsayılan bir şablon değeri **10**'dur.
- Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten ekleyerek, Finance and Operations'daki el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** - Bir varsayılan site, Finance and Operations'taki ürünlerde de tanımlanabilir. Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir. **SiteId** için bir şablon değeri tanımlanmamıştır.
    - **WarehouseId** - Bir varsayılan ambar, Finance and Operations'taki ürünlerde de tanımlanabilir. Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir. **WarehouseId** için bir şablon değeri tanımlanmamıştır.
    - **LanguageId** - Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir. **LanguageId** için varsayılan şablon değeri **en-us** olur.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

### <a name="contact-to-contact"></a>İlgili Kişi'den İlgili Kişi'ye

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki İlgili Kişiler için şablon eşleme](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>İlgili Kişi'den Müşteri'ye

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki İlgili Kişiler için şablon eşleme](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>İlgili konular

[Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme](products-template-mapping.md)

[Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping.md)

[Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme](sales-quotation-template-mapping.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme](sales-order-template-mapping.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme](sales-invoice-template-mapping.md)

