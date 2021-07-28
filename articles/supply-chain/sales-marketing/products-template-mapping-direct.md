---
title: Supply Chain Management'taki ürünleri doğrudan Sales'daki ürünlerle eşitleme
description: Bu konuda, ürünleri Dynamics 365 Sales'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.
author: ChristianRytt
ms.date: 06/10/2019
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
ms.openlocfilehash: 613fd4bad93e28360ca6862b7b30b2e4356ca489
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353408"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>Supply Chain Management'taki ürünleri doğrudan Sales'daki ürünlerle eşitleme

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.

Bu konuda, ürünleri doğrudan Dynamics 365 Sales'dan Dynamics 365 Supply Chain Management'a eşitlemek için kullanılan şablon ve temel görevler ele alınmaktadır.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir. Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve temel görevler, ürünleri Supply Chain Management'tan Sales'a eşitlemek için kullanılmaktadır.

- **Veri tümleştirmede şablonun adı:** Ürünler (Supply Chain Management'tan Sales'a) - Doğrudan
- **Veri tümleştirme projesindeki görevin adı:** Ürünler

Ürün eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.

## <a name="entity-set"></a>Varlık kümesi

| Supply Chain Management    | Satışlar    |
|----------------------------|----------|
| Satış yapılabilir serbest bırakılan ürünler | Ürünler |

## <a name="entity-flow"></a>Varlık akışı

Ürünler, Supply Chain Management'ta yönetilir ve Sales'a eşitlenir. Supply Chain Management'taki **Satılabilir serbest bırakılan ürünler** veri varlığı, yalnızca *satılabilir* ürünleri dışarı aktarır. Satış yapılabilir ürünler, bir satış siparişinde kullanılmak üzere gerekli bilgilere sahip olan ürünlerdir. Aynı kurallar, bir ürün **Serbest bırakılan ürün** sayfasında **Doğrula** işleviyle doğrulanıyorsa da geçerlidir.

Ürün numarası anahtar olarak kullanılır. Bu nedenle, ürün çeşitleri Sales'e eşitlendiğinde her ürün çeşidinin ayrı bir ürün kimliği vardır.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Sales'ta ürünlere, ürünün dışarıda tutulduğunu belirten yeni bir **Dışarıda tutulan** alanı eklenir. Varsayılan olarak değer Sales'a içe aktarma sırasında **Evet** olarak ayarlanır. Aşağıdaki değerler kullanılabilir:

- **Evet** – Ürün, Supply Chain Management'tan gelir ve Sales'da düzenlenemez.
- **Hayır** – Ürün doğrudan Sales içinden girilmiştir.
- **(Boş)** – Aday müşteriden nakde çözümü etkinleştirilmeden önce ürün Sales içinde vardır.

**Dışarıda Tutulan** alanı, yalnızca dışarıda tutulan ürünler bulunan teklif ve satış siparişlerinin Supply Chain Management ile eşitlenmesini sağlamaya yardımcı olur.

Dışarıda tutulan ürünler otomatik olarak aynı para birimine sahip ilk geçerli fiyat listesine eklenir. Fiyat listeleri ada göre alfabetik olarak düzenlenir. Supply Chain Management'taki ürün satış fiyatı, fiyat listesindeki fiyat olarak kullanılır. Bu nedenle, Supply Chain Management'taki her ürün satış para birimi için Sales'da bir fiyat listesi olmalıdır. Serbest bırakılmış satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.

> [!NOTE]
> - Eşleşen para birimine sahip bir fiyat listesi olmadığı sürece ürün eşitleme başarılı olmaz.
> - Tümleştirmeyle kullanılan fiyat listesini, Veri Tümleştirme projesindeki pricelevelid.name [Varsayılan Fiyat Listesi (Ad)] ile eşleştirerek denetleyebilirsiniz. Girişin tamamen küçük harflerden oluşması gerekir. Örneğin Satışta "Standard" adlı bir fiyat listesi varsayılanı şöyle olur: Hedef alan: pricelevelid.name [Varsayılan Fiyat Listesi (Ad)] ve Eşleşme türü: [ { "transformType": "Default", "defaultValue": "standard" } ].

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- Eşitlemeyi ilk kez çalıştırmadan önce Farklı ürün tablosu'nu Supply Chain Management'taki mevcut ürünler için doldurmanız gerekir. Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.

    1. Supply Chain Management'ta **Farklı ürün tablosunu doldur**'u aramak için Arama'yı kullanın.
    2. İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u seçin. Bu işlemin yalnızca bir kez çalıştırılması gerekir.

- Supply Chain Management ile Sales arasındaki satış ölçü birimi (UOM) için gerekli değer eşlemesinin **SalesUnitSymbol** ile **DefaultUnit (Ad)** eşlemesinde var olduğundan emin olun.
- **Birim gurubu** (**defaultuomscheduleid.name**) için değer eşlemesini güncelleştirin, böylece bu eşleme Sales'deki **Birim grupları** ile eşleşir.

    Varsayılan şablon değeri **Varsayılan birim**'dir.

- Supply Chain Management'taki tüm ürünlerin satış UOM'larının Sales'da mevcut olduğundan emin olun.
- Fiyat listelerinin Supply Chain Management'taki her ürün satış para birimi için Sales'da mevcut olduğundan emin olun.
- Sales'de ürünler oluşturulduğunda, durumları **Taslak** veya **Etkin** olabilir. Davranış Sales'deki **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altından kontrol edilebilir.

    **Taslak** durumuna sahip olan ürünler oluşturulduğunda, satış siparişleri veya tekliflere eklenmeleri için etkinleştirilmeleri gerekir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görsel, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.

![Veri tümleştirici içerisindeki şablon eşleme.](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>İlgili konular

[Aday müşteriden nakde](prospect-to-cash.md)

[Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]