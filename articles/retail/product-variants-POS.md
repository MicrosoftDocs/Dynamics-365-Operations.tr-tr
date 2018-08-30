---
title: "Satış noktasında (POS) stok arama"
description: "Bu konu (POS) satış noktasındaki stok bilgilerini görüntülemek için kullanılabilir seçenekleri açıklar."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: e40c558e03ef230fee6726994bc94979d40493c2
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a>Satış noktasında (POS) stok arama

[!include [banner](includes/banner.md)]

Satış notasında (POS) stok araması perakendecilerin gerçek zamanlı işlem başarısına ulaşmasına ve mağazalara, POS'a ve arka ofise bağlanarak öngörüler edinmesine yardımcı olur. Bu işlev, mağazalar ve dağıtım merkezleri arasında ürün stoğunun doğru ve gerçek zamanlı görünümünü sağlar. Ayrıca, stok planlamasını gerçek zamanlı geliştirerek perakendecilerin ek verimlilik ve maliyet tasarrufu sağlamasına yardımcı olur.

Bir kuruluştaki stoğun doğru ve gerçek zamanlı görünümü mağaza görevlilerinin zamanında, üst seviye müşteri hizmeti sunmasını sağlar. En önemli olan zaman müşterinin satın alma kararını vermeye hazır olduğu andır. Mağazadaki kasiyerlerin gerçek zamanı bilgileri parmaklarının ucunda bulması çok önemlidir; böylece ürün teslimatı ve alınması için doğru şekilde taahhütte bulunabilirler.

**Stok araması** sayfasını **Retail Modern POS** çalışma alanından veya **Retail Cloud POS** çalışma alanından açabilirsiniz.

![POS ana sayfasında stok araması kutucuğu](media/POSHomepage.png)

**Stok araması** sayfasında, ürün numarasını girmek için sayısal bir klavye kullanabilirsiniz. Daha sonra birden çok mağaza veya ambar için eldeki miktarı görebilirsiniz.

![Standart stok arama sayfası](media/InventoryLookUp.png)

**Ayrılmış** ve **Sipariş edilmiş** miktarlar da her yerleşim için gösterilir.

- **Ayrılmış** – Bu miktar, yerleşimde belirtilen ürün numarası için arka ofisteki **Fiziksel rezerve** değerine başvuruda bulunur.
- **Sipariş edilmiş** – Bu miktar, yerleşimde belirtilen ürün numarası için arka ofisteki **Toplam sipariş edilen** değerine başvuruda bulunur.

## <a name="locations-that-inventory-availability-information-is-shown-for"></a>Stok kullanılabilirlik bilgisinin gösterildiği yerleşimler

Yerleşimlerin listesi iki varlık türünü içerir:

- **Perakende mağazalar** – Liste Retail Headquarters'da geçerli mağaza için mağaza bulucu grubunu kullanarak yapılandırılan mağazalar listesini gösterir. 
- **Dağıtım merkezleri** – Microsoft Dynamics 365 for Retail'de çeşitli türde dağıtım merkezleri (ambarlar gibi) yapılandırılabilir. Bununla birlikte, liste stok kullanılabilirlik bilgisini yalnızca **standart** varsayılan türündeki dağıtım merkezleri için gösterir. 

    > [!NOTE]
    > Stok kullanılabilirlik bilgileri POS'ta **Transit**, **karantina** ve **Rotadaki Mallar** türündeki ambarlar için gösterilmez.

**Stok arama** sayfasında, eldeki geçerli miktarların, rezerve edilen miktarların ve sipariş edilen miktarların yanı sıra her mağaza için karşılanabilir miktar (ATP) miktarlarını da görebilirsiniz. ATP bilgilerini görmek için mağaza seçin ve ardından **Mağaza kullanılabilirliğini göster**'i seçin.

