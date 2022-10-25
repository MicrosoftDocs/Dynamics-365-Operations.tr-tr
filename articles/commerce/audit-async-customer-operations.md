---
title: Genel merkezdeki müşteri işlemlerinin eşitlenmesini denetleme
description: Bu makalede, herhangi bir site kullanıcısı sorununu gidermeye yardımcı olmak için Microsoft Dynamics 365 Commerce headquarters'taki müşteri işlemlerinin eşitlemesinin nasıl denetleneceği açıklanır.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691111"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Genel merkezdeki müşteri işlemlerinin eşitlenmesini denetleme

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu makalede, herhangi bir site kullanıcısı sorununu gidermeye yardımcı olmak için Microsoft Dynamics 365 Commerce headquarters'taki müşteri işlemlerinin eşitlemesinin nasıl denetleneceği açıklanır.

Kuruluşlar, zaman uyumsuz biçimde müşteri oluşturma ve düzenleme yeteneğini benimsemeyi başlatmasından dolayı, site yöneticilerinin, site kullanıcı isteklerine veya işlem hatalarına göre işlemleri görüntülemek ve sorunları gidermek için bir yola ihtiyacı vardır. Bu senaryolarda, site yöneticileri müşteri oluşturma ve düzenleme işlemlerini denetleyebilmeli ve bir self servis modeli kullanarak hataları düzeltebilmelidir.

## <a name="customer-synchronization-status"></a>Müşteri eşitleme durumu

Müşteri yönetiminin ve ilgili özelliklerinin zaman uyumsuz modunu tercih ettiğinizde, Commerce headquarters yöneticilerinin, zaman uyumsuz müşterilerin Commerce headquarters'da zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup zamanlaması gerekir. Müşteri yönetim işlemlerinin eşitlenmesi, bu işler her çalıştırıldığında gerçekleşir. Daha fazla bilgi için bkz. [Zaman uyumlu müşteri oluşturma modu](async-customer-mode.md).

İşletme sahibi olarak, aşağıdaki işlemleri gerçekleştirebilirsiniz:

- Site kullanıcılarının tüm oluşturma/düzenleme işlemlerini görüntüleyin. Ayrıntılar, durum ve zaman damgasını içerir.
- Denetim günlüğünü daraltmak için müşteri tablosu alanlarından ve değerlerinden herhangi birini kullanarak işlemleri filtreleyin.
- İşlemleri üst düzeyde anlamak için, durum ayrıntılarıyla birlikte yapılan değişikliklerin kısa açıklamalarını görüntüleyin.
- Arızalar için sorunlu alanları düzenleyip düzeltin ve ardından belirli müşteri işlemlerini kaydedip eşitleyin.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Müşteri eşitleme durum sayfasındaki öğeler

Tüm eşitleme işlemlerinin bir listesini görüntülemek için Commerce headquarters'ta **Ticaret ve Satış \> Müşteriler \> Müşteri eşitleme durumu** bölümüne gidin. Aşağıdaki çizimde, **Müşteri eşitleme durumu** sayfasının bir örneği gösterilmektedir.

![Commerce headquarters'ta müşteri eşitleme durumu sayfası.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Varsayılan olarak **Müşteri senkronizasyon durumu** sayfasının sol tarafındaki müşteri senkronizasyon işlemleri listesi aşağıdaki sütunları içerir:

- Kanal adı
- Müşteri hesabı
- Zaman uyumsuz müşteri hesabı
- İşlem zaman damgası
- Müşteri eşitleme durumu

Sayfanın sağ üst köşesinde **Müşteri hesabı**, **Satış asenkron işlemi**, **Müşteri eşitleme durumu** ve **Bilenen son hata** değerleri gibi müşteri hesap ayrıntıları gösterilir.

**Değişiklik açıklaması** bölümü, çalıştırılan müşteri yönetimi işlemi türünün açıklamasını içerir (örneğin müşteri oluşturma, hesap güncelleştirme veya ayrıntılı eşitleme hatası).

**Müşteri öznitelikleri** bölümü, eski ve yeni değerlerle birlikte tüm müşteri özniteliklerini gösteren bir kılavuz içerir. Hataları düzeltmek için müşteri öznitelik değerlerinizi değiştirmek istiyorsanız bu bölümü düzenleyebilir ve ardından yeniden eşitleyebilirsiniz.
