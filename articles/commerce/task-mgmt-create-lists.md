---
title: Görev listeleri oluşturma ve görev ekleme
description: Bu makalede, Microsoft Dynamics 365 Commerce'tegörev listeleri oluşturma ve bunlara görev ekleme açıklanmaktadır.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a299be239d911e4605ed26625a313c93bd3020b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881643"
---
# <a name="create-task-lists-and-add-tasks"></a>Görev listeleri oluşturma ve görev ekleme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'tegörev listeleri oluşturma ve bunlara görev ekleme açıklanmaktadır.

Bir *görev*, bir kişinin belirli bir iş parçasını veya belirtilen bir vade tarihinden önce veya bu tarihten önce tamamlanması gereken bir eylemi tanımlar. Dynamics 365 Commerce'De bir görev, ilgili kişi hakkında ayrıntılı yönergeler ve bilgiler içerebilir. Ayrıca, üretkenliği artırmaya yardımcı olmak ve görev sahibinin görevi etkili şekilde tamamlaması için gereken bağlamı sağlamak amacıyla, geri-ofis operasyonları, satış noktası (POS) işlemleri veya site sayfaları ile ilgili bağlantılar içerebilir.

*Görev listesi*, iş sürecinin bir parçası olarak tamamlanması gereken görevler topluluğudur. Örneğin, yeni bir çalışanın ekleme sırasında tamamlanması gereken bir görev listesi, akşam vardiyaları olan kasiyerlerin görev listesi veya depoyu yaklaşan bir tatil döneminde hazırlamak için tamamlanması gereken bir görev listesi olabilir. Commerce'te, hedef tarihi olan her görev listesi herhangi bir sayıda mağazaya veya çalışana atanabilir ve yinelenecek şekilde konfigüre edilebilir.

Hem Yöneticiler hem de çalışanlar, ticari ofislerinde görev listeleri oluşturabilir ve bunları bir mağaza kümesine atayabilirler.

## <a name="create-a-task-list"></a>Bir görev oluştur

Görev listesi oluşturmak için şu adımları izleyin.

1. **Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.
1. **Yeni**'yi seçin ve sonra **ad**, **Açıklama** ve **sahip** alanlarına değerleri girin.
1. **Kaydet**'i seçin.

## <a name="add-tasks-to-a-task-list"></a>Görev listesine görev ekleme

Bir görev listesine görevler eklemek için bu adımları izleyin.
 
1. Görev eklemek için, varolan bir görev listesinin **görevler** hızlı sekmesinde **yeni**'yi seçin.
1. **Yeni görev oluştur** iletişim kutusunda, **ad** alanına görev için bir ad girin.
1. **Son veri bitiş tarihi** alanına, artı veya eksi bir tamsayı değeri girin. Örneğin görev listesinin vade tarihinden iki gün önce tamamlanması gerekiyorsa, **-2** girin.
1. **Notlar** alanına ayrıntılı yönergeler girin.
1. **İlgili kişi** alanında, yardım gerekirse görev sahibinin başvurmasının gerektiği konu uzmanı adını girin.
1. **Görev bağlantısı** alanına, görevin doğasına göre bir bağlantı girin.

> [!TIP]
> Görev listesi oluştururken bir kişiye **görev atamak** için atanan alanını kullanabilseniz de, görev listesi oluşturma sırasında görev atamaktan kaçınmanızı öneririz. Bunun yerine, belirli Mağazalar için liste örneği oluşturulduktan sonra görevleri atayın.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Çalışanların üretkenliğini artırmaya yardımcı olması için görev bağlantılarını kullan

Commerce, bir satış raporu çalıştırmak, yeni çalışan yönlendirmesi için çevrimiçi eğitim videosunu görüntülemek veya bir arka ofis operasyonu gerçekleştirmek gibi, görevleri belirli POS operasyonlarına bağlamanızı sağlar. Bu özellik, görev sahiplerinin bir görevi etkili şekilde tamamlamak için gereken bilgileri edinmesine yardımcı olur.

Görev oluştururken görev bağlantıları eklemek için, aşağıdaki adımları izleyin.

1. Varolan bir görev listesinin **görevler** hızlı sekmesinde **Düzenle**'yi seçin.
1. **Görev bağlantısı** alanındaki **Görevi Düzenle** iletişim kutusunda aşağıdaki seçeneklerden bir veya birkaçını seçin:

    - "Ürün takımları" gibi bir arka ofis işlemi yapılandırmak için **menü öğesini** seçin.
    - "Satış raporları" gibi bir POS işlemini konfigüre etmek için **POS işlemi** seçin.
    - Mutlak bir URL konfigüre etmek için **URL**'yi seçin.

Aşağıdaki resimde, **görevi düzenle** iletişim kutusunda görev bağlantılarının seçimi gösterilmektedir.

![Düzenle görev iletişim kutusunda görev bağlantıları seçme.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Bir göreve bağlanabilmesi için bir POS operasyonu konfigüre et

Bir göreve bağlanabilmesi için bir POS operasyonu konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Operasyonlar** öğelerini seçin.
1. **Düzenle**'yi seçin, POS işlemini bulun ve bunun için **Görev yönetimini etkinleştir** onay kutusunu seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Görev yönetimine genel bakış](task-mgmt-overview.md)

[Görev yönetimini yapılandırma](task-mgmt-configure.md)

[Mağazalara veya personele görev listeleri atama](task-mgmt-assign-lists.md)

[POS'ta görev yönetimi](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
