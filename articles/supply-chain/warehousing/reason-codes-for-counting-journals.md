---
title: Stok sayımı neden kodları
description: Bu makale sayım görevleri için neden kodlarının nasıl ayarlanacağını ve uygulanacağını açıklar.
author: perlynne
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountingReasonCodePolicy, InventCountingReasonCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 7d182f1d979543eeec700924d2bd180ee06be8ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857126"
---
# <a name="reason-codes-for-inventory-counting"></a>Stok sayımı neden kodları

[!include [banner](../includes/banner.md)]

Neden kodları sayım işleminin sonucunu ve bu işlem sırasında oluşan tutarsızlıkları analiz etmenize olanak tanır. Kırılmış palet veya stok örneklerine dayanan stok ayarlaması gibi bir sayım yapma nedeni belirtebilirsiniz. Aynı zamanda, her stok ayarlamasının nedenine bağlı olarak eldeki stok ayarlamalarının değerini uygun mahsup hesap defterine nakletmek için ayarlama işlevini kullanabilirsiniz.

## <a name="recommendation"></a>Öneri

Sistemi ayarlamadan önce neden kodları ile çalışmak için bir strateji tanımlamanızı öneririz. Örneğin, aşağıdaki soruları yanıtlamaya çalışın:

- Neden kodları ambarlarda zorunlu olmalı mı?
- Neden kodları bazı maddelerde zorunlu mu yoksa veya isteğe bağlı mı olmalı?
- Ne kadar neden kodu gerekli?
- Ayarlamalar için neden kodlarının sınırlı listesini önceden seçmeniz gerekir mi?
- Barkod tarayıcısı kullanıcıları neden kodlarını nasıl kullanmalı? Neden kodları önceden seçilmiş mi, zorunlu mu yoksa düzenlenemez mi olsun?
- Ambar çalışanları için mobil tarayıcıda farklı neden kodu davranışı gerekli mi? Yanıtınız evet ise, daha fazla menü öğesi oluşturabilir ve bunları farklı kişilere atayabilirsiniz.
- Neden kodları mali mahsup hesap defterine nakledilmeyi yönlendirir mi?

## <a name="turn-on-reason-code-features-in-your-system"></a>Sisteminizdeki neden kodu özelliklerini açma

Bu makalede açıklanan tüm özellikleri sisteminizde görmüyorsanız muhtemelen *Mahsup hesaplara bağlı yapılandırılabilir neden kodlarını kullanarak eldeki stok ayarlamalarını deftere nakletme* özelliğini açmanız gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Mahsup hesaplara bağlı yapılandırılabilir neden kodlarını kullanarak eldeki stok ayarlamalarını deftere nakletme*

## <a name="set-up-reason-codes"></a>Neden kodlarını ayarla

### <a name="set-up-reason-code-policies"></a>Neden kodu ilkeleri ayarlama

Sayım nedeni kodlarının ne zaman ve nasıl uygulanacağını denetlemek için birden çok neden kodu ilkesi oluşturabilirsiniz. Her neden kodu ilkesi iki sayım nedeni kodu türünden (*İsteğe Bağlı* veya *Zorunlu*) birini içerebilir. Sayım nedeni kodu ilkeleri, ambar düzeyinde veya madde düzeyinde kullanılabilir.

Neden kodu ilkesi oluşturmak için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Kurulum** \> **Stok** \> **Sayım nedeni kodu ilkeleri**'ne gidin.
1. Eylem Bölmesi'nde, ızgaraya bir ilke eklemek için **Yeni**'yi seçin.
1. Yeni ilke için **Ad** alanını ayarlayın.
1. **Sayım nedeni kodu türü** alanında, bir neden kodu seçiminin aşağıdaki stok ayarlaması işlemlerinden birinde isteğe bağlı veya zorunlu olması gerektiğini belirtmek için *Zorunlu* veya *İsteğe Bağlı*'yı seçin:

    - Döngü Sayısı (mobil cihaz)
    - Nokta Sayısı (mobil cihaz)
    - Eşik Sayısı (mobil cihaz)
    - Ayarlama etkin (mobil cihaz)
    - Ayarlama devre dışı (mobil cihaz)
    - Sayım Günlüğü (zengin istemci)
    - Miktar düzeltmesi/Çevrimiçi sayım (zengin istemci)

Tek tek ambarlar ve ürünler için de neden kodu ilkeleri ayarlayabilirsiniz. Bir ürün için neden kodu kurulumu, ürünün ambarının kurulumunu geçersiz kılabilir.