![ATP miktarları](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a>Tüm ürün çeşitlerini görmek için Boyut tabanlı matrisi açma

Ana ürünün **Ürün ayrıntıları** sayfasında veya **Stok arama** sayfasında, sayfanın altındaki uygulama çubuğundan **Tüm ürün çeşitlerini görüntüle**'yi seçin. Bu sayfalardan ilk başlatma için **Boyut tabanlı matris** görünümü geçerli mağaza için bir ürünün tüm çeşitlerine ilişkin stok kullanılabilirlik bilgisini gösterir.

> [!NOTE]
> **Tüm ürün çeşitlerini görüntüle** düğmesi yalnızca ürün çeşitleri bulunan madde ana ürünleri için kullanılabilir. Bağımsız ürünler veya setler için kullanılamaz.

![Stok arama sayfasındaki tüm ürün çeşitlerini görüntüle düğmesi](media/StandardToMatrix.png)

Bir ana ürünün **Ürün ayrıntıları** sayfasında **Tüm ürün çeşitlerini görüntüle**'yi seçin veya **Stok arama** sayfasında, bir yerleşim seçmeden **Boyut tabanlı matris** görünümüne giderek geçerli mağaza için bir ürünün tüm çeşitlerinin stok kullanılabilirlik bilgisini görüntüleyin.

![Stok arama sayfası için boyut tabanlı matris görünümü](media/Matrix.png)

> [!NOTE]
> Önceki örnekte boyutların görüntülenme sırası alfabetikti çünkü boyutların görüntülenme sırası seçilen ürün için yapılandırılmamıştı.

**Boyut tabanlı matris** görünümünde, ürün çeşitlerine ait hücreler alt sağ köşede bir eldeki değer içerir. Aşağıdaki tablo çeşitli değerlerin anlamını açıklar.

| Eldeki değer                            | Tanım |
|------------------------------------------|-------------|
| 0 (sıfır)'dan büyük olan sayısal değer | Seçili yerleşime bir ürün çeşidi serbest bırakılmıştır ve hücrede ek eylemler gerçekleştirebilirsiniz. (Bu eylemler, bu konuda daha ayrıntılı açıklanacaktır.) |
| **0** (sıfır)                             | Bir ürün çeşidi seçili yerleşime serbest bırakılır ancak madde seçili yerleşimde kullanılabilir değildir. Bununla birlikte, hücrede ek eylemler gerçekleştirebilirsiniz. (Bu eylemler, bu konuda daha ayrıntılı açıklanacaktır.) |
| **yok** veya etkin olmayan bir hücre              | Seçili yerleşime bir ürün çeşidi serbest bırakılmamıştır ve hücrede ek eylemler gerçekleştiremezsiniz. |

Kullanmak üzere yeni bir boyut seçerek boyutlar için pivotu değiştirebilirsiniz. 

![Pivotu değiştirme](media/ChangePivot.png)

![Pivot değiştirildi](media/PivotChanged.png)

> [!NOTE]
> Önceki örneklerde , seçili ürün için boyutları görüntüleme sırası özeldir (alfabetik değildir). Arka ofiste ayarlanan boyut görüntüleme sırasını temel alır.

Ayrıca, **Boyut tabanlı matris** görünümde, bir mağaza çalışanının verimliliği artırmasına yardımcı olacak başka eylemler gerçekleştirilebilir. Burada bazı örnekler verilmiştir:

- Diğer yerleşimlerdeki tüm ürün çeşitlerinin stok kullanılabilirliğine bakmak için mağaza yerleşimini değiştirin. Bu yerleşimler mağaza bulucu grubundaki diğer mağazaları ve **Standart** varsayılan türündeki dağıtım merkezlerini içerir.
- Bir müşteriye bağımsız bir ürün çeşidini peşin alışveriş, mağazadan alma veya adrese sevkiyat kullanarak satın.
- Belirli bir yerleşimdeki bağımsız ürün çeşidi için müşteriye ATP bilgisini verin.

![Ürün çeşidi kutularındaki ek eylemler](media/VariantActions.png)

> [!NOTE]
> Önceki örnekte boyutların görüntülenme sırası alfabetikti çünkü boyutların görüntülenme sırası seçilen ürün için yapılandırılmamıştı.

Aşağıdaki tablo kullanılabilen ek eylemler hakkında daha fazla bilgi sağlar.


|        Eylem        |                                                                                                                    Tanım                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       Şimdi sat       |                               Seçili madde ürün çeşidini harekete ekleyin ve kullanıcıyı hareket ekranına yönlendirin. (Bu eylem seçili yerleşim bir dağıtım merkezi olduğunda kullanılamaz.)                               |
|   Mağazadan alma   |      Seçilen yerleşimden alınacak ürün çeşidi için bir müşteri siparişi oluşturun ve kullanıcıyı hareket ekranına yönlendirin. (Bu eylem seçili yerleşim bir dağıtım merkezi olduğunda kullanılamaz.)       |
|     Ürün sevk et     |                                                 Seçilen yerleşimden sevk edilecek ürün çeşidi için bir müşteri siparişi oluşturun ve kullanıcıyı hareket ekranına yönlendirin.                                                 |
|     Kullanılabilirlik     |                                                                             Seçili yerleşim için seçilen ürün çeşidi birleşimine ilişkin ATP bilgisini gösterin.                                                                              |
|  Tüm yerleşimleri göster  | Standart stok arama görünüme geçin ve mağaza bulucu grubundaki tüm mağazalarda ve <strong>Standart/Varsayılan</strong> türündeki dağıtım merkezlerinde madde ürün çeşidi için stok kullanılabilirlik bilgilerini vurgulayın. |
| Ürün ayrıntılarını görüntüle |                                                                         Kullanıcıyı ilişkili ana ürünün <strong>Ürün ayrıntıları</strong> sayfasına yönlendirin.                                                                          |


