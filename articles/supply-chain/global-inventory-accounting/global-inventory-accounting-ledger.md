---
title: Global Stok Muhasebesi genel defteri
description: Bu konu, bir para birimi, takvim, kural ve tüzel kişilikle ilişkilendirme birleşimiyle tanımlanan Global Stok Muhasebesi genel defterlerini açıklar.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273238"
---
# <a name="global-inventory-accounting-ledger"></a>Global Stok Muhasebesi genel defteri

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Global Stok Muhasebesi'nin kendi genel muhasebe defterleri kümesi vardır. İlgili bir tüzel kişilik için stokla ilgili bir hareket işlendiğinde, sistem bu hareketi gerektiği gibi herhangi bir sayıdaki Global Stok Muhasebesi genel muhasebe defterlerinde hesaplayabilir.

Genel muhasebe defteri, borç ve alacak ölçümlerinin bir kaydıdır. Bu ölçümler maliyet öğeleri ve yardımcı muhasebe hesapları kullanılarak sınıflandırılır. Global Stok Muhasebesi genel muhasebe defteri bir para birimi, takvim, kural ve tüzel kişilikle ilişkilendirme birleşimiyle tanımlanır.

Global Stok Muhasebesi defterlerinizi ayarlamak için **Global stok muhasebesi \> Ayar \>Global tok muhasebesi defterleri**'ne gidin. Her genel muhasebe defteri için aşağıdaki alanları ayarlayın:

- **Ad**: Defterin adını girin.
- **Açıklama**: Defterin açıklamasını girin.
- **Mali takvim**: Genel muhasebe defteri için mali takvimi belirtin.
- **Para birimi ve döviz kuru türü**: Genel muhasebe defterinin kullandığı muhasebe para birimini ve döviz kuru türünü seçmek için bu hızlı sekmedeki alanları kullanın. Seçtiğiniz para birimi tüzel kişiliğin kullandığı para biriminden farklı olabilir. Global Stok Muhasebesi'nde, kullanıcılar istedikleri kadar maliyetlendirme genel defteri tanımlayabilir. Global Stok Muhasebesi, birden fazla para biriminde ve birden fazla değerlemede stok muhasebesini destekler. Aşağıdaki alanları ayarlayın:

    - **Para Birimi**: Stokla ilgili değerlerin tutulduğu maliyetlendirme para birimini seçin. Bu değerler stok değerini, satılan malların maliyetini, transitteki stoğu ve her türlü farkı içerir.
    - **Döviz kuru türü**: Hareket para birimi cinsinden hareket tutarını ve maddelerin standart maliyetini maliyet para birimine dönüştürmek için sistemin kullanması gereken döviz kurunu seçin.

- **Kural adı**: Bir kural belirtin. Kural, maliyetlerin bu genel muhasebede nasıl hesaplanacağını belirleyen ilkeler topluluğudur.
- **Tüzel kişilik**: Genel muhasebe, seçili tüzel kişiliğe nakledilen belgeleri muhasebeleştirecektir.
- **Hazırlama**: Genel muhasebe oluşturulmadan önce oluşturulan stok hareketlerinin genel muhasebedeki para birimine ve kurala göre işlenip işlenmeyeceğini seçin. Aşağıdaki değerlerden birini seçin:

    - **Etkinleştirildi**: Genel muhasebe, genel muhasebe oluşturulmadan önce oluşturulan hareketleri işlemelidir.
    - **Devre dışı**: Genel muhasebe, yalnızca genel muhasebe oluşturulduktan sonra oluşturulan hareketleri işlemelidir.

    > [!IMPORTANT]
    > Yeni belgeler girdikten sonra geri dönüp bu alanı **ayarlayamazsınız**.

- **Durum**: Sistem, yeni oluşturulan genel muhasebe defterlerinin durumunu otomatik olarak *Hazırla* olarak ayarlar.