> [!NOTE]
> **Sayım nedeni kodu ilkeleri** alanının *Zorunlu* olarak ayarlandığı ambarlar ve maddeler için bir neden kodu sağlanana kadar sayım günlüğü tamamlanamaz ve kapatılamaz. Daha fazla bilgi edinmek için sonraki bölüme bakın.

### <a name="assign-counting-reason-code-policies-to-warehouses"></a>Ambara sayım nedeni kodu ilkeleri atama

Ambara sayım nedeni kodu ilkesi atamak için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Kurulum** \> **Stok dökümü** \> **Ambarlar**'a gidin.
1. Liste bölmesinde bir ambar seçin.
1. Eylem Bölmesi'nde **Ambar** sekmesindeki **Kurulum** grubunda, **Sayım nedeni kodu ilkesi**'ni seçin. Ardından **Sayım nedeni kodu ilkesi ata** açılır iletişim kutusunda, şu adımlardan birini izleyin:

    - Sayım günlüklerinin zorunlu olup olmadığını belirlemek üzere ilke ayarını her madde için kullanmak üzere hiç değer girmeyin (veya mevcut değeri silin).
    - Ambar için sayım günlüklerinde bir neden kodu istemek üzere **Sayım nedeni kodu türü** alanının *Zorunlu* olarak ayarlandığı bir neden ilkesi seçin.
    - Neden kodu, ambar için sayım günlüklerinde isteğe bağlıysa **Sayım nedeni kodu türü** alanının *İsteğe Bağlı* olarak ayarlandığı bir neden ilkesi seçin.

### <a name="assign-counting-reason-code-policies-to-products"></a>Sayım nedeni kodu ilkelerini ürünlere atama

Ürüne bir sayım nedeni kodu ilkesi atamak için aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.
1. Izgarada bir ürün seçin.
1. Eylem Bölmesi'nde **Ürün** sekmesindeki **Kurulum** grubunda, **Sayım nedeni kodu ilkesi**'ni seçin. Ardından **Sayım nedeni kodu ilkesi ata** açılır iletişim kutusunda, şu adımlardan birini izleyin:

    - Sayım günlüklerinin ürün için zorunlu olup olmadığını belirlemek üzere ilke ayarını depo için kullanmak üzere hiç değer girmeyin (veya mevcut değeri silin).
    - Ürün için sayım günlüklerinde bir neden kodu istemek üzere **Sayım nedeni kodu türü** alanının *Zorunlu* olarak ayarlandığı bir neden ilkesi seçin. Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.
    - Neden kodu, ürün için sayım günlüklerinde isteğe bağlıysa **Sayım nedeni kodu türü** alanının *İsteğe Bağlı* olarak ayarlandığı bir neden ilkesi seçin. Bu ayar ambar düzeyindeki neden kodu ayarını geçersiz kılar.

### <a name="set-up-counting-reason-codes"></a>Sayım nedeni kodları ayarlama

Sayım nedeni kodlarınızı ayarlamak için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Kurulum** \> **Stok** \> **Sayım nedeni kodu ilkesi**'ne gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. **Sayım nedeni kodu** ve **Açıklama** yeni satırda aşağıdaki alanları ayarlayın.
1. Mahsup hesabı atamak için **Mahsup hesap** alanına bir değer girin veya seçin.

    > [!NOTE]
    > Mahsup hesabı bir sayım nedeni koduna atanırsa bu sayım nedeni koduna sahip bir sayım günlüğünü deftere naklettiğinizde değer, varsayılan stok deftere nakil profili hesabı yerine atanan mahsup hesabına nakledilir.

### <a name="set-up-counting-reason-code-groups"></a><a name="reason-groups"></a>Sayım nedeni kodu grupları ayarlama

