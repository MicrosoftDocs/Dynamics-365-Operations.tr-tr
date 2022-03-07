---
title: Dalga yürütme bildirimleri
description: Bu konu, dalga yürütme bildirimlerini ve bunları nasıl ayarlayabileceğinizi açıklamaktadır.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 26810f6e21f9c8ba6e92621a8e1ddee17837b6048107b961afb0e428059051af
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752596"
---
# <a name="wave-execution-notifications"></a>Dalga yürütme bildirimleri

[!include [banner](../includes/banner.md)]

*Dalga yürütme bildirimleri* özelliği, dalga yürütme ile ilgili bildirimler sağlamak için iş olaylarını ve eylem merkezini kullanır. Bildirimler üreten olayların tiplerini, onları oluşturan ambarları ve onları alan kullanıcıları belirtmenize olanak tanır.

Gezinti çubuğunun sağ tarafındaki **iletileri göster** düğmesi (çan sembolü), geçerli kullanıcı için bir Eylem Merkezi iletisinin ne zaman kullanılabileceğini gösterir. Kullanıcı, eylem merkezini açmak ve iletileri incelemek için **iletileri göster** düğmesini seçebilir.

İş olayları, iş süreçleri çalıştırıldığında oluşur. İş süreçleri görevlerden oluşur. Bir iş süreci sırasında, buna katılan kullanıcılar bu görevleri tamamlamak için iş eylemlerini gerçekleştirirler. İş olayları, dış sistemlerin Finance and Operations uygulamalarından bildirimler almasına olanak tanıyan bir mekanizma sağlar. Bu şekilde, sistemler iş olaylarına yanıt olarak iş eylemlerini gerçekleştirebilir. Daha fazla bilgi için bkz. [İş olaylarına genel bakış](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-on-the-wave-execution-notifications-feature"></a>Dalga yürütme bildirimleri özelliğini açma

*Dalga yürütme bildirimleri* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Dalga yürütme bildirimleri*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Senaryo: İşlem merkezine dalga toplu iş yürütme bildirimleri gönderme

Bu senaryo, dalga toplu iş yürütme hataları hakkında, Eylem Merkezi aracılığıyla belirli bir role bildirim göndermek için uçtan uca akışı gösterir.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Dalgaların toplu iş modunda çalıştığından emin olun

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Dalga işleme** hızlı sekmesinde, **Dalgaları Toplu işle** öğesini *Evet* olarak ayarlayın.

> [!NOTE]
> Dalga toplu yürütme bildirimlerini devre dışı bırakmak istiyorsanız, **dalga işleme toplu iş bildirimlerini devre dışı bırak** seçeneğini *Evet* olarak ayarlayın.

### <a name="configure-a-wave-notification-policy"></a>Dalga bildirim ilkesi Yapılandırma

Dalga bildirim ilkeleri, gönderilen bildirim türlerini ve uyarılacak kullanıcıları tanımlar.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga bildirim ilkeleri**'ne gidin.
1. Aşağıdaki ayarlara sahip bir kayıt oluşturun:

    - **Dalga bildirim ilkesi:** *24BatchError*
    - **Açıklama:** *Ambar 24 dalga toplu iş hatası*
    - **Bildirim gönderme:** *Yalnızca hata*
    - **Gönderilen rol:** *Sistem Yöneticisi*

        > [!NOTE]
        > Bu senaryo demo verileri kullandığı için, *Sistem Yöneticisi* rolü kolaylık olması için seçilir. Bu nedenle, Sistem Yöneticisi kullanıcısı olarak oturum açtığınızdan, bildirimleri alacaksınız. Ancak uygulamada, dalga toplu yürütme hatalarını bildirmek için genellikle *Ambar Yöneticisi* gibi daha belirli bir rol seçmelisiniz.

1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="configure-a-wave-template"></a>Dalga şablonu yapılandırma

Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonlarına bağlayabilmenizi sağlar.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Liste bölmesinde, **dalga şablonu türü** alanını *sevkiyat* olarak ayarlayın ve sonra da Ambar 24 için *24 sevkiyat varsayılan* dalga şablonunu seçin.
1. **Genel** hızlı sekmesinde, **Dalga bildirim ilkesi** alanını *24BatchError* olarak ayarlayın.

### <a name="configure-a-work-template"></a>İş şablonu yapılandırma

İş şablonları, dalga yürütmesi sırasında iş oluşturmak için kullanılır. Bu senaryoda, dalga yürütmenin bir hata tetiklemesi gerekir. İş şablonu sorgusunu varolmayan bir ambarı kullanacak şekilde ayarlayarak, dalga yürütmenin başarısız olmasını ve dolayısıyla bir bildirim göndermesini sağlayın.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Liste bölmesinde, **İş şablonu türü** alanını *Satış emirleri* olarak ayarlayın ve sonra da Ambar 24 için *24 SO Aşaması* iş şablonunu seçin.
1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. Sorgu Düzenleyicisi iletişim kutusunda **Aralık** sekmesinde aşağıdaki satırı düzenleyin (veya yoksa ekleyin):

    - **Tablo:** *geçici iş hareketleri*
    - **Türetilmiş tablo:** *geçici iş hareketleri*
    - **Alan:** *Ambar*
    - **Ölçüt:** Değeri *24*'ten *Hata*'ya değiştirin.

1. **Tamam**'ı seçin ve değişikliği onaylayın.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Satış siparişi oluşturma ve ambara serbest bırakma

1. **Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.
1. Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *24*

1. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip satış emri satırı ekleyin:

    - **Madde numarası:** *A0001*
    - **Miktar:** *10*

    > [!NOTE]
    > Bu maddeler ve miktarlar yalnızca örnektir. Belirtilen ambarda yeterli stok bulunmalıdır.

1. Yeni satır **Satış siparişi satırları** hızlı sekmesinde seçiliyken, araç çubuğunda **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, eylem bölmesinde, **Lot ayır** 'yi seçin. Ardından sayfayı kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

### <a name="notifications-from-wave-batch-job-execution"></a>Dalga toplu iş yürütmeden bildirimler

İş olaylarınızın kurulumuna bağlı olarak, sonuçta dalga yürütme hatası hakkında bir bildirim alacaksınız. Eylem Merkezi iletisi aşağıdaki örneğe benzeyecek ve başarısız olan bir dalgaya bağlantı içerecektir.

> **Dalga yürütme sırasında hata oluştu**  
> Dalga USMF-000000001 yürütülürken hata oluştu.  
> Son iletiler: Dalga USMF-000000001 için iş oluşturulmadı.
>
> **DURUM**  
> Active
>
> Dalga ayrıntılarını aç

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
