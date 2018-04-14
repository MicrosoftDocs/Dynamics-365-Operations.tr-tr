---
title: "Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Sales'e eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: 3ae50372edcd473f2288f8172b71eac33e24b636
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.

Bu konu, ürünleri doğrudan Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Sales'e eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="data-flow-in-prospect-to-cash"></a>Aday müşteriden nakde çözümünde veri akışı

Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır. Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir. Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.

[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Şablonlar ve görevler

Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın. **Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.

Aşağıdaki şablon ve altta yatan görevler, ürünleri Finance and Operations'dan Sales'e eşitlemekte kullanılır:

- **Veri tümleştirmedeki şablonun adı:** Ürünler (Fin and Ops'dan Sales'e) - Doğrudan
- **Veri tümleştirme projesindeki görevin adı:** Ürünler

Ürün eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.

## <a name="entity-set"></a>Varlık kümesi

| Finance and Operations     | Satış    |
|----------------------------|----------|
| Satış yapılabilir serbest bırakılan ürünler | Ürünler |

## <a name="entity-flow"></a>Varlık akışı

Ürünler Finance and Operations'ta yönetilir ve Sales'a eşitlenir. Finance and Operations'da **Satış yapılabilir serbest bırakılan ürünler** veri varlığı yalnızca *satış yapılabilir* ürünleri dışa aktarır. Satış yapılabilir ürünler, bir satış siparişinde kullanılmak üzere gerekli bilgilere sahip olan ürünlerdir. Aynı kurallar, bir ürün **Serbest bırakılan ürün** sayfasında **Doğrula** işleviyle doğrulanıyorsa da geçerlidir.

Ürün numarası anahtar olarak kullanılır. Bu nedenle, ürün çeşitleri Sales'e eşitlendiğinde her ürün çeşidinin ayrı bir ürün kimliği vardır.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Sales'ta ürünlere, ürünün dışarıda tutulduğunu belirten yeni bir **Dışarıda tutulan** alanı eklenir. Varsayılan olarak değer Sales'a içe aktarma sırasında **Evet** olarak ayarlanır. Aşağıdaki değerler kullanılabilir:

- **Evet** – Ürün Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.
- **Hayır** – Ürün doğrudan Sales içinden girilmiştir.
- **(Boş)** – Aday müşteriden nakde çözümü etkinleştirilmeden önce ürün Sales içinde vardır.

**Dışarıda Tutulan** alanı yalnızca dışarıda tutulan ürünleri bulunan tekliflerin ve satış siparişlerinin Finance and Operations ile eşitlenmesini sağlamaya yardımcı olur.

Dışarıda tutulan ürünler otomatik olarak aynı para birimine sahip ilk geçerli fiyat listesine eklenir. Fiyat listeleri ada göre alfabetik olarak düzenlenir. Finance and Operations'taki ürün satış fiyatı, fiyat listesindeki fiyat olarak kullanılır. Bu nedenle, Sales içerisinde, Finance and Operations içindeki her bir ürün satış para birimi için bir fiyat listesi olmalıdır. Serbest bırakılmış satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.

> [!NOTE]
> Eşleşen para birimine sahip bir fiyat listesi olmadığı sürece ürün eşitleme başarılı olmaz.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

- Eşitlemeyi ilk kez çalıştırmadan önce Farklı ürün tablosu'nu Finance and Operation içindeki mevcut ürünler için doldurmalısınız. Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.

    1. Finance and Operations'ta, **Farklı ürün tablolarını doldur**'u aramak için Arama'yı kullanın.
    2. İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u seçin. Bu işlemin yalnızca bir kez çalıştırılması gerekir.

- Finance and Operations ile Sales arasındaki satış ölçü birimi (UOM) için gerekli değer eşlemesinin **SalesUnitSymbol** ile **DefaultUnit (Name)** eşlemesinde var olduğundan emin olun.
- **Birim gurubu** (**defaultuomscheduleid.name**) için değer eşlemesini güncelleştirin, böylece bu eşleme Sales'deki **Birim grupları** ile eşleşir.

    Varsayılan şablon değeri **Varsayılan birim**'dir.

- Finance and Operations'daki tüm ürünlerin satış UOM'larının Sales'de mevcut olduğundan emin olun.
- Fiyat listelerinin Sales içerisinde, Finance and Operations içindeki her bir ürün satış para birimi için mevcut olduğundan emin olun.
- Sales'de ürünler oluşturulduğunda, durumları **Taslak** veya **Etkin** olabilir. Davranış Sales'deki **Ayarlar** > **Yönetim** > **Sistem ayarları** > **Satış** altından kontrol edilebilir.

    **Taslak** durumuna sahip olan ürünler oluşturulduğunda, satış siparişleri veya tekliflere eklenmeleri için etkinleştirilmeleri gerekir.

## <a name="template-mapping-in-data-integration"></a>Veri tümleştirmede şablon eşleme

Aşağıdaki görsel, veri tümleştirmede bir şablon eşleme örneğini gösterir. 

> [!NOTE]
> Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.

![Veri entegratörü içerisindeki şablon eşleme](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>İlgili konular

[Müşteri adayından nakde](prospect-to-cash.md)

[Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping-direct.md)

[Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping-direct.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-order-template-mapping-direct-two-ways.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme](sales-invoice-template-mapping-direct.md)