*Sayım nedeni kodu grupları*, sayım nedeni kodları listesini sınırlamak için Warehouse Management mobil uygulamasında *Ayarlama etkin* ve *Ayarlama devre dışı* menü öğelerinin parçası olarak kullanılabilir. (Sayım nedeni kodu grupları hakkında daha fazla bilgi için bu makalenin ilerleyen bölümlerinde yer alan [Ayarlama etkin ve Ayarlama devre dışı için mobil cihaz menü öğeleri ayarlama](#setup-adjustment-in-out) bölümüne bakın.)

1. **Stok yönetimi** \> **Kurulum** \> **Stok** \> **Sayım nedeni kodu grupları**'na gidin.
1. Eylem Bölmesi'nde, bir grup eklemek için **Yeni**'yi seçin.
1. Yeni grup için **Sayım nedeni kodu** ve **Grup açıklaması** alanlarını ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Ayrıntılar** bölümünde, ızgaraya bir satır eklemek için **Yeni**'yi seçin. Ardından, yeni satır için **Sayım nedeni kodu** alanını ayarlayın. 
1. Gerektiği şekilde daha fazla kod atamak için önceki adımı tekrarlayın. Gruptan bir kod kaldırmanız gerekiyorsa kodu seçin ve ardından araç çubuğunda **Sil** seçeneğini belirleyin.

### <a name="set-up-reason-codes-for-mobile-device-menu-items"></a>Mobil cihaz menü öğeleri için neden kodları ayarlama

Aşağıdaki eldeki stoku düzeltme türleri için neden kodlarını yapılandırabilirsiniz:

- Döngü Sayımı
- Nokta Sayımı
- Eşik Sayımı
- Ayarlama etkin
- Ayarlama devre dışı

Çoğu durumda, her ilgili mobil cihaz menü öğesi için aşağıdaki bilgileri tanımlayabilirsiniz:

- Neden kodunun mobil cihaz çalışanına sayım sırasında gösterilip gösterilmeyeceği
- Mobil cihaz menü öğesinde gösterilen varsayılan neden kodu.
- Kullanıcının neden kodunu düzenleyip düzenleyemeyeceği.

#### <a name="set-up-mobile-device-menu-items-for-a-counting-process"></a>Sayım işlemi için mobil cihaz menü öğeleri ayarlama

Sayım işlemi için bir mobil cihaz menü öğesi ayarlamak üzere aşağıdaki adımları izleyin.

1. **Warehouse Management** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**'ne gidin.
1. Liste bölmesinde ilgili menü öğesini seçin veya yeni bir menü öğesi oluşturun.
1. Eylem Bölmesinde, **Döngü sayımı**'nı seçin.
1. **Varsayılan sayım nedeni kodu** alanında, saymak için mobil cihaz menü öğesi kullanıldığında kaydedilmesi gereken varsayılan neden kodunu ayarlayın.
1. **Sayım nedeni kodunu görüntüle** alanında, aşağıdaki değerlerden birini seçin:

    - *Satır*: Her fark kaydedildikten sonra neden kodunu gösterir.
    - *Gizle*: Neden kodunu göstermez.

1. Sayım sırasında mobil cihazda gösterildiğinde çalışanın neden kodunu düzenlemesine izin vermek için **Sayım nedeni kodunu düzenle**'yi *Evet* olarak ayarlayın. Çalışanın kodu düzenlemesini önlemek için *Hayır* olarak ayarlayın.

> [!NOTE]
> **Döngü sayımı** düğmesi sayımın yapılabileceği herhangi bir mobil cihaz menüsünde etkinleştirilebilir. Örnekler arasında nokta sayımı, kullanıcı yönlendirmeli iş ve sistem yönlendirmeli iş için menü öğeleri sayılabilir.

#### <a name="set-up-mobile-device-menu-items-for-adjustment-in-and-adjustment-out"></a><a name="setup-adjustment-in-out"></a>Ayarlama etkin ve Ayarlama devre dışı için mobil cihaz menü öğesi ayarlama

Ayarlama etkin ve ayarlama devre dışı için mobil cihaz menü öğesi ayarlamak üzere aşağıdaki adımları izleyin.

1. **Warehouse Management** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**'ne gidin.
1. Eylem Bölmesi'nde, menü öğesini oluşturmak için **Yeni**'yi seçin.
1. Yeni menü öğesi için **Mobil öğe adı** ve **Başlık** alanlarını ayarlayın.
1. **Mod** alanını *İş* olarak ayarlayın.
1. **Mevcut işi kullan** seçeneğinde *Hayır*'ı işaretleyin.
1. **İş oluşturma işlemi** alanında, *Ayarlama etkin* veya *Ayarlama devre dışı*'nı seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın. (**İş oluşturma işlemi** alanında *Ayarlama etkin* veya *Ayarlama devre dışı*'nı seçtiğinizde tüm bu alanlar eklenir.)

    - **İşlem kılavuzu kullan**: *Ayarlama devre dışı* işlemi oluşturuyorsanız bu seçeneği *Evet* olarak ayarladığınızdan emin olun. *Ayarlama devre dışı* işlemi oluşturuyorsanız bu seçenek her zaman *Evet* olarak ayarlanır.
    - **Varsayılan sayım nedeni kodu**: Sayımı yapmak için mobil cihaz menü öğesi kullanıldığında kaydedilmesi gereken varsayılan neden kodunu ayarlayın.
    - **Sayım nedeni kodunu görüntüle**: Aşağıdaki değerlerden birini seçin:

        - *Satır*: Her fark kaydedildikten sonra neden kodunu gösterir.
        - *Gizle*: Neden kodunu göstermez.

    - **Sayım nedeni kodunu düzenle**: Sayım sırasında mobil cihazda gösterildiğinde çalışanın neden kodunu düzenlemesine izin vermek için bu seçeneği *Evet* olarak ayarlayın. Çalışanın kodu düzenlemesini önlemek için *Hayır* olarak ayarlayın.
    - **Sayım nedeni kodu grubu**: Çalışanlara sunulan seçeneklerin listesini sınırlandırmak istiyorsanız bir neden kodu grubu seçin. Neden kodu gruplarını ayarlamak hakkında daha fazla bilgi için bu makalenin önceki bölümündeki [Sayım nedeni kodu ilkesi ayarlama](#reason-groups) bölümüne bakın. 

> [!NOTE]
> Sayım nedeni kodu grubunu **İşlem kılavuzu kullan** seçeneğinin *Evet* olarak ayarlandığı *Ayarlama etkin* ve *Ayarlama devre dışı* menü öğelerine atadığınızda Warehouse Management mobil uygulamasında işlemenin parçası olarak sayım nedeni kodlarının sınırlı bir listesini alabilirsiniz.
>
> **İşlem kılavuzu kullan** seçeneği yanlışlıkla büyük düzeltme miktarlarının oluşmasını engellemeye de yardımcı olabilir. (Örneğin, bir çalışan bir miktar değeri yerine yanlışlıkla bir madde numarasının barkodunu tarayabilir.) Bu işlevi ayarlamak için **İşlem kılavuzu kullan** seçeneğini ilgili menü öğesi için *Evet* olarak ayarlayın. Ardından **Warehouse Management \> Kurulum \> Çalışan**'a gidin ve çalışanın kaydedebileceği maksimum düzeltme miktarını belirtmek üzere her ilgili ambar çalışanı için **Düzeltme miktarı sınırı** alanını ayarlayın.

## <a name="processing-that-uses-counting-reason-codes"></a>Sayım nedeni kodlarını kullanan işlem

Çalışanlar Warehouse Management mobil uygulamasını kullandıklarında, neden kodları kaydedilir. Sayım onay işlemi tanımlanmadığı sürece kaydedilen neden kodları, izleyen sayım günlüğü deftere nakil işleminin parçası olarak hemen kullanılır.

### <a name="cycle-count-approvals"></a>Döngü sayımı onayları

Bir sayım onaylanmadan önce çalışan sayımla ilişkili neden kodunu değiştirebilir. Sayım onaylandığında neden kodu sayım günlüğü satırlarına girilir.

#### <a name="modify-reason-codes-for-cycle-count-approvals"></a>Döngü sayımı onayları için neden kodlarını değiştirme

Döngü sayımı onayını değiştirmek için aşağıdaki adımları izleyin.

1. **Warehouse Management** \> **Döngü sayımı** \> **İnceleme bekleyen döngü sayımı işi**'ne gidin.
1. Izgarada bir döngü sayımını seçin.
1. Eylem Bölmesindeki **İş** sekmesinde, **Döngü Sayımı**'nı seçin. Ardından, **Neden kodu** alanında yeni bir neden kodu seçin.

Neden kodları *Sayım günlüğü* türündeki sayım günlüklerindeki günlük satırlarına eklenir.

1. **Stok yönetimi** \> **Günlük girişleri** \> **Madde sayımı** \> **Sayım**'a gidin.
2. Sayım günlüğünün satır ayrıntılarındaki **Sayım nedeni kodu** alanında, geçerli durumunuza uygun neden kodunu seçin.

### <a name="view-the-reason-codes-recorded-in-the-counting-history"></a>Sayım geçmişinde kaydedilen neden kodlarını görüntüleme

Sayım geçmişinde kaydedilen neden kodlarını görüntülemek için aşağıdaki adımları izleyin.

1. **Stok yönetimi** \> **Sorgular ve raporlar** \> **Sayım geçmişi**'ne gidin.
1. Liste bölmesinde bir madde sayımı kaydını seçin.
1. **Sayma nedeni kodu** alanında, bir neden kodu aracılığıyla kaydedilen sayım geçmişini görüntüleyin.

### <a name="use-reason-codes-for-quantity-adjustment-or-online-counting"></a>Miktar düzeltmesi veya çevrimiçi sayım için neden kodları kullanma

Miktar düzeltmesi veya çevrimiçi sayım için neden kodları kullanmak üzere aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.
1. Eylem Bölmesi'nde **Miktar düzeltmesi**'ni seçin.
1. **Miktar düzeltmesi**'ni seçin ve ardından **Sayım nedeni kodu** alanında bir neden kodu seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
