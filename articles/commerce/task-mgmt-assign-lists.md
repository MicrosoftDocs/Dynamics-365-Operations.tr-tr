---
title: Mağazalara veya personele görev listeleri atama
description: Bu makalede, Microsoft Dynamics 365 Commerce'ta mağazalara veya çalışanlara görev listeleri atama açıklanmaktadır.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: 8aa1d61e235244ee9400419e51da638c059892e5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284670"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Mağazalara veya personele görev listeleri atama

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'ta mağazalara veya çalışanlara görev listeleri atama açıklanmaktadır.

Dynamics 365 Commerce'teki görev yönetimi, bir görev listesini birden fazla mağazaya veya çalışana veya mağaza ve çalışanların bir birleşimine atamanıza olanak tanır. Örneğin, 20 mağaza için bir bölgesel yönetici, **tatil sezonuna hazırlık** görev listesini tüm 20 mağazalara atamak isteyebilir.

## <a name="start-the-task-list-assignment-process"></a>Görev listesi atama işlemini Başlat

Görev listesi atama işlemini başlatmak için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.
1. Atanacak görev listesini seçin.
1. **İşlemi başlat**'ı seçin.
1. **İşlem Başlat** iletişim kutusundaki **genel** sekmesinde, **işlem adı** alanına bir ad girin (örneğin, **Doğu bölge depoları**).
1. **Hedef Tarih** alanına bir tarih girin.
1. Görev listesini mağazalara atamak için **mağazalar** sekmesinde, depoları bulup seçmek için **organizasyon hiyerarşisi** filtresini kullanın.

    Görev listesini çalışanlara atamak için **çalışanlar** sekmesinde, çalışanları bulun ve seçin.

1. İşlemi başlatmak için **Tamam**'ı seçin. Görevler listesi seçilen mağazalara veya çalışanlara atanır.

Aşağıdaki şekil, **işlem Başlat** iletişim kutusunda depoların nasıl bulunacağı ve seçgeleile ilgili bir örnek göstermektedir.

![İşlem Başlat iletişim kutusunda depoları bulma ve seçme.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Görev listelerini yinelenen bir temelde ata

Perakende, bazen "Perşembe kapatma denetim listesi" veya "ay denetim listesinin ilk günü" gibi görevlere tekrarlayan görevler de içerebilir. Bu nedenle, görev listesini yinelenen bir temelde atamak isteyebilirsiniz.

1. **Retail ve Commerce \> görev yönetimi \>görev yönetimi idaresi**'ne gidin.
1. Atanacak görev listesini seçin.
1. **İşlemi başlat**'ı seçin.
1. **İşlem Başlat** iletişim kutusundaki **genel** sekmesinde, **işlem adı** alanına bir ad girin.
1. **Yineleme** seçeneğini **Evet** olarak ayarlayın.
1. **Gün cinsinden tekrarlama hedefi Tarih farkı** alanında, gün sayısını girin. Örneğin, **4** girerseniz, hedef tarih tekrarlama tarihi artı dört gün olarak hesaplanır.
1. **Arka planda çalıştır** sekmesinde **Tekrar** ı seçin.
1. **Tekrarı tanımla** iletişim kutusunda sıklık ölçütünü girin ve **Tamam** 'ı seçin.

Aşağıdaki çizimde, **yinelenme tanımla** iletişim kutusunda sıklık ölçütünün nasıl girmenin bir örneği gösterilmektedir.

![Tekrarı tanımla iletişim kutusunda sıklık ölçütünü girme.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Görev listesi durumunu izle

Bir bölgesel yönetici veya mağaza yöneticisiyseniz, birden fazla mağazaya veya çalışana atanmış görev listelerinin durumunu izlemek isteyebilirsiniz. Böylece, kendilerine atanan görevleri zamanında tamamlamadıkları mağazalar veya işçilere göre izleyebilirsiniz. Commerce arka ofisi, görev listelerinin durumunu görüntülemenizi, görevlerin yeniden atanmasını veya bir görevin durumunu değiştirmenizi sağlar.

Tüm görevlerin görev listesi durumunu izlemek için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> görev yönetimi \>görev yönetimi süreçleri**'ne gidin.
1. Çeşitli mağazalara atanan tüm görev listelerinin durumunu görüntülemek için **tüm görev listeleri** sekmesini seçin.

Size atanan tüm görevlerin görev listesi durumunu izlemek için, aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> görev yönetimi \>görev yönetimi süreçleri**'ne gidin.
1. Size atanan görevlerin durumunu görüntülemek veya güncelleştirmek için **Görevlerim** veya **tüm görevler** sekmesini seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Görev yönetimine genel bakış](task-mgmt-overview.md)

[Görev yönetimini yapılandırma](task-mgmt-configure.md)

[Görev listeleri oluşturma ve görev ekleme](task-mgmt-create-lists.md)

[POS'ta görev yönetimi](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
