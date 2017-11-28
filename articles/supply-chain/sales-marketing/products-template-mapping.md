---
title: "Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme"
description: "Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 405a6cf9f3e6cc52925ff7d9f10836196343c36b
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun. 

Bu konu, ürünleri Microsoft Dynamics 365 for Sales'a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan eşitlemek için altta yatan görevleri ve şablonları açıklar.

## <a name="template-and-task"></a>Şablon ve görev

Ürünleri Microsoft Dynamics 365 for Sales'a (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'tan (Finance and Operations) eşitlemek için aşağıdaki görevleri ve şablonları açıklar.

-   Şablonun adı: Ürünler (Fin and Ops'tan Sales'a)

-   Görevin proje içindeki adı: Ürünler

Ürün eşitlemesinden önce gerekli görevler: Hiçbiri

## <a name="entity-set"></a>Varlık kümesi

| **Finance and Operations** | **CDS** | **Satış**  |
|----------------------------|---------|------------|
| Satış yapılabilir serbest bırakılan ürünler | Ürün | Ürünler   |

## <a name="entity-flow"></a>Varlık akışı

Ürünler Finance and Operations'ta yönetilir ve Sales'a eşitlenir. Finance and Operations'taki **Satılabilir serbest ürünler** veri varlığı, yalnızca satılabilir olan ürünleri dışa aktarır; bu da bir satış siparişinde kullanılması gereken bilgiye sahip ürünler anlamına gelir. Aynı kurallar, bir ürün **Yayımlanan ürün** sayfasında **Doğrula** işlevi le doğrulanıyorsa da geçerlidir.

**Ürün numarası** bir anahtar olarak kullanılır, bu da ürün çeşitlerinin CDS ve Sales ile **Ürün çeşidi** başına bireysel **Ürün kodları** ile eşitlendiği anlamına gelir.

## <a name="prospect-to-cash-solution-for-sales"></a>Sales için Aday müşteriden nakde çözümü

Sales'ta, ürünlere, ürünün dışarıda tutulduğunu belirten **Harici olarak tutulan** alanı eklenir. Değer, Sales'a içe aktarmada varsayılan olarak **Evet** olarak ayarlanır.

-   **Dışarıda tutulan = Evet**: Ürün Finance and Operations'tan geliyor ve Sales'ta düzenlenebilir olmayacaktır.

-   **Dışarıda tutula = Hayır**: Ürün doğrudan Sales'a girildi.

-   **Dışarıda tutulan = Boş**: Ürün Sales'ta, Aday müşteriden nakde çözümünü etkinleştirmeden önce mevcuttu.

**Dışarıda tutulan** bilgisi yalnızca **Dışarıda tutulan ürünler** özelliğine sahip **Tekliflerin** ve **Satış siparişlerinin** Finance and Operations'a eşitleneceği anlamına gelir.

**Dışarıda tutulan ürünler** otomatik olarak ilk geçerli **Fiyat listesine**, aynı para birimi ile eklenir. Listenin **Ad** sıralamasına göre alfabetik olarak düzenlendiğini unutmayın. Finance and Operations'taki ürün satış fiyatı, **Fiyat listesindeki** fiyat olarak kullanılır. Bu, Finance and Operations içindeki her bir **Ürün satış para birimi** için Sales içinde bir **Fiyat listesi** bulundurmanın zorunlu olduğu anlamına gelir. Yayımlanan satılabilir ürünler üzerindeki para birimi, ürünün dışa aktarıldığı tüzel kişiliğin muhasebe para birimine uygun olarak ayarlanır.

> [!NOTE]
> Ürün eşitleme, eşleşen para birimine sahip bir **Fiyat listesi** olmadan başarılı olmaz.

## <a name="preconditions-and-mapping-setup"></a>Önkoşullar ve eşleme kurulumu

-   İlk eşitlemeyi çalıştırmadan önce **Farklı ürün tablosu**'nu Finance and Operation içindeki mevcut ürünler için doldurmalısınız. Mevcut ürünler bu iş tamamlanana kadar eşitlenmeyecektir.

    -   Finance and Operations'ta, **Farklı ürün tablolarını doldur**'u aramak için Arama'yı kullanın.

    -   İşi çalıştırmak için **Farklı ürün tablosunu doldur**'u tıklatın. Bu işin yalnızca bir kere çalıştırılması gerekir.

-   **Ölçü birimi** satmak için ihtiyaç duyulan **ValueMap**'in Finance and Operations'ta **Kaynak-\> CDS eşleme SalesUnitSymbol / DefaultSellingUnitOfMeasure** içinde mevcut olduğundan emin olun.

-   **Kaynak -\> CDS** içindeki **CDS Kuruluş Kodu Organization_OrganizationId**.

    -   Şablon değeri varsayılan olarak ORG001 olur.

-   **Unit group** (**defaultuomscheduleid.name**) için **ValueMap**'i **CDS -\> Hedef** içerisinde, Sales içindeki **Birim grupları** ile eşleşmek için güncelleştirin.

    -   Şablon değeri **Varsayılan birim**'e varsayılan olarak değiştirilir.

-   Finance and Operations'tan UOM'ler satan tüm ürünlerin Sales içinde **CDS çekme listeleri** değeri ile mevcut olduğundan emin olun.

-   **Fiyat listelerini** Sales içerisinde, Finance and Operations içindeki her bir ürün satış para biriminde mevcut olduğundan emin olun.

-   Ürünler Sales'ta **Taslak** veya **Etkin** durumuyla oluşturulabilir. Bu, Sales'ta **Satışlar** altında **Sistem ayarları** içerisinde denetlenebilir.

    -   Taslak durumunda oluşturulan ürünlerin **Teklif** veya **Satış siparişi**'ne eklenebilmeden önce etkinleştirilmesi gerekir.

## <a name="template-mapping-in-data-integrator"></a>Veri entegratörü içerisindeki şablon eşleme

Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.

![veri entegratörü içerisindeki şablon eşleme](./media/products-template-mapping-data-integrator-1.png)

![veri entegratörü içerisindeki ürünler için şablon eşleme](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>İlgili konular

[Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme](accounts-template-mapping.md)

[Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme](contacts-template-mapping.md)

[Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme](sales-quotation-template-mapping.md)

[Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme](sales-order-template-mapping.md)

[Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme](sales-invoice-template-mapping.md)


