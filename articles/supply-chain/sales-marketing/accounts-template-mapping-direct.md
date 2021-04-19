---
title: Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme
description: Bu konu, hesapları Dynamics 365 Sales'den Supply Chain Management'a eşitlemek için altta yatan görevleri ve şablonları açıklar.
author: ChristianRytt
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1bf0da5ba5274b61758bc0efdc2f2167327966ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831662"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.

Bu konu, hesapları doğrudan Dynamics 365 Sales'den Dynamics 365 Supply Chain Management'a eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.  Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve altta yatan görev, hesapları Sales'tan Supply Chain Management'a eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan
- **Projedeki görevin adı:** Hesaplar - Müşteriler

Hesap/Müşteri eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.

## <a name="entity-set"></a>Varlık kümesi

| Satışlar    | Supply Chain Management |
|----------|------------------------|
| Hesaplar | Müşteriler V2           |

## <a name="entity-flow"></a>Varlık akışı

Hesaplar Sales'ta yönetilir ve Supply Chain Management'a müşteriler olarak eşitlenir. Bu müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen müşterileri izlemek için **Evet** olarak ayarlanır. Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

**Hesap Numarası** sütunu, **Hesap** sayfasında bulunur. Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır. Müşteri İlişkileri Yönetimi (CRM) çözümünün doğal anahtar özelliği, halihazırda **Hesap Numarası** sütununu kullanan ancak hesap başına benzersiz **Hesap Numarası** değerleri kullanmayan müşterileri etkileyebilir. Şu anda, tümleştirme çözümü bu durumu desteklemez.

Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur. Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir. Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**

Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme komut dosyası **Hesap Numarası** sütununu Sales içindeki mevcut hesaplarda ayarlar. **Hesap Numarası** değeri yoksa, daha önce belirtilen numara serisi kullanılır.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- **CustomerGroupId** eşlemesi Supply Chain Management içinde geçerli bir değer bulmak için güncelleştirilmelidir. Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz.

    Varsayılan şablon değeri **10**'dur.

- Aşağıdaki eşleşmeleri ekleyerek, Supply Chain Management'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz. Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.

    - **SiteId** - Supply Chain Management'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir. Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir.

        Varsayılan şablon değeri **1**'dur.

    - **WarehouseId** - Supply Chain Management'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir. Bir varsayılan ambar, Supply Chain Management'ta sipariş başlığında üründen veya müşteriden alınabilir.

        Varsayılan şablon değeri **13**'dur.

    - **LanguageId** - Supply Chain Management'ta teklifler ve satış siparişlerini oluşturmak için bir dil gereklidir. Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır.

        Varsayılan şablon değeri **tr-tr**'dir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

> [!NOTE]
> **Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** sütunları varsayılan eşlemelere dahil değildir. Bu sütunları eşleştirmek için, tablonun aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşlemesi ayarlamanız gerekir.

Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi sütun bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.

![Veri tümleştirmede şablon eşleme](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>İlgili konular


[Aday müşteriden nakde](prospect-to-cash.md)

[Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]