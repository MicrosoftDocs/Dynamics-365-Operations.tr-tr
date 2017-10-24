---
title: "Finans işlemlerini ve müşterilere satış hesaplarını eşitle"
description: "Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Finans işlemlerini ve müşterilere satış hesaplarını eşitle

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun. 

Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="template-and-task"></a>Şablon ve görev

Aşağıdaki şablonlar ve altta yatan görevler, hesapları Sales'tan Finance to Operations'a eşitlemekte kullanılır:

- **Şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a)
- **Projedeki görevin adı:** Hesaplar - Hesap - Müşteriler

Hesap / Müşteri eşitlemesinden önce gerekli görevler: Hiçbiri

## <a name="entity-set"></a>Varlık kümesi

| Satış    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Hesaplar | Hesap | Müşteriler              |

## <a name="entity-flow"></a>Varlık akışı

Hesaplar Sales'ta yönetilir ve Finance and Operations'a Müşteriler olarak eşitlenir. Bu Müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen Müşterileri izlemek için **Evet** olarak ayarlanır. Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

**Hesap numarası** alanı, **Hesap** sayfasında kullanılabilir. Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır. Müşteri İlişkileri Yönetimi'nin (CRM) doğal anahtar özelliği, halihazırda **Hesap Numarası** alanını kullanan ancak hesap başına benzersiz **Hesap Numarası** kullanmayan müşterileri etkileyebilir. Şu anda, tümleştirme çözümü bu durumu desteklemez.

Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur. Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**

Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme kodu **Hesap Numarası** alanını Sales içindeki mevcut hesaplarda ayarlar. **Hesap Numarası** değeri yoksa, daha önce açıklanan numara serisi kullanılır.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- **CustomerGroupId** içinden **CDS &gt; Hedef** eşleşmesi, Finance and Operations içinde geçerli bir değer bulmak için güncelleştirilmelidir. Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz. Varsayılan şablon değeri **10**'dur.
- **Adres ülke bölge kodu** alanı Finance and Operations'ta gereklidir. Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinden belirtebilirsiniz. Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.

    - **AddressCountryRegionISOCode** için varsayılan şablon değeri **ABD**'dir.
    - **DeliveryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.

- Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir. **SiteId** için varsayılan bir şablon değeri **1**'dur.
    - **WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. Bir varsayılan ambar, Finance and Operations'ta sipariş başlığında üründen veya müşteriden alınabilir. **WarehouseId** için varsayılan bir şablon değeri **13**'dur.
    - **LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir. Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır. **LanguageId** için varsayılan şablon değeri **en-us** olur.

- CDS kuruluş kodunu (**Organization_OrganizationId**) **Kaynak &gt; CDS** eşlemesinde güncelleştirin. Varsayılan şablon değeri **ORG001**'dir.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir. Bu alanları eşleştirmek için bir değer eşleşmesi ayarlamanız gerekir. Değer eşlemeleri, varlığın aralarında eşitlendiği kuruluşlardaki veriye özgüdür.

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

![Veri entegratörü içerisindeki şablon eşleme](./media/accounts-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki Hesaplar için şablon eşleme](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>İlgili konular

[Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme](products-template-mapping.md)

[Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping.md)

[Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme](sales-quotation-template-mapping.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme](sales-order-template-mapping.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme](sales-invoice-template-mapping.md)




