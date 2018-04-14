---
title: "Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme"
description: "Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Sales'teki hesapları doğrudan Finance and Operations'taki müşterilerle eşitleme

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.

Bu konu, hesapları doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.  Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve altta yatan görev, hesapları Sales'tan Finance to Operations'a eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan
- **Projedeki görevin adı:** Hesaplar - Müşteriler

Hesap/Müşteri eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.

## <a name="entity-set"></a>Varlık kümesi

| Satış    | Finance and Operations |
|----------|------------------------|
| Hesaplar | Müşteriler V2           |

## <a name="entity-flow"></a>Varlık akışı

Hesaplar Sales'ta yönetilir ve Finance and Operations'a müşteriler olarak eşitlenir. Bu müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen müşterileri izlemek için **Evet** olarak ayarlanır. Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

**Hesap numarası** alanı, **Hesap** sayfasında kullanılabilir. Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır. Müşteri İlişkileri Yönetimi'nin (CRM) doğal anahtar özelliği, halihazırda **Hesap Numarası** alanını kullanan ancak hesap başına benzersiz **Hesap Numarası** kullanmayan müşterileri etkileyebilir. Şu anda, tümleştirme çözümü bu durumu desteklemez.

Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur. Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**

Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme kodu **Hesap Numarası** alanını Sales içindeki mevcut hesaplarda ayarlar. **Hesap Numarası** değeri yoksa, daha önce belirtilen numara serisi kullanılır.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- **CustomerGroupId** eşlemesi Finance and Operations içinde geçerli bir değer bulmak için güncelleştirilmelidir. Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz.

    Varsayılan şablon değeri **10**'dur.

- Aşağıdaki eşleşmeleri ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir.

        Varsayılan şablon değeri **1**'dur.

    - **WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. Bir varsayılan ambar, Finance and Operations'ta sipariş başlığında üründen veya müşteriden alınabilir.

        Varsayılan şablon değeri **13**'dur.

    - **LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir. Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır.

        Varsayılan şablon değeri **tr-tr**'dir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir. Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.

![Veri tümleştirmede şablon eşleme](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>İlgili konular


[Müşteri adayından nakde](prospect-to-cash.md)

[Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)


