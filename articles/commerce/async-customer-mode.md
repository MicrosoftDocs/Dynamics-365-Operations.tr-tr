---
title: Zaman uyumsuz müşteri oluşturma modu
description: Bu konu, Microsoft Dynamics 365 Commerce'teki zaman uyumsuz müşteri oluşturma modunu açıklamaktadır.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 43418b61778d187364d4d52a05178078a37623eb
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984282"
---
# <a name="asynchronous-customer-creation-mode"></a>Zaman uyumsuz müşteri oluşturma modu

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'teki zaman uyumsuz müşteri oluşturma modunu açıklamaktadır.

Commerce'te, iki müşteri oluşturma modu vardır: zaman uyumlu (veya senkron) ve zaman uyumsuz (veya asenkron). Varsayılan olarak, müşteriler zaman uyumlu olarak oluşturulur. Başka bir deyişle, bunlar Commerce genel merkezinde gerçek zamanlı olarak oluşturulur. Zaman uyumlu müşteri oluşturma modu, tüm kanallar arasında yeni müşteriler hemen aranabilir hale geldiği için yararlıdır. Ancak, bir dezavantajı da vardır. Commerce genel merkezine [Commerce Data Exchange: Gerçek Zamanlı Servis](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) çağrıları oluşturduğundan, birçok eşzamanlı müşteri oluşturma çağrısı yapılırsa performans etkilenebilir.

**Zaman uyumsuz modda müşteri oluştur** seçeneği mağazanın işlevsellik profilinde **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Channel kurulum \> çevrimiçi mağaza kurulumu \> İşlev profilleri**), gerçek zamanlı Servis çağrıları kanal veritabanında müşteri kayıtları oluşturmak için kullanılmaz. Zaman uyumsuz müşteri oluşturma modu, Commerce genel merkezinin performansını etkilemez. Bir geçici genel benzersiz tanımlayıcı (GUID), her yeni zaman uyumsuz müşteri kaydına atanır ve müşteri hesap kodu olarak kullanılır. Bu GUID, satış noktası (POS) kullanıcıları için gösterilmez. Bunun yerine, bu kullanıcılar müşteri hesap kodu olarak **bekleyen eşitlemeyi** görürler.

> [!IMPORTANT]
> POS çevrimdışı olduğunda zaman uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, zaman uyumlu ve zaman uyumsuz müşteri oluşturma modları arasındaki seçiminiz ne olursa olsun Commerce genel merkezi yöneticilerinin **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi (eski adıyla **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi) ve **1010** işi için yinelenen bir toplu iş oluşturması ve zamanlaması gerekir. Böylece tüm zaman uyumsuz müşteriler Commerce genel merkezindeki zaman uyumlu müşterilere dönüştürülür.

## <a name="async-customer-limitations"></a>Zaman uyumsuz müşteri sınırlamaları

Zaman uyumsuz müşteri işlevinde şu sınırlamalar vardır:

- Müşteri Commerce genel merkezinde oluşturulmadıysa ve yeni müşteri hesap kodu kanala geri eşitlenmediyse zaman uyumsuz müşteri kayıtları düzenlenemez.
- Yeni müşteri hesap kodu kanalla geri eşitlenmedikçe, bağlılık programı kartları zaman uyumsuz müşterilere verilemez.

## <a name="async-customer-enhancements"></a>Zaman uyumsuz müşteri iyileştirmeleri

Commerce 10.0.24 sürümü itibarıyla, **Özellik yönetimi** çalışma alanında **Geliştirilmiş zaman uyumsuz müşteri oluşturmayı etkinleştir** özelliğini etkinleştirebilirsiniz. Bu özellik, aşağıdaki yöntemlerle, POS ve e-ticaretteki zaman uyumsuz ve zaman uyumlu müşteri oluşturma modları arasındaki boşlukta köprü oluşturur:

- İlişkiler zaman uyumsuz müşterilerle ilişkilendirilemez.
- Unvanlar, zaman uyumsuz müşterilere eklenebilir.
- Zaman uyumsuz müşteriler ikincil e-posta adresleri ve telefon numaraları kaydedilemez.

Commerce 10.0.22 sürümü itibarıyla, **Özellik yönetimi** çalışma alanında **Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir** özelliğini etkinleştirebilirsiniz. Bu özellik, yeni oluşturulan müşteri adreslerinin hem zaman uyumlu müşteriler hem de zaman uyumsuz müşteriler için zaman uyumsuz olarak kaydedilmesine olanak tanır.

Daha önce bahsedilen özellikleri etkinleştirdikten sonra zaman uyumsuz müşterilerin Commerce genel merkezinde zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Zaman uyumsuz modundan müşteri ve iş ortaklarını eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup planlamanız gerekir.

### <a name="customer-creation-in-pos-offline-mode"></a>POS Çevrimdışı modunda müşteri oluşturma

Daha önce bahsedildiği gibi, POS çevrimdışı olduğunda zaman uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, Commerce genel merkezi yöneticilerinin zaman uyumsuz müşterilerin Commerce genel merkezinde zaman uyumlu müşterilere dönüştürülmesi için **P işi**, **Zaman uyumsuz modundan müşteri ve iş ortaklarını eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup planlaması gerekir.

> [!NOTE]
> **Paylaşılan müşteri veri tablolarını filtrele** seçeneği, **Commerce kanal şeması** sayfasında **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Genel merkez kurulumu \> Commerce Planlayıcı \> Kanal veritabanı grubu**), müşteri kayıtları POS çevrimdışı modunda oluşturulmaz. Daha fazla bilgi için bkz. [Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Ek kaynaklar

[Mağazalardaki müşteri yönetimi](customer-mgmt-stores.md)

[Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme](convert-async-to-sync.md)

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
