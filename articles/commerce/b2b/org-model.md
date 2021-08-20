---
title: B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma
description: Bu konuda, işletmeler arası (B2B) kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma yöntemi açıklanmıştır.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0602e0f4e36beda06f47314f40b59967272469755d1b9959432e86f407c098e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738089"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma

[!include [banner](../../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te işletmeler arası (B2B) kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma yöntemi açıklanmıştır.

Commerce Headquarters'da iş ortağı kuruluşları, müşteri ve müşteri hiyerarşisi varlıklarıyla temsil edilir. İş ortağı kuruluş ve kullanıcıları, müşteri olarak temsil edilir ve müşteri hiyerarşileri bu müşterileri birbirleriyle ilişkilendirmek için kullanılır.

Bir B2B e-ticaret sitesine katılmak için iş ortağı isteği onaylandığında, aşağıdaki eylemler gerçekleştirilir:

- Sistemde iki yeni müşteri kaydı oluşturulur: iş ortağı kuruluş için **Tür Kuruluş** müşteri kaydı ve istek sahibi (diğer bir deyişle, talebi gönderen iş ortağı kullanıcı) için **Tür Kişi** müşteri kaydı.
- **Müşteri\> Müşteri hiyerarşisi** altında yeni bir müşteri hiyerarşisi kaydı oluşturulur. Bu kayıt aşağıdaki başlık özelliklerine sahiptir:

    - **Müşteri hiyerarşisi kimliği** – Müşteri hiyerarşisi için benzersiz bir kimlik. Bu kimlik, Commerce Headquarters'daki paylaşılan Commerce parametrelerinde tanımlanan numara serisini kullanır.
    - **Ad** - İş ortağının kuruluş adı ekleme isteğinde belirttiği kuruluş adı.
    - **Amaç** – Bu özellik önceden tanımlanmış **B2B kuruluşu** değerine ayarlanır.
    - **Kuruluş** - İş ortağının müşteri kimliği.

Müşteri hiyerarşisi kaydının ayrıntıları aşağıdadır:

- İstek sahibinin müşteri kaydı, müşteri hiyerarşisiyle ilişkilidir.
- Yönetici rolü istek sahibi ile ilişkilendirilir.

Yönetici, bir B2B sitesinde iş ortağı kuruluşuna daha fazla kullanıcı eklediğinde, Commerce Headquarters'da her bir kullanıcı için yeni bir müşteri kaydı oluşturulur. Bu müşteri kaydı aynı zamanda iş ortağı için ilgili müşteri hiyerarşisi kaydına eklenir ve bir "Kullanıcı" rolüne sahip olur.

> [!NOTE]
> Çoğu durumda, bir hiyerarşideki tüm müşteri kayıtlarının karşılık gelen özellik değerleri eşleşmelidir. Örneğin, tüm iş ortağı kullanıcıların ürünlerle ilgili benzer fiyatları alması gerektiğinden, fiyat grubu ve ilişkili yapılandırmaların eşleşmesi gerekir. Ancak, sistem bu tutarlılığı zorunlu kılmaz. Bu nedenle, ilgili Commerce Headquarters kullanıcıları belirli bir hiyerarşideki tüm müşteriler için özellik değerlerinin ve yapılandırmaların eşleşmesini sağlamaya karşı sorumludur.

Commerce Headquarters kullanıcıları, hiyerarşideki tüm müşteri kayıtlarının özellik değerlerine yan yana görünümde bakabilir. Açılan menüden sekme adlarını seçerek ilgili müşteri kaydı özelliklerini seçin. Kullanıcılar bu görünümdeki özellik değerlerini doğrudan görüntüleyebilir ve düzenleyebilir. Alternatif olarak, yöneticinin müşteri kaydındaki tüm değerleri tüm kullanıcı müşteri kayıtlarına uygulamak istiyorsanız, Müşteri hiyerarşisi ayrıntılarında **Geçersiz kıl**'ı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[B2B e-ticaret sitesi ayarlama](set-up-b2b-site.md)

[B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme](manage-b2b-users.md)

[B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma](payment-method.md)

[B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]