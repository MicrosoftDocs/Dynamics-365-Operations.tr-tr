---
title: Mobil cihaz menü öğelerindeki adımların deturlarını konfigüre etme
description: Bu makalede, çalışanların geçerli görevi park edebilmesi, başka bir görev gerçekleştirmesi ve herhangi bir bilgiyi kaybetmeden özgün göreve geri dönebilmesi için menü öğelerinin deturlarını konfigüre etme yöntemi açıklanmıştır.
author: Mirzaab
ms.date: 09/01/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour, WHSMobileAppFlowStepDetourSelectFields, WHSMobileAppFlowStepSelectPromotedFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e387dd4e6499912f2d53dddc17ccc053f1ca699
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689323"
---
# <a name="configure-detours-for-steps-in-mobile-device-menu-items"></a>Mobil cihaz menü öğelerindeki adımların deturlarını konfigüre etme

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

> [!IMPORTANT]
> Bu makalede açıklanan özellikler yalnızca yeni Warehouse Management mobil uygulaması için geçerlidir. Artık kullanımdan kaldırılan eski ambar uygulamasını etkilemezler.

Bu makalede, çalışanların geçerli görevi "park" edebilmesi, başka bir görev gerçekleştirmesi ve herhangi bir bilgiyi kaybetmeden özgün göreve geri dönebilmesi için menü öğelerinin deturlarını konfigüre etme yöntemi açıklanmıştır.

Sapma, ana görevdeki bir adımdan açılabilen ayrı bir menü öğesidir. Sapmanın sonunda, çalışan, ana görevin solundaki yere geri döndürülür. Konfigürasyon sırasında, sapma olarak davranması gereken menü öğesini belirtirsiniz. Ayrıca ana görevdeki hangi alan değerlerinin sapmaya otomatik olarak iletildiğini (kopyalanacağını) ve buraya girileceğini seçebilirsiniz. Bu nedenle, görev akışında, sapmanın çalışanlar için nereye kullanılabileceğini istediğinizi anlamanız gerekir. Ayrıca, sapma için kopyalanması gereken bilgilerin görev akışı adımı için kullanılabilir durumda olduğundan emin olmalısınız.

## <a name="enable-detours-in-your-system"></a>Sisteminizdeki sapmaları etkinleştirme

Mobil aygıt menü öğelerindeki adımların sapmalarını konfigüre etmeden önce, gerekli özellikleri etkinleştirmek ve Warehouse Management mobil uygulamasında gerekli alan adlarını oluşturmak için aşağıdaki yordamı tamamlamanız gerekir.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. Sistem için *Ambar uygulaması adım yönergeleri* özelliğinin açık olduğundan emin olun. Supply Chain Management sürüm 10.0.29 itibariyle, bu özellik varsayılan olarak açıktır. *Ambar uygulaması adım yönergeleri* özelliği hakkında daha fazla bilgi için , [Warehouse Management mobil uygulaması ile ilgili adım başlıklarını ve yönergeleri özelleştirme](mobile-app-titles-instructions.md) konusuna bakın. Bu özellik, *Warehouse Management uygulaması sapmaları* özelliği için bir önkoşuldur.
1. Bu makalede açıklanan işlevselliği sağlayan aşağıdaki özellikleri açın:
    - *Warehouse Management uygulaması sapmaları*<br>(Supply Chain Management sürüm 10.0.29 itibariyle, bu özellik varsayılan olarak açıktır.)
    - *Warehouse Management mobil uygulaması için çok düzeyli sapmalar*
    - *Warehouse Management mobil uygulaması için sapma adımlarını otomatik olarak gönder*
1. *Warehouse Management uygulama sapmaları* ve/veya *Warehouse Management mobil uygulaması için çok düzeyli sapmalar* özelliği zaten açık değilse **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Ambar uygulaması alan adları**'na gidip **Varsayılan kurulum oluştur**'u seçerek Warehouse Management mobil uygulamasında alan adlarını güncelleştirin. - Daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulaması için alanları yapılandırma](configure-app-field-names-priorities-warehouse.md).
1. Warehouse Management mobil uygulamasını kullandığınız her yasal varlık (şirket) için önceki adımı yineleyin.

## <a name="configure-a-detour-from-a-menu-specific-override"></a>Menüye özel bir geçersiz kılma için sapmayı konfigüre etme

Menüye özel bir geçersiz kılmada bir sapma ayarlamak için aşağıdaki yordamı kullanın.

