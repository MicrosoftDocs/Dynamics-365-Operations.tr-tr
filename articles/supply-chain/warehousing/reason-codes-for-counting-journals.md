---
title: Stok sayımı neden kodları
description: Bu konu sayım görevleri için neden kodlarının nasıl ayarlanacağını ve uygulanacağını açıklar.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 1025dd00db2e8b87e3c76e3047a7cf470a2d6641
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439093"
---
# <a name="reason-codes-for-inventory-counting"></a>Stok sayımı neden kodları

[!include [banner](../includes/banner.md)]

Neden kodları sayım işleminin sonucunu ve bu işlem sırasında oluşan tutarsızlıkları analiz etmenize olanak tanır. Kırılmış palet veya stok örneklerine dayanan stok ayarlaması gibi bir sayım yapma nedeni belirtebilirsiniz.

## <a name="recommendation"></a>Öneri

Sistemi ayarlamadan önce neden kodları ile çalışmak için bir strateji tanımlamanızı öneririz. Örneğin, aşağıdaki soruları yanıtlamaya çalışın:

- Neden kodları ambarlarda zorunlu olmalı mı?
- Neden kodları bazı maddelerde zorunlu mu yoksa veya isteğe bağlı mı olmalı?
- Ne kadar neden kodu gerekli?
- Barkod tarayıcısı kullanıcıları neden kodlarını nasıl kullanacak? Neden kodları önceden seçilmiş mi, zorunlu mu yoksa düzenlenemez mi olsun?
- Ambar çalışanları için mobil tarayıcıda farklı neden kodu davranışı gerekli mi? Yanıtınız evet ise, daha fazla menü öğesi oluşturabilir ve bunları farklı kişilere atayabilirsiniz.

## <a name="where-reason-codes-apply"></a>Neden kodlarının uygulandığı yerler

Birden fazla neden kodu ilkesi oluşturabilirsiniz ve her neden kodu ilkesinin iki sayım nedeni kodu ilkesi olabilir. Sayım neden kodu ilkeleri ambar düzeyi veya madde düzeyinde kullanılabilir.

## <a name="set-up-reason-code-policies"></a>Neden kodu ilkeleri ayarlama

1. **Stok yönetimi** \> **Kurulum** \> **Stok** \> **Sayım neden kodu ilkeleri**'ni seçin ve yeni bir neden kodu ilkesi oluşturun.
2. **Sayım neden kodu türü** alanında **Zorunlu** veya **İsteğe bağlı**'yı seçerek neden kodunun aşağıdaki sayım günlüklerinden birinde isteğe bağlı mı yoksa zorunlu bir eylem mi olması gerektiğini belirtin:

    - Döngü Sayısı (mobil cihaz)
    - Nokta Sayısı (mobil cihaz)
    - Eşik Sayısı (mobil cihaz)
    - Ayarlama etkin (mobil cihaz)
    - Ayarlama devre dışı (mobil cihaz)
    - Sayım Günlüğü (zengin istemci)

Ayrıca tek tek ambarlar ve ürünler için de neden kodu ayarlayabilirsiniz. Ürünler için neden kodu ayarı ambar ayarını yok sayabilir.

## <a name="mandatory-reason-codes"></a>Zorunlu neden kodları

**Zorunlu** parametresi ambarlar veya maddeler için neden kodu yapılandırmasında ayarlanırsa, sayım günlüğü tamamlanamaz ve bir neden kodu sağlanan kadar kapatılır.

### <a name="set-up-reason-codes-for-warehouses"></a>Ambarlar için neden kodları ayarlama

1. **Stok yönetimi** \> **Kurulum** \> **Stok dökümü** \> **Ambarlar**'ı seçin.
2. **Ambar** sekmesindeki **Sayım neden kodu ilkesi** alanında, aşağıdaki seçeneklerden birini seçin:

    - **Boş** – Madde için ayarlanan parametre sayım günlüklerinin ürün için zorunlu olup olmadığını belirlemek için kullanılır.
    - **Zorunlu** – Ambar için sayım günlüklerinde daima bir neden kodu gereklidir.
    - **İsteğe bağlı** – Ambar için sayım günlüklerinde bir neden kodu gerekli değildir.

### <a name="set-up-reason-codes-for-products"></a>Ürünler için neden kodları ayarlama

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılan ürünler**'i seçin.
2. **Ürün** sekmesinde **Sayım neden kodu ilkesi** 'ni ve aşağıdaki seçeneklerden birini seçin:

    - **Boş** – Ambar için ayarlanan parametre sayım günlüklerinin ürün için zorunlu olup olmadığını belirlemek için kullanılır.
    - **Zorunlu** – Ürün için sayım günlüklerinde daima bir neden kodu gereklidir. Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.
    - **İsteğe bağlı** – Ürün için sayım günlüklerinde bir neden kodu gerekli değildir. Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.

