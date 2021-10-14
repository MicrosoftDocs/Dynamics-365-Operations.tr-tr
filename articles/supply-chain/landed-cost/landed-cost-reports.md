---
title: Varış yeri maliyeti raporları
description: Bu konuda, varış yeri maliyeti modülü için kullanılabilen çeşitli rapor türlerinin nasıl bulunacağı ve kullanılacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: cb0ea44c0924fc5d2c295a9285701d1f678c3473
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571749"
---
# <a name="landed-cost-reports"></a>Varış yeri maliyeti raporları

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a>Bekleyen faturalar

Bekleyen faturalar raporu, her yolculukla ilişkili çeşitli maliyet düzeylerindeki bekleyen tüm faturaların bir listesini içerir. Yolculuk ve yolculuk maliyetlerini genel muhasebe hareketleri listesiyle düzenli olarak mutabık kılmak için kullanılır. Ek yük maliyeti faturalandıktan sonra rapordan kaldırılır.

Bekleyen fatura raporu oluşturmak için aşağıdaki adımları izleyin.

1. **Varış yeri maliyeti \> Raporlar \> İzleme \> Bekleyen faturalar**'a gidin.
1. **Bekleyen faturalar** iletişim kutusunda, **Tarih itibarıyla** alanında bir tarih belirtin. Bu tarihte veya bu tarihten önceki bekleyen tüm faturalar çıktıya dahil edilecektir.
1. **Göster** altında aşağıdaki seçeneklerden birini belirleyin:

    - **Faturalanmayan maliyet**: Tahmini maliyet değeri olan ancak fiili maliyeti olmayan faturalanmış sevk irsaliyelerinin maliyetlerini dahil eder.
    - **Faturalanmayan stok**: Faturalanan ancak satın alma siparişinin henüz alınmadığı maliyetleri dahil eder.
    - **Tümü faturalı değil**: Hem **Faturalanmayan maliyet** seçeneğinin hem de **Faturalanmayan stok** seçeneğinin sonuçlarını ekler.

1. Henüz fiili maliyeti olmayan ve stok alınmamış maliyetleri dahil etmek için **Yeni maliyetleri dahil et** seçeneğini *Evet* olarak ayarlayın. *Hayır* olarak ayarlarsanız rapor yalnızca faturalanan maliyetleri içerir.
1. **Görünüm** bölümünde, rapora eklemek istediğiniz her ayrıntı türünü etkinleştirin.
1. Microsoft Dynamics 365 Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, raporun çıktı biçimini seçmek için **Hedef** hızlı sekmesini kullanın.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, rapora dahil edilecek kayıtları daha da sınırlamak için **Rapora dahil edilecek kayıtlar** hızlı sekmesini kullanın.
1. Raporu oluşturmak için **Tamam**'ı seçin.

## <a name="activityprovider-analysis-reports"></a>Etkinlik/sağlayıcı analiz raporları

Etkinlik/sağlayıcı analiz raporları, her sağlayıcı için zaman tahminlerinizin doğruluğunu gözden geçirmenizi sağlar.

Bir etkinlik/sağlayıcı analiz raporu oluşturmak için aşağıdaki adımları izleyin.

1. Oluşturmak istediğiniz raporun türüne bağlı olarak şu adımlardan birini izleyin:

    - **Varış yeri maliyeti \> Raporlar \> Etkinliğe göre etkinlik/sağlayıcı analizi**'ne gidin. Bu durumda, zaman tahminleri etkinliğe göre gruplandırılır.
    - **Varış yeri maliyeti \> Raporlar \> Sağlayıcıya göre etkinlik/sağlayıcı analizi**'ne gidin. Bu durumda, zaman tahminleri sağlayıcıya göre gruplandırılır.

    **Etkinliğe göre etkinlik/sağlayıcı analizi** iletişim kutusu veya **Sağlayıcıya göre etkinlik/sağlayıcı analizi** iletişim kutusu görüntülenir. Her iki iletişim kutusu da aynı seçenekleri sağlar.

1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, raporun çıktı biçimini seçmek için **Hedef** hızlı sekmesini kullanın.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, rapora dahil edilecek kayıtları daha da sınırlamak için **Rapora dahil edilecek kayıtlar** hızlı sekmesini kullanın.
1. Raporu oluşturmak için **Tamam**'ı seçin.

## <a name="voyage-costing-reports"></a>Seyahat maliyetlendirme raporları

Seyahat maliyetlendirme raporları, raporu oluştururken seçtiğiniz seçeneklere bağlı olarak maddelerin maliyetini ve folyo, sevkiyat konteyneri veya yolculuk başına ithalat maliyetlerini gösterir. Her seyahat maliyetlendirme raporu, bir seyahatin tahmini maliyetini gerçek maliyete kıyasla görüntülemenizi sağlar ve birkaç tanımlayıcı faktöre göre ayrılabilir.

Bir seyahat maliyetlendirme raporu oluşturmak için aşağıdaki adımları izleyin.

