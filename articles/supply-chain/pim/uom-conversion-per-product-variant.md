---
title: Ürün çeşidi başına ölçü birimi dönüşümü
description: Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "345939"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Ürün çeşidi başına ölçü birimi dönüşümü

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

Bu konu, ürün çeşitlerinde ölçü birimi dönüşümlerinin nasıl ayarlanabileceğini açıklar. Bir kurulum örneği içerir.

Bu özellik, şirketlerin aynı ürün üzerindeki farklı çeşitler için farklı birim dönüştürmeleri tanımlamalarına olanak tanır. Aşağıdaki örnek bu konuda kullanılır. Bir şirket, Küçük, Medium, Large ve X-Large ebatlarında tişörtler satmaktadır. Tişört, bir ürün olarak tanımlanmıştır ve farklı ebatları ürünün çeşitleri olarak tanımlanmıştır. Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-Large beden hariç. Şirket, **Adet** biriminde tişörtlerin farklı türlerini izlemek istemektedir ancak tişörtleri **Kutu** biriminde satmaktadır. Stok birimi ve satış birimi için dönüşüm, X-Large ürün çeşidi için 1 Kutu = 4 Adet olduğu durum dışında 1 Kutu = 5 Adettir.

## <a name="setup"></a>Ayarlar

**Tüm işlemler** veya yalnızca **Ambar işlemleri** için etkinleştirilmiş ürünler için parametreleri özelliği kullanarak, **Ölçü birimi dönüşümlerini**, **Ürün bilgi parametreleri** sayfasında kullanarak yapılandırabilirsiniz.

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Çeşit başına birim dönüşümü için bir ürün ayarla

Ürün çeşitleri, yalnızca **Ürün alt türü**: **Ana Ürün** ürünleri için oluşturulabilir. Daha fazla bilgi için [Bir ana ürün oluşturma](tasks/create-product-master.md) konusuna bakın.

Bu özellik fiili ağırlık işlemler için ayarlanmış olan ürünler için etkin değildir. 

Bir ana ürün birimi ölçü dönüşümünü **Ölçü dönüşümleri birimi etkinleştir** seçeneğini **Ürün ayrıntıları** sayfasında kullanarak etkinleştirirken.

Ana ürün, serbest bırakılan ürün çeşitleri ile oluşturulursa, çeşit başına ölçü dönüşümü ayarlanabilir. Bir ürün veya ürün çeşidi bağlamında ölçü birimi dönüştürme sayfası için menü öğesini, aşağıdaki sayfalarda bulabilirsiniz.

-   **Ürün ayrıntıları** sayfası
-   **Serbest bırakılan ürünlerin ayrıntıları** sayfası
-   **Serbest bırakılan ürün çeşitleri** sayfası

**Birim dönüştürme** sayfasını, bir ana ürün veya serbest bırakılmış ürün çeşidi bağlamında açtığınızda, biri dönüştürmeyi ürün mü yoksa ürün çeşidi mi için ayarlamak istediğinizi seçebilirsiniz. Bun **Ürün çeşidi** veya **Ürün**'ü, **Dönüşüm ayarla** alanında seçerek yaparsınız.

### <a name="product-variant"></a>Ürün çeşidi

**Ürünü çeşidi** seçerseniz, hangi çeşit için ürün dönüşümünü ayarlayacağınızı **Ürün çeşidi** alanında seçebilirsiniz.

### <a name="product"></a>Ürün

**Ürün** seçerseniz, ana ürün için bir birim dönüştürme ayarlayabilirsiniz. Bu birim dönüştürme, tanımlanmış bir birim dönüştürmeye sahip olmayan tüm ürün çeşitlerine uygulanır.

### <a name="example"></a>Örnek

Bir ana ürün, **Tişört**, serbest bırakılmış dört çeşide sahiptir, Küçük, Medium, Large ve X-Large. Tişörtler, bir kutuda beş tişört olabileceği şekilde paketlenmiştir, yalnızca dört tişört için yer olan X-large beden hariç.

İlk olarak **Birim dönüştürme** sayfasını, **Tişört** için serbest bırakılmış ürün ayrıntıları sayfasından seçin.

**Birim dönüştürme** sayfasında, serbest bırakılmış ürün çeşidi X-Large için birim dönüştürmeyi ayarlayın.

| **Alan**             | **Ayar**             |
|-----------------------|-------------------------|
| Dönüşüm formu oluştur | Ürün çeşidi         |
| Ürün çeşidi       | Tişört : : X-Large : : |
| İlk birim             | Kutular                   |
| Katsayı                | 4                       |
| Son Birim               | Parça                  |

Serbest bırakılan ürün çeşitleri Küçük, Medium ve Large, Kutu ve Adet arasında aynı birim dönüştürmeye sahiptir, bu da bu ürünler için birim dönüştürmeyi ana ürün üzerinde ayarlayabileceğiniz anlamına gelmektedir.

| **Alan**             | **Ayar** |
|-----------------------|-------------|
| Dönüşüm formu oluştur | Ürün     |
| Ürün               | Tişört     |
| İlk birim             | Kutular       |
| Katsayı                | 5           |
| Son Birim               | Parça      |

### <a name="using-excel-to-update-the-unit-conversions"></a>Birim dönüştürmelerini güncelleştirmek için Excel kullanmak

Bir ürün, farklı birim dönüştürmelerine sahip çok sayıda ürün çeşidine sahipse, birim dönüştürmeyi **Birim dönüştürme** sayfasından bir Excel elektronik tablosuna dışa aktarmak, dönüşümleri güncelleştirmek ve daha sonra Finance and Operations'a geri yayınlamak iyi bir fikir olabilir.

Excel'e dışa aktarma ve düzenlemeleri Finance and Operations'a yayınlama, **Birim dönüştürme** sayfasındaki **Microsoft Office'te aç** menü öğesinde etkinleştirilir.