### <a name="use-reason-codes-in-counting-journals"></a>Sayım günlüklerinde neden kodları kullanma

Bir sayım günlüğüne, aşağıda türde sayımlar için neden kodları ekleyebilirsiniz:

- Döngü Sayımı
- Nokta Sayımı
- Eşik Sayımı
- Ayarlama etkin
- Ayarlama devre dışı

Neden kodları **Sayım günlüğü** türündeki sayım günlüklerindeki günlük satırlarına eklenir.

1. **Stok Yönetimi** \> **Günlük girişleri** \> **Madde sayımı** \> **Sayım**'a gidin.
2. Sayım günlüğü satır ayrıntılarında **Sayım neden kodu** alanında, bir seçenek belirleyin.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Sayım geçmişini neden kodları tarafından kaydedildiği gibi görme

- **Stok yönetimi** \> **Sorgular ve raporlar** \> **Sayım geçmişi**'ni ve ardından **Sayım neden kodu** alanında bir neden kodu aracılığıyla kaydedilmiş olan sayım geçmişini görüntüleyin.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Miktar ayarlaması için neden kodu kullanma

1. **Eldeki stok** sayfasında **Miktarı ayarla**'yı seçin. **Eldeki stok** sayfasını farklı yollarla açabilirsiniz. Örneğin **Stok yönetimi** \> **Sorgular ve raporlar** \> **Eldeki stok**'a gidin.
2. **Miktarı ayarla**'yı ve daha sonra **Sayım neden kodu** alanından neden kodu seçin.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Mobil cihaz menü öğeleri için neden kodları yapılandırma

Bir mobil cihaz menü öğesinde herhangi bir sayım türü için neden kodları yapılandırabilirsiniz. Mobil cihaz menü öğesi yapılandırması aşağıdaki bilgileri içerir:

- Neden kodunun mobil cihaz çalışanına sayım sırasında gösterilip gösterilmeyeceği
- Mobil cihaz menü öğesinde gösterilen varsayılan neden kodu.
- Kullanıcının neden kodunu düzenleyip düzenleyemeyeceği.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Mobil cihazda neden kodları ayarlama

1. **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menüsü öğeleri**'ni seçin.
2. **Döngü sayısı** sekmesinde **Döngü sayımı**'nı seçin.
3. **Varsayılan sayım neden kodu** alanında, sayım mobil cihaz menü öğesi kullanılarak yapıldığında kaydedilmesi gereken varsayılan neden kodunu ayarlayın.
4. **Sayım neden kodunu görüntüle** alanında, her fark kaydedildikten sonra neden kodunun gösterilmesi için **Satır**'ı seçin. Alternatif olarak, neden kodunun gösterilmemesi gerekiyorsa **Gizle**'yi seçin.
5. **Sayım neden kodunu düzenle** seçeneğini **Evet** veya **Hayır** olarak ayarlayın. Bu seçeneği **Evet** olarak ayarlarsanız, çalışan sayım sırasında mobil cihazda gösterildiğinde neden kodunu düzenleyebilir.

> [!NOTE]
> **Döngü sayımı** düğmesi sayımın yapılabileceği herhangi bir mobil cihaz menüsünde etkinleştirilebilir. Örnek nokta sayısı, kullanıcı yönlendirmeli iş ve sistem yönlendirmeli iş için menü öğelerini içerir.

## <a name="cycle-count-approvals"></a>Döngü sayımı onayları

Bir sayım onaylanmadan önce kullanıcı sayımla ilişkili neden kodunu değiştirebilir. Sayım onaylandığında neden kodu sayım günlüğü satırlarına girilir.

### <a name="modify-cycle-count-approvals"></a>Döngü sayımı onaylarını değiştirme

1. **Ambar yönetimi** \> **Döngü sayımı** \> **İnceleme bekleyen döngü sayımı işi**'ni seçin.
2. **Döngü sayımı**'nı seçin ve daha sonra **Neden kodu** alanından yeni bir neden kodu seçin.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Ayarlama etkin ve Ayarlama devre dışı için mobil cihaz menü öğesini değiştirme

1. **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**'ni ve ardından **Ayarlama etkin ve devre dışı**'nı seçin.
2. **Mevcut işi kullan** seçeneğinde **Hayır**'ı işaretleyin.
3. **İş oluşturma işlemi** alanında **Ayarlama etkin**'i seçin.

İş oluşturma işlemi sırasında **Ayarlama etkin** veya **Ayarlama devre dışı** seçildiğinde aşağıdaki alanlar mobil cihaz menüsüne eklenir:

- Varsayılan sayım nedeni kodu
- Sayım nedeni kodunu görüntüle
- Sayım nedeni kodunu düzenle


[!INCLUDE[footer-include](../../includes/footer-banner.md)]