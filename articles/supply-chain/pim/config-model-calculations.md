---
title: Ürün yapılandırma modeli hesaplamaları
description: Bu konuda, bir ürün yapılandırma modelinde öznitelikler için hesaplamaların nasıl oluşturulacağı açıklanmaktadır
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 349fed3ca75b94db2f421a1ff3c3553c96c202c37d59857a3d973f3de8f995ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755263"
---
# <a name="product-configuration-model-calculations"></a>Ürün yapılandırma modeli hesaplamaları

[!include [banner](../includes/banner.md)]

Bu konuda, bir ürün yapılandırma modelinde öznitelikler için hesaplamaların nasıl oluşturulacağı açıklanmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Ürün konfigürasyon modelinde, bir ürünün konfigürasyon değerlerini hesaplamak için hesaplamalar kullanılır. Hesaplamaları ayarlamaya başlamadan önce ilgili ürün konfigürasyon modeli mevcut olmalıdır. Konfigürasyon modellerinin kurulum işlemine ve ilgili görevlere genel bakış için, bkz. [ürün konfigürasyon modeli ayarlama](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Hesaplama oluşturma

Bir hesaplama bir ifade ve bir hedef özniteliğinden oluşur. Daha fazla bilgi için, bkz. [Ürün konfigürasyon modellerini hesaplama SSS](calculate-product-configuration-models.md).

Varolan bir ürün modeli için hesaplama oluşturmak üzere, aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi \> Ortak \> Ürün yapılandırma modelleri** öğelerini tıklayın.
1. Bir ürün konfigürasyon modeli açın ve **Düzenle**'yi seçin.
1. **Hesaplamalar** hızlı sekmesinde, hesaplama eklemek için **Ekle**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

    - **Ad**: Hesaplama için bir ad girin.
    - **Açıklama**: Hesaplamanın açıklamasını girin.
    - **Hedef özniteliği**: Hesaplamasını yapmakta olduğunuz özniteliği seçin.

1. **İfadeyi Düzenle**'yi seçin.
1. **Bir hesaplama girin** iletişim kutusunda, ifadeye gerekli öznitelikleri, işleçleri ve değerleri ekleyin. Bu unsurlarla çalışma hakkında daha fazla bilgi için bkz. [Ürün yapılandırma modellerinde ifade kısıtlamaları ve tablo kısıtlamaları](expression-constraints-table-constraints-product-configuration-models.md).
1. İfadeniz hazır olduğunda **Tamam**'ı seçin.

## <a name="calculation-examples"></a>Hesaplama örnekleri

Bu bölümde, hesaplamaların nasıl çalıştığını gösteren birkaç örnek sağlanmaktadır.

### <a name="example-1"></a>Örnek 1

Hedef özniteliği Boole'dir, hesaplama aşağıdaki koşullu ifadeyi kullanır:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

`decimalAttribute2` değeri, `decimalAttribute1` değerine eşitse veya daha yüksekse bu ifade, hedef özniteliğe *True* değerini döndürür. Aksi takdirde, *False* değeri döndürür.

### <a name="example-2"></a>Örnek 2

Bu örnek, hedef özniteliği olarak `textFixedList` metin özniteliğini kullanır. Bu öznitelik aşağıdaki sabit listeyi içerir.

| Değer | Çözücü değeri |
|---|---|
| A | 1a |
| B: | 2b |
| A | 2c |

Aşağıdaki ekran görüntüsü, bu öznitelik için ayarların sisteminizde nasıl görünebileceğini gösterir.

![Öznitelik türü ayarları Örnek 2.](media/model-calculations-example2.png "Öznitelik türü ayarları Örnek 2")

Öznitelik aşağıdaki koşul deyiminde kullanılır:

`If[integerAttribute < 150, 0, 2]`

`integerAttribute` 150'den küçükse, bu ifade sabit listesindeki ilk kaydın metin değerini *A* döndürür. Aksi durumda, sabit listedeki üçüncü kaydın metin değerini *C* döndürür.

> [!NOTE]
> Sabit liste sıfır tabanlı bir numaralandırmaya (enum) eşdeğerdir ve değerlerine uygun tamsayı değeri tarafından erişilir. Bu nedenle, ilk sabit liste değeri (*A*) *0* ile eşleşirse, ikinci değer (*B*) *1* ile eşleşir ve üçüncü değer (*C*) *2* ile eşleşir.

### <a name="example-3"></a>Örnek 3

Bu örnek, önceki örnekten `textFixedList` hedef özniteliğini kullanır. Ayrıca, aşağıdaki sabit listeyi içeren başka bir metin özniteliği (`textAttribute`) de kullanır.

| Değer | Çözücü değeri |
|---|---|
| AA | 1aa |
| BB | 2bb |

Aşağıdaki ekran görüntüsü, bu öznitelik için ayarların sisteminizde nasıl görünebileceğini gösterir.

![Öznitelik türü ayarları Örnek 3.](media/model-calculations-example3.png "Öznitelik türü ayarları Örnek 3")

`textFixedList` Özniteliğinin değeri aşağıdaki koşul deyimi kullanılarak hesaplanır:

`If[textAttribute == "1aa", 0, 2]`

`textAttribute` değeri *1aa* ile eş değer bir çözücü değerine sahipse bu ifade `textFixedList` sabit listesindeki ilk kaydın metin değerini *A* döndürür. Aksi durumda, `textFixedList` sabit listesindeki üçüncü kaydın metin değerini *C* döndürür.

> [!NOTE]
> - Koşullu deyim özniteliğin çözücü değerini kullanmalıdır.
> - Hesaplamalarda yalnızca sabit liste metin öznitelikleri kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [Ürün yapılandırma modeli için hesaplamalar SSS](calculate-product-configuration-models.md)
- [Ürün yapılandırma modeline bir ifade kısıtlaması ekleme](tasks/add-expression-constraint-product-configuration-model.md)
- [Ürün yapılandırma modellerine genel bakış](product-configuration-models.md)