1. İlgili menü için, [Warehouse Management mobil uygulaması için adım başlıklarını ve talimatlarını özelleştirme](mobile-app-titles-instructions.md) bölümünde açıklandığı şekilde ilgili menü ve adımlar için menüye özel geçersiz kılma oluşturun.
1. Düzenlemek istediğiniz **Adım Kimliği** ve **Menü öğesi adı** değerlerinin birleşimini bulun ve **Adım Kimliği** sütunundaki değeri seçin.
1. Görüntülenen sayfada, **Mevcut sapmalar (menü öğeleri)** hızlı sekmesinde, bir gezinti görevi görecek menü öğesini belirtebilirsiniz. Ayrıca ana görevdeki hangi alan değerlerinin sapmaya ve sapmadan otomatik olarak iletildiğini belirleyebilrisiniz. Bu ayarların nasıl kullanılacağını gösteren örnekler için, bu makalenin ilerleyen kısımlarında yer alan senaryolara bakın.

## <a name="sample-scenario-1-sales-picking-where-a-location-inquiry-acts-as-a-detour"></a><a name="scenario-1"></a>Örnek Senaryo 1: Bir yerleşim sorgulaması sırasında yapılacak bir sapma olarak hareket eden satış çekme

Bu senaryo, çalışanların yönlendirilmiş satış malzeme çekme görev akışındaki bir yerleşim sorgulaması ile sapma olarak konfigüre etme şeklini gösterir. Bu sapma, çalışanların çekmeye çalıştıkları konumdaki tüm lisans levhalarını arayıp çekmeyi tamamlamak için kullanmak istedikleri lisans levhasını çeker. Bu tür bir sapma, barkod hasar görmüşse ve bu nedenle tarayıcı aygıtı tarafından okunamıyorsa yararlı olabilir. Alternatif olarak, bir çalışanın sistemde neler olduğunu öğrenmesine yardımcı olması gerektiğinde yararlı olabilir. Bu senaryonun yalnızca lisans levhası denetimli konumlardan çekme yapıyorsanız çalıştığına dikkat edin.

### <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Belirtilen örnek kayıtlarını ve değerlerini kullanarak bu senaryoda çalışmak için standart [demo verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklü olduğu bir sistem kullanmanız gerekir. Ayrıca başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-1"></a>Menüye özel geçersiz kılma oluşturma ve senaryo 1 için sapmayı konfigüre etme

Bu yordamda, plaka adımında **Satış seçme** menü öğesi için bir sapma yapılandıracaksınız.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. *LicensePlateId* adlı adım kodunu bulun ve seçin.
1. Eylem Panosunda, **Adım yapılandırması ekle**'yi seçin.
1. *Satış çekme*'yi bulmak ve seçmek için açılan iletişim kutusunda **Menü öğesi** alanını kullanın.
1. **Tamam**'ı seçin.
1. Yeni oluşturduğunuz geçersiz kılma için ayrıntılar sayfası görüntülenir. **Kullanılabilir sapmalar (menü öğeleri)** hızlı sekmesinde, araç çubuğundan **Ekle**'yi seçin.
1. **Sapma ekle** iletişim kutusunda, Warehouse Management mobil uygulamasında kullanılabilir yapılacak sapma olarak **Yerleşim sorgusu**'nu seçin.
1. **Tamam**'ı seçin.
1. **Kullanılabilen sapmalar (menü öğeleri)** hızlı sekmesinde, az önce eklediğiniz sapmayı seçin ve araç çubuğunda **Gönderilecek alanları seç**'i belirleyin.
1. **Gönderilecek alanları seçin** iletişim kutusunda, sapmadan ve sapmaya gönderilecek bilgileri belirleyin. Bu senaryoda, çalışanların konum sorgulama sapması için giriş olarak seçim yapmaları gereken konumları kullanmasını etkinleştiriyoruz. Bu nedenle, **Satış çekmesinden gönder** bölümünde, kılavuza satır eklemek için araç çubuğundan **Ekle**'yi seçin. Ardından yeni satırda aşağıdaki değerleri ayarlayın:

    - **Satış Çekmeden kopyalama:** *Konum*
    - **Konum Sorgusuna yapıştır:** *Konum*
    - **Otomatik gönder:** *Seçildi* (sayfa, yapıştırılan *Konum* değeriyle yenilenir)

1. Bu senaryodaki sapma, lisans levhası adımında yapılandırıldığı için, çalışanlar lisans levhasını sorgudan ana akışa geri gönderme yaparken yararlı olacaktır. Bu nedenle, **Konum sorgusundan geri getir** bölümünde, kılavuza satır eklemek için araç çubuğundan **Ekle**'yi seçin. Ardından yeni satırda aşağıdaki değerleri ayarlayın:

    - **Konum Sorgusundan kopyala:** *Lisans levhası*
    - **Satış Çekmeye yapıştır:** *Lisans levhası*
    - **Otomatik gönder:** *Temizlendi* (*Plaka* değeri olan sapmadan döndürülürken otomatik güncelleştirme gerçekleşmez)

