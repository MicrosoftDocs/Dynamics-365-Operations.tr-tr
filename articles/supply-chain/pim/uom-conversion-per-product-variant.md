---
title: Ürün çeşidi başına ölçü birimi dönüşümü
description: Bu konuda, ürün çeşitleri için ölçü birimi dönüştürmelerinin nasıl ayarlanacağı açıklanmaktadır. Bir kurulum örneği içerir.
author: johanhoffmann
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: ed28928b0f07833d5906a68f780e3bb5bbe0bfe9
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921229"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Ürün çeşidi başına ölçü birimi dönüşümü

[!include [banner](../includes/banner.md)]

Bu konuda, farklı ürün çeşitleri için ölçü birimi dönüştürmelerinin nasıl ayarlanacağı açıklanmaktadır.

Korunması gereken birden fazla ayrı ürün oluşturmak yerine tek bir ürünün çeşitlerini oluşturmak için ürün çeşitlerini kullanabilirsiniz. Örneğin, belirli bir boyut ve renkteki tişört bir ürün çeşidi olabilir.

Önceden, birim dönüştürmeleri yalnızca ana ürün üzerinde ayarlanabilirdi. Bu nedenle, tüm ürün çeşitleri aynı birim dönüştürme kurallarına sahipti. Ancak, *Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliği etkinleştirildiğinde; tişörtleriniz kutularda satılıyorsa ve bir kutuda paketlenebilecek tişörtlerin sayısı boyutlarına bağlıysa artık farklı tişört boyutları ve paketleme için kullanılan kutular arasında birim dönüştürmeleri ayarlayabilirsiniz.

## <a name="turn-on-the-feature-in-your-system"></a>Sisteminizdeki özelliği etkinleştirme

Sisteminizde bu özelliği henüz görmüyorsanız [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) konusuna gidin ve *Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliğini açın.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Çeşit başına birim dönüşümü için bir ürün ayarla

Ürün çeşitleri, yalnızca ana ürünler için oluşturulabilir. Daha fazla bilgi için [Bir ana ürün oluşturma](tasks/create-product-master.md) konusuna bakın. *Ürün çeşitleri için ölçü birimi dönüştürmeleri* özelliği, fiili ağırlık işlemleri için ayarlanmış ürünlerde kullanılamaz.

Ana ürünü, birim dönüştürmeyi her çeşit için destekleyecek şekilde yapılandırmak üzere aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Ana ürünler**'e gidin.
1. Ana ürünün **Ürün ayrıntıları** sayfasına gitmek için bir ana ürün oluşturun veya açın.
1. **Ölçü birimi dönüştürmelerini etkinleştir** seçeneğini *Evet* olarak ayarlayın.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **Ayar** gurubunda **Birim dönüştürmeleri**'ni seçin.
1. **Birim dönüştürmeleri** sayfası açılır. Aşağıdaki sekmelerden birini seçin:

    - **Sınıf içi dönüştürmeler**: Aynı birim sınıfına ait birimler arasında dönüştürme yapmak için bu sekmeyi seçin.
    - **Sınıflar arası dönüştürmeler**: Farklı birim sınıflarına ait birimler arasında dönüştürme yapmak için bu sekmeyi seçin.

1. Yeni bir birim dönüştürme eklemek için **Yeni**'yi seçin.
1. **Dönüştürme oluştur** alanını aşağıdaki değerlerden birine ayarlayın:

    - **Ürün**: Bu değeri seçerseniz ana ürün için birim dönüştürme ayarlayabilirsiniz. Bu birim dönüştürme, birim dönüştürmenin tanımlanmadığı tüm ürün çeşitleri için geri dönüş olarak kullanılacaktır.
    - **Ürün çeşidi**: Bu değeri seçerseniz belirli bir ürün çeşidi için birim dönüştürme ayarlayabilirsiniz. Ürün çeşidini seçmek için **Ürün çeşidi** alanını kullanın.

    ![Yeni bir birim dönüştürme ekleme](media/uom-new-conversion.png "Yeni bir birim dönüştürme ekleme")

1. Birim dönüştürmenizi ayarlamak için sağlanan diğer alanları kullanın.
1. Yeni birim dönüştürmeyi kaydetmek için **Tamam**'ı seçin.

> [!TIP]
> Ürün veya ürün çeşidi için **Birim dönüştürmeleri** sayfasını aşağıdaki sayfalardan herhangi birinden açabilirsiniz:
> 
> - Ürün ayrıntıları
> - Serbest bırakılan ürünlerin ayrıntıları
> - Serbest bırakılan ürün çeşitleri

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryoda bir şirket küçük, orta, büyük ve çok büyük ebatlarda tişörtler satmaktadır. Tişört, bir ürün olarak ve farklı ebatları, ürünün çeşitleri olarak tanımlanmıştır. Tişörtler, kutularda paketlenmiştir. Küçük, orta ve büyük ebatlar için her kutuda beş tişört olabilir. Ancak, çok büyük ebat için her kutuda sadece dört tişörtlük yer vardır.

Şirket, farklı ürün çeşitlerini *Adet* biriminde izlemek istemektedir ancak ürünleri *Kutular* biriminde satmaktadır. Küçük, orta ve büyük ebatlar için stok birimi ile satış birimi arasındaki dönüştürme 1 Kutu = 5 Adettir. Çok büyük ebat için dönüştürme 1 Kutu = 4 Adettir.

1. **Tişört** ürününün **Serbest bırakılan ürün ayrıntıları** sayfasından **Birim dönüştürmeleri** sayfasını açın.
1. **Birim dönüştürmeleri** sayfasında, serbest bırakılan ürün çeşidi **Çok büyük** için aşağıdaki birim dönüştürmeyi ayarlayın.

    | Alan                 | Ayar                 |
    |-----------------------|-------------------------|
    | Dönüşüm formu oluştur | Ürün varyantı         |
    | Ürün varyantı       | Tişört : : X-Large : : |
    | İlk birim             | Kutular                   |
    | Katsayı                | 4                       |
    | Son Birim               | Parça                  |

1. **Küçük**, **Orta** ve **Büyük** ürün çeşitlerinin tümü, *Kutu* ile *Adet* birimleri arasında aynı birim dönüştürmeye sahip olduğu için onların aşağıdaki birim dönüştürmesini ana ürün üzerinden tanımlayabilirsiniz.

    | Alan                 | Ayar |
    |-----------------------|---------|
    | Dönüşüm formu oluştur | Ürün |
    | Ürün               | Tişört |
    | İlk birim             | Kutular   |
    | Katsayı                | 5       |
    | Son Birim               | Parça  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Birim dönüştürmelerini güncelleştirmek için Excel kullanmak

Bir üründe, farklı birim dönüştürmeleri olan birçok ürün çeşidi varsa birim dönüştürmelerini bir Microsoft Excel çalışma kitabına aktarmak, güncelleştirmek ve ardından tekrar Dynamics 365 Supply Chain Management uygulamasına yayımlamak iyi bir fikirdir.

Birim dönüştürmelerini Excel'e aktarmak için **Birim dönüştürmeleri** sayfasında, Eylem Bölmesi'nde **Microsoft Office uygulamasında aç**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Ölçü birimlerini yönetme](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]