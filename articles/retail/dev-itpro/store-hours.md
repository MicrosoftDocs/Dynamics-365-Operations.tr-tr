---
title: Mağaza çalışma saatleri oluşturma ve güncelleştirme
description: Bu konu, Retail Headquarters'ta mağaza saatlerini oluşturmayı ve güncelleştirmeyi açıklar.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 1b55b91246b22951f4e1d148f59444423e1d8a3d
ms.sourcegitcommit: e54607a2c80bec4db05045825914f50947f6e31e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917524"
---
# <a name="create-and-update-store-hours"></a>Mağaza çalışma saatleri oluşturma ve güncelleştirme

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Genel bakış

Perakendeciler tek bir yerden, coğrafi bölgeler arasında farklı mağazalar için mağaza saatleri oluşturabilir, bakımını yapabilir ve bunları yönetebilir. Depolama saatleri daha sonra satış noktasında (POS) gösterilebilir. Böylece kasiyerler, mağaza saatlerini müşterilerle paylaşabilir ve diğer mağazalarda stoğa ilgilenen alışverişçilere daha iyi yardımcı olabilir. Müşteriler mağazaya sonradan geri dönmek istiyorsanız, mağaza saatleri girişlere de yazdırılabilir.

Farklı kanallar arasında birden fazla depolama saati yapılandırılabilir. Bu kanallar arasında gerçek mekan depoları, çağrı merkezleri, mobil aygıtlar ve e-ticaret siteleri sayılabilir.

Bir müşterinin farklı bir mağaza için bir malzeme çekme siparişi varsa, malzeme çekme bu mağazada kullanılabilir olduğunda, kasiyer program seçebilir. Mağaza arama, tarihlere ve depolama zamanlarında bir başvuru sağlayacaktır. Kasiyer bir tarih ve yerleşim seçebilir ve mağaza saatlerini içeren bir teslim alma girişi de yazdırabilir.

Bu işlevsellik, Microsoft Dynamics 365 for Retail sürümler 8.1.2 ve sonraki sürümlerinde kullanılabilir.

## <a name="configure-store-hours"></a>Mağaza saatlerini yapılandır

Mağaza saatlerini yapılandırmak için şu adımları izleyin.

1. **Retail** \> **Kanal Kurulumu** \> **Mağaza saatleri**'ne gidin.
2. Yeni bir mağaza saatleri şablonu oluşturmak için **Yeni**'yi seçin. Varolan bir şablonu kullanmak için, sol bölmedeki şablonu seçin.
3. **Aralık Ekle** iletişim kutusunda Tarih aralığını, mağaza saatlerini ve gerekli tüm tatilleri tanımlayın.

    - Mağaza saatleri değişmiyorsa, **bitiş tarihi** alanında **hiçbir zaman bitmemesi** seçeneğini belirleyin.
    - Depolama saatleri belirli bir ay, hafta veya gün için ise, **başlangıç tarihi** ve **bitiş tarihi** alanlarında uygun tarihleri ayarlayın.

    > [!NOTE]
    > Örtüşen başlangıç ve bitiş tarihlerine sahip birden çok şablon oluşturabilirsiniz. Bu nedenle, örneğin, farklı saat dilimlerindeki Mağazalar için mağaza saatleri tanımlayabilirsiniz.

    ![Aralık ekle iletişim kutusu](../dev-itpro/media/Storehours1.png "Aralık ekle iletişim kutusu")

4. Mağaza saatleri şablonunu, kullanılacak mağazalar ile ilişkilendirin. **Kuruluş düğümlerini Seç** iletişim kutusunda, şablonun ilişkilendirilmesi gereken depoları, bölgeleri ve organizasyonları seçin.

    - Her bir mağaza ile yalnızca bir depolama saatleri şablonu ilişkilendirilebilir.
    - Mağaza, bölge veya organizasyon seçmek için ok düğmelerini kullanın. Takvim mağazalar veya mağaza grupları tarafından kullanılabilir ve burada referans olarak görünür.

    ![Kuruluş düğümleri seç iletişim kutusu](../dev-itpro/media/Storehours2.png "Kuruluş düğümleri seç iletişim kutusu")

5. **Dağıtım zamanlaması** sayfasında **1070** ve **1090** işlerini çalıştırarak mağaza saatlerini POS'ta kullanılabilir kılın.

## <a name="add-store-hours-to-printed-receipts"></a>Yazdırılmış fişlere mağaza saatlerini ekle

Yazdırılan POS alış irsaliyelerine mağaza saatleri eklemek için bu adımları izleyin.

1. Fiş tasarımcısını açın.
2. Sol alt köşedeki **Alt bilgi**'yi seçin.
3. **Mağaza saatleri** öğesini sol panodan fiş şablonunun altındaki alt bilgi bölmesine taşıyın.
4. Varsayılan etiketi ihtiyaç duyduğunuz şekilde **Mağaza saatleri** öğesinde düzenleyebilirsiniz.
5. Fişi kaydedin ve fiş tasarımcısını kapatın.
6. **Dağıtım zamanlaması** sayfasında **1070** ve **1090** işlerini çalıştırın.
7. POS'ta oturum açın.
8. Bir satışı tamamlayın ve bir makbuz yazdırmak için seçin.

POS makbuzları şimdi mağaza saatlerini içerir. Şablonda herhangi bir tatil varsa, bunlar alındı bilgisi içinde gösterilir.

![Fiş örneği](../dev-itpro/media/Storehours3.png "Fiş örneği")