1. **Tamam**'ı seçin.

Sapma şimdi tam olarak yapılandırılmıştır. **Konum sorgulama** sapmasını başlatacak bir düğme, lisans levhası adımında **Satış çekme** menü öğesinde görünür.

### <a name="complete-a-sales-pick-on-a-mobile-device-and-use-the-detour"></a>Mobil cihazda bir satış çekmeyi tamamlayın ve sapmayı kullanın

Bu yordamda, Warehouse Management mobil uygulamasını kullanarak bir satış çekmeyi tamamlayacaksınız. Çekme adımını tamamlamak için kullanacağınız, yeni lisans levhasını bulmak için konfigüre ettiğiniz sapmayı kullanacaksınız.

1. Microsoft Dynamics 365 Supply Chain Management'ta, lisans levhası izlenen bir konumdan çekme adımı gerektirecek bir satış siparişi oluşturun. Ardından satış siparişini ambara serbest bırakın. Oluşturulan iş kimliğini not edin.
1. Warehouse Management mobil uygulamasını açın ve ambar 24'te oturum açın. (Standart demo verilerinde, kullanıcı kimliği *24* ve parola olarak *1*'i kullanarak oturum açın.)
1. **Çıkış** menüsünü seçin ve sonra **Satış malzeme çekme** menü maddesini seçin.
1. Adım 1'de oluşturulan iş kodunu girmek için ekrandaki veri giriş yönergelerini izleyin.
1. **Lisans levhasını tarama** metnini içeren adımda eylemler menüsünü açın. **Konum sorgusu** olarak etiketlenmiş yeni bir düğme görmelisiniz. Sol üst köşedeki ok işareti, düğmenin bir sapmayı başlatacağını gösterir. **Konum sorgusu**'nu seçin.
1. Sapma başlatılır. Bir sonraki sayfada, ana akıştan kopyalanan konumu onaylayın.
1. Konumdaki kullanılabilir lisans levhaları listesinde, ana akışa geri kopyalamak istediğiniz lisans kalıbına dokunun. Sonra **Geri** düğmesini seçin.
1. Satış malzeme çekme ana akışına iade edilir ve lisans levhası, sapmadan geri kopyalanır. Sonraki adımla devam etmek için değeri onaylayın.
1. Artık istenen veri girişi yönergelerini girerek standart akışın geri kalanını tamamlayabilirsiniz.

Ambar çalışması şimdi tamamlandı. Çalışan, ana görevdeki yerini kaybetmeden ikincil bir görev (konum sorgusu) gerçekleştirmek için bir sapmayı açtı ve ana görevi tamamlamak için gereken bilgileri geri getirdi.

## <a name="sample-scenario-2-item-inquiry-with-movement-and-adjustment-detours"></a>Örnek Senaryo 2: Hareket ve düzeltme sapmalarıyla madde sorgulaması

Bu senaryo, yerleşim sorgulama görev akışında hareketin ve ayarlamaların çoklu sapmalar olarak nasıl yapılandırılacağını gösterir. Bu yetenek, bir çalışanın bir yerleşime ulaştığı durumlarda yararlı olabilir, yerleşimdeki stoğun sistemde kayıtlı olandan farklı olduğunu ve bu nedenle mal ayarlanması veya taşıması gerektiğini fark edebilir.

Konum sorgulamasını, bir lisans levha sorgusu veya gereksinim duyduğunuz bir madde sorgulaması ile değiştirebilirsiniz.

### <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Belirtilen örnek kayıtlarını ve değerlerini kullanarak bu senaryoda çalışmak için standart [demo verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklü olduğu bir sistem kullanmanız gerekir. Ayrıca başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="create-a-menu-specific-override-and-configure-the-detour-for-scenario-2"></a>Menüye özel geçersiz kılma oluşturma ve senaryo 2 için sapmayı konfigüre etme

Bu yordamda, plaka adımında **Satış seçme** menü öğesi için bir sapma yapılandıracaksınız.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz adımları**'na gidin.
1. *LocationInquiryList* adlı adım kodunu bulun ve seçin.

    > [!NOTE]
    > Yerleşim sorgusu yerine bir madde sorgulaması kullanmak için, adım kodunun *ItemInquiryList* adını taşıdığı bir satır seçin. Lisans levhası sorgusu kullanmak için adım kimliğinin *LPInquiryList* adını taşıdığı satırı seçin.

1. Eylem Panosunda, **Adım yapılandırması ekle**'yi seçin.
1. *Konum sorgusu*'nu bulmak ve seçmek için açılan iletişim kutusunda **Menü öğesi** alanını kullanın.
1. **Tamam**'ı seçin.
1. Yeni oluşturduğunuz geçersiz kılma için ayrıntılar sayfası görüntülenir. **Kullanılabilir sapmalar (menü öğeleri)** hızlı sekmesinde, araç çubuğundan **Ekle**'yi seçin.
1. **Sapma ekle** iletişim kutusunda, Warehouse Management mobil uygulamasında kullanılabilir yapılacak sapma olarak **Hareket**'i seçin.
1. **Tamam**'ı seçin.
1. **Kullanılabilen sapmalar (menü öğeleri)** hızlı sekmesinde, az önce eklediğiniz sapmayı seçin ve araç çubuğunda **Gönderilecek alanları seç**'i belirleyin.
1. **Gönderilecek alanları seçin** iletişim kutusunda, sapmadan ve sapmaya gönderilecek bilgileri belirleyin. Bu senaryoda, çalışanların, lisans levhası denetimli konumlara bakmalarını beklersiniz. Bu nedenle, lisans levhasının sorgudan taşıma **Hareket** grubuna kopyalanması yararlı olacaktır. **Satış çekmesinden gönder** bölümünde, kılavuza satır eklemek için araç çubuğundan **Ekle**'yi seçin. Ardından yeni satırda aşağıdaki değerleri ayarlayın:

    - **Konum Sorgusundan kopyala:** *Konum*
    - **Harekete yapıştır:** *Loc / LP*
    - **Otomatik gönder:** *Temizlendi* (otomatik güncelleştirme gerçekleşmez)

    Ana akış ek adımların gerekli olmadığı bir sorgu olduğundan, bu sapma sırasında herhangi bir bilginin geri kopyalanmasını bekleyemezsiniz.

1. **Tamam**'ı seçin.

Sapma şimdi tam olarak yapılandırılmıştır. **Hareket** sapmasını başlatacak bir düğme, lisans levhası adımında **Konum sorgusu** menü öğesinde görünür.

### <a name="do-a-location-inquiry-on-a-mobile-device-and-use-the-detour"></a>Mobil cihazda bir yerleşim sorgusu yapma ve sapmayı kullanma

Bu yordamda, Warehouse Management mobil uygulamasını kullanarak konum sorgusu yapacaksınız. Daha sonra, bir mal hareketini tamamlamak için sapmayı kullanacaksınız.

1. Warehouse Management mobil uygulamasını açın ve ambar 24'te oturum açın. (Standart demo verilerinde, kullanıcı kimliği *24* ve parola olarak *1*'i kullanarak oturum açın.)
1. **Stok** menüsünü seçin ve sonra **Konum sorgusu** menü maddesini seçin.
1. *FL-001* gibi sorgulayacak bir konum girin.
1. Liste göründüğünde, mevcut sapmaların gösterilmesi için, içindeki kartlardan birine dokunup bekleyin.
1. **Hareket**'i seçin.
1. Lisans levhasının seçtiğiniz karttan kopyalanmış olduğuna dikkat edin. Değeri onaylayın.
1. Hareketi tamamlamak için artık standart görev akışını izleyebilirsiniz. İş tamamlandıktan sonra, eylemler menüsünü açın ve **İptal**'i seçin.
1. **Konum sorgulama** sayfasına geri dönersiniz. Değerlerin otomatik olarak güncelleştirilmediği unutmayın. Bu nedenle, hareket sapma çubuğundan değişiklikleri görmek için sayfayı el ile yenilemeniz gerekir.

> [!NOTE]
> *Warehouse Management mobil uygulaması için çok düzeyli sapmalar* özelliği, çalışanların mevcut bir sapmadan saniyede iki kez atlamasına ve ardından tekrar geri dönmesine olanak tanıyan çok düzeyli sapmalar (sapmalar içinde sapmalar) tanımlamanıza olanak tanır. Özellik, kullanıma hazır iki sapma düzeyini destekler ve gerekirse `WHSWorkUserSessionState` tablosunda kod uzantıları oluşturarak sisteminizi üç veya daha fazla sapma düzeyini destekleyecek şekilde özelleştirebilirsiniz.
>
> *Warehouse Management mobil uygulaması için sapma adımlarını otomatik olarak gönder* özelliği, çalışanların Warehouse Management mobil uygulamasında sapma akışlarını tamamlamasını hızlandırıp kolaylaştırabilir. Bu, [*Örnek Senaryo 1: Bir yerleşim sorgulaması sırasında yapılacak bir sapma olarak hareket eden satış çekme*](#scenario-1) bölümünde gösterildiği üzere uygulamanın arka uçta sapma verilerini doldurmasına ve ardından sayfayı otomatik göndererek otomatik olarak sonraki adıma geçmesine olanak tanıyarak bazı akış adımlarının atlanmasını sağlar.