1. Oluşturmak istediğiniz raporun türüne bağlı olarak şu adımlardan birini izleyin:

    - **Varış yeri maliyeti \> Raporlar \> Maliyetlendirme \> Ayrı maliyetlere göre seyahat maliyetlendirmesi**'ne gidin. Bu durumda, ayrı maliyet seçeneği, maliyet türü kodu ve maliyet alanı başına ithalat maliyetlerini gösterir.
    - **Varış yeri maliyeti \> Raporlar \> Maliyetlendirme \> Raporlama kategorisine göre seyahat maliyetlendirmesi**'ne gidin. Bu durumda, ithalat maliyeti çeşitli raporlama kategorilerine ayrılır. Maliyet türleri raporlama kategorilerine göre gruplandırılır.

    **Ayrı maliyetlere göre seyahat maliyetlendirmesi** iletişim kutusu veya **Raporlama kategorisine göre seyahat maliyetlendirmesi** iletişim kutusu görüntülenir. Bu iletişim kutuları benzerdir. Bu prosedürün geri kalanında farklar ele alınacaktır.

1. **Raporlama kategorisine göre seyahat maliyetlendirmesi** iletişim kutusunu açtıysanız **Maliyet** alanında aşağıdaki değerlerden birini seçin:

    - **Maliyet değeri**: Değer, otomatik maliyetler kullanılarak hesaplanır veya maliyet alanında el ile oluşturulur.
    - **Tahmini**: Mallar teslim alındıktan sonra tahmini maliyet ayarlanır.
    - **Gerçek**: Sipariş faturalandıktan sonra, fiili maliyet faturadaki maliyete ayarlanır.
    - **En İyi**: Sistem, önceki üç seçenek arasından hangisi en doğruysa onu kullanacaktır. (Bu seçeneği belirlemenizi öneririz.)

1. Her maddenin maliyetini göstermek için **Madde başına** seçeneğini *Evet* olarak ayarlayın. Seyahat başına maliyetleri göstermek için *Hayır* olarak ayarlayın.
1. **Görünüm** bölümünde, maliyetin ayrılacağı kategorileri seçin.
1. **Boyutlar** bölümünde, rapora dahil edilecek boyutları seçin.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, raporun çıktı biçimini seçmek için **Hedef** hızlı sekmesini kullanın.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, rapora dahil edilecek kayıtları daha da sınırlamak için **Rapora dahil edilecek kayıtlar** hızlı sekmesini kullanın.
1. Raporu oluşturmak için **Tamam**'ı seçin.

## <a name="shipping-container-receipts-list"></a>Sevkiyat konteyneri girişlerinin listesi

Sevkiyat konteyneri girişlerinin listesi, beklenen tarihte veya daha önce ödenmesi gereken tüm teslim alınmamış miktarları içerir. Ambar personeli, bir sevkiyat konteynerinde beklenen malları tanımlamak için bu raporu kullanabilir. Ayrıca, malları bir sevkiyat konteynerinde teslim alındıklarında el ile doğrulamak için de kullanılabilir.

Sevkiyat konteyneri girişleri listesi oluşturmak için şu adımları izleyin.

1. **Varış yeri maliyeti \> Raporlar \> İzleme \> Sevkiyat konteyneri girişlerinin listesi**'ne gidin.
1. **Sevkiyat konteyneri girişlerinin listesi** iletişim kutusunda, **Beklenen tarih** alanında bir tarih belirtin. Bu tarihte veya bu tarihten önce teslim alınmamış miktarlar çıktıya dahil edilir.
1. **Boyutlar** bölümünde, rapora dahil edilecek boyutları seçin.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, raporun çıktı biçimini seçmek için **Hedef** hızlı sekmesini kullanın.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, rapora dahil edilecek kayıtları daha da sınırlamak için **Rapora dahil edilecek kayıtlar** hızlı sekmesini kullanın.
1. Raporu oluşturmak için **Tamam**'ı seçin.

## <a name="expected-delivery-report"></a>Beklenen teslimat raporu

Beklenen teslimat raporu seyahat, sevkiyat konteyneri, folyo, öğeler ve beklenen teslimat tarihi hakkında temel bilgileri içerir.

Bir beklenen teslimat raporu oluşturmak için aşağıdaki adımları izleyin.

1. **Varış yeri maliyeti \> Raporlar \> İzleme \> Beklenen Teslimat**'a gidin.
1. **Beklenen teslimat** iletişim kutusunda, **Beklenen tarih** alanında, malların son hedef ambara teslim edilmesinin beklendiği tarihi seçin. Beklenen tarihi bu tarihte veya bu tarihten önce olan ve henüz teslim alınmamış olan tüm seyahatler çıktıya dahil edilecektir.
1. İsteğe bağlı: **Satıcı hesabı** alanında, yalnızca belirli bir satıcıdan gelen teslimatları dahil etmek için bir satıcı hesabı seçin.
1. **Boyutlar** bölümünde, rapora dahil edilecek boyutları seçin.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, raporun çıktı biçimini seçmek için **Hedef** hızlı sekmesini kullanın.
1. Supply Chain Management'taki diğer rapor türlerinde yaptığınız gibi, rapora dahil edilecek kayıtları daha da sınırlamak için **Rapora dahil edilecek kayıtlar** hızlı sekmesini kullanın.
1. Raporu oluşturmak için **Tamam**'ı seçin.
