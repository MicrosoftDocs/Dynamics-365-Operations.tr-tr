---
title: Commerce Scale Unit'i (bulut) başlatma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te Commerce Scale Unit'in (bulut) nasıl başlatılacağı açıklanmaktadır.
author: AamirAllaq
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.openlocfilehash: 969dd220a7b73a676b9cf5ac26223ebd9b3f2296
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942866"
---
# <a name="initialize-commerce-scale-unit-cloud"></a>Commerce Scale Unit'i (bulut) başlatma

[!include[banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te Commerce Scale Unit'in (bulut) nasıl başlatılacağı açıklanmaktadır.

8.1.2.x veya sonraki bir uygulama sürümüne sahip bir Katman 2 korumalı alanı veya üretim ortamı kullanıyorsanız satış noktası (POS) işlemleri veya bulutta Retail Server kullanan e-ticaret işlemleri için perakende kanalı işlevselliğini kullanabilmeniz için önce Commerce Scale Unit'i (bulut) başlatmanız gerekir. Başlatma işlemi, bir Commerce Scale Unit (bulut) dağıtacaktır.

> [!IMPORTANT]
> Bulutta perakende kanalı işlevselliğini kullanan mevcut müşteriler, işletmeleri için sürekli ve kesintisiz destek sağlamak üzere perakende kanallarını Commerce Scale Unit kullanacak şekilde güncelleyebilir. Commerce Scale Unit olmadan dağıtılan yeni ortamlar artık bulutta barındırılan perakende kanalı bileşenleri için kalite ve hizmet güncelleştirmeleri almayacak. Yalnızca Commerce Scale Unit (kendi kendine barındırılan) kullanan müşteriler için herhangi bir işlem yapılması gerekmez. Uzatmaya ihtiyacınız varsa Microsoft FastTrack çözüm mimarınıza başvurun.

## <a name="prerequisites"></a>Önkoşullar

1. 8.1.2.x veya sonraki bir sürümü olan bir Katman 2 korumalı alanı veya üretim ortamı dağıtın.
2. Ortam başına en fazla 2 Commerce Scale Unit dağıtabilirsiniz. Ortam başına 2'den fazla Commerce Scale Unit'e ihtiyacınız varsa, Microsoft Dynamics Lifecycle Services'de (LCS), bir destek isteği oluşturun ve **Ek Commerce Scale Unit talebi girin** ve ortam kimliği, Commerce Scale Unit sayısı ve istenen veri merkezi bölgelerini belirtin. Talep beş iş günü içinde tamamlanacaktır. Ortam başına 2'den fazla Commerce Scale Unit gerekmiyorsa bir destek isteği oluşturmanız gerekmez. 
3. Commerce Scale Unit'i başlatmadan önce Lifecycle Services'da Proje Sahibi izinlerine sahip olmanız gerekir.
4. Perakende lisans yapılandırma anahtarlarının ortamınızda etkinleştirildiğinden emin olun. Daha fazla bilgi için bkz. [Lisans kodları ve yapılandırma anahtarları raporu](../sysadmin/license-codes-configuration-keys-report.md). Commerce Scale Unit'i kullanmak için aşağıdaki anahtarların açık olması gerekir.

    - RetailBasic
    - RetaileCommerce - Dynamics 365 Commerce için E-Ticaret kullanmayı planlıyorsanız.
    - RetailGiftCard - Hediye kartları kullanmayı planlıyorsanız.
    - RetailInvent - Stok kullanmayı planlıyorsanız.
    - RetailModernPos - Satış noktası (POS) kullanmayı planlıyorsanız.
    - RetailReplenishment - Stok yenilemeleri kullanmayı planlıyorsanız.
    - RetailScheduler
    - RetailStores - POS kullanmayı planlıyorsanız.


## <a name="region-availability"></a>Bölgeşere göre kullanılabilirlik
Commerce Scale Unit aşağıdaki bölgelerde dağıtım için kullanılabilir.

| Global konum | Bölge              | Kullanılabilirlik        | Açıklamalar                  |
|-----------------|---------------------|---------------------|---------------------------|
| AMERİKA KITASI        | Doğu ABD             | Genel kullanılabilir |                           |
| AMERİKA KITASI        | Doğu ABD 2           | Genel kullanılabilir |                           |
| AMERİKA KITASI        | Kuzey Orta ABD    | Sınırlı kapasite    |                           |
| AMERİKA KITASI        | Güney Orta ABD    | Sınırlı kapasite    |                           |
| AMERİKA KITASI        | Orta ABD          | Genel kullanılabilir |                           |
| AMERİKA KITASI        | Batı ABD             | Genel kullanılabilir |                           |
| AMERİKA KITASI        | Batı ABD 2           | Genel kullanılabilir |                           |
| AMERİKA KITASI        | Orta Kanada      | Sınırlı kapasite    |                           |
| AMERİKA KITASI        | Doğu Kanada         | Sınırlı kapasite    |                           |
| AMERİKA KITASI        | Batı Orta ABD     | Sınırlı kapasite    |                           |
| APAC            | Doğu Avustralya      | Genel kullanılabilir |                           |
| APAC            | Güneydoğu Asya      | Sınırlı kapasite | Dağıtıma izin verilmiyor    |
| APAC            | Doğu Japonya          | Genel kullanılabilir |                           |
| APAC            | Batı Japonya          | Genel kullanılabilir |                           |
| APAC            | Güneydoğu Avustralya | Genel kullanılabilir |                           |
| APAC            | Doğu Asya           | Sınırlı kapasite    |                           |
| APAC            | Güney Hindistan         | Sınırlı kapasite | Dağıtıma izin verilmiyor    |
| APAC            | Hindistan Orta       | Sınırlı kapasite    | Onay süreci gerekiyor |
| EMEA            | Batı Avrupa         | Genel kullanılabilir |                           |
| EMEA            | Kuzey Avrupa        | Genel kullanılabilir |                           |
| EMEA            | Birleşik Krallık Güney            | Sınırlı kapasite    |                           |
| EMEA            | Batı Birleşik Krallık             | Sınırlı kapasite    |                           |
| İsviçre     | Kuzey İsviçre   | Sınırlı kapasite    | Onay süreci gerekiyor |
| BAE             | Kuzey BAE           | Sınırlı kapasite    | Onay süreci gerekiyor |

Sınırlı kapasite bölgelerinde dağıtım kapasitesi son derece kısıtlanmıştır. Dağıtım istekleri duruma göre değerlendirilir. Sınırlı kapasite bölgelerinde dağıtım için yeterli bir ticari gerekçeniz varsa bekleme listesine eklenecek bir destek isteğinde bulunabilirsiniz. Kapasitenin sınırlandığı alanlar, şu anda Commerce Scale Unit dağıtımına izin vermiyor. 

![Bölge kullanılabilirliğini gösteren harita.](media/Commerce-Scale-Unit-Region-Availability.png "Bölge kullanılabilirliğini gösteren harita")

## <a name="initialize-commerce-scale-unit-as-part-of-a-new-environment-deployment"></a>Yeni bir ortam dağıtımının parçası olarak Commerce Scale Unit'i başlatma

Lütfen Headquarters'ın kullanılabilir olduğundan emin olun. Bu, başlatma işlemi sırasında ölçek birimini Headquarters'a kaydetmek için gereklidir. Headquarters'a servis uygulanırken bir ölçek biriminin başlatılması önerilmez çünkü servis işlemi sırasında kullanılamaz hale gelebilir.

1. Headquarters ortamının kullanılabilir durumda olduğundan ve [Bakım modunda](../sysadmin/maintenance-mode.md) olmadığından emin olun.
2. LCS'de, ortam ayrıntıları sayfasında **Ortam özellikleri \> Commerce**'ü seçin.
3. Commerce kurulum dağıtımı sayfasında **Başlat**'ı seçin.
4. Başlatılacak Commerce Scale Unit sürümünü seçin.
5. Commerce Scale Unit'in başlatılacağı bir bölge seçin.

## <a name="configure-channels-to-use-commerce-scale-unit"></a>Kanalları Commerce Scale Unit kullanacak şekilde yapılandırma

Commerce Scale Unit dağıtıldıktan sonra, kanallarınızın veritabanını kullanacak şekilde yapılandırıldığından emin olmalısınız. 

Kanallarınızı Commerce Scale Unit veritabanını kullanacak şekilde yapılandırmak için şu adımları izleyin.

1. Commerce Headquarters'da **Retail ve Commerce \> Headquarters ayarı \> Commerce Planlayıcısı \> Kanal veritabanı**'na gidin.
1. Sol bölmede bir kanal veritabanı seçin.
1. **Perakende kanalı** Hızlı Sekmesinde **Ekle**'yi seçin ve ardından açılan listede perakende kanalınızı seçin.
1. **Ekle**'yi seçin ve sonra açılan listeden çevrimiçi kanalınızı seçin. 

İşiniz bittiğinde, **Retail ve Commerce \> Retail ve Commerce BT \> Dağıtım programı**'na gidin ve 9999 işini çalıştırın.

> [!NOTE] 
> İş 9999, tüm yeni ürünleri ve müşterileri Commerce Scale Unit ile eşitler. Bu işlem uzun sürebilir. Kanalın yalnızca e-ticaret sitesi oluşturucu yapılandırması için kullanılabilir olması gerekiyorsa iş 9999 yerine 1070 işini çalıştırabilirsiniz.

### <a name="database-refresh-and-commerce-scale-units"></a>Veritabanı yenileme ve Commerce Scale Unit

Başlamadan önce, [Commerce işlevselliğini kullanan ortamlar için veritabanı yenilemesinden sonra tamamlanacak adımlar](../database/database-refresh.md)'a hakim olduğunuzdan emin olun.

Ölçek birimi kanal veritabanı kayıtları (Kanal Veritabanı formunda), veritabanı yenilemesinin bir parçası olarak ortamlar arasında taşınamaz. Bunun nedeni, kayıtların ortama özgü yapılandırmayı temsil ediyor olmasıdır.

Veritabanı yenilemeden sonra, ölçek biriminizin LCS'de yeniden dağıtımını yayınlayarak ölçek biriminin kanal veritabanı kaydını yeniden oluşturabilirsiniz. Ölçek birimindeki herhangi bir dağıtım veya servis işlemi, kaydın eksik olduğu tespit edilirse, ölçek birimini Headquarters'a kaydetmeye çalışır.

Ölçek biriminizin zaten olduğu sürümü dağıtmayı seçerek herhangi bir bileşeni değiştirmeden ölçek biriminin yeniden dağıtımını sağlayabilirsiniz. Bu işlem, şu adımlar izlenerek LCS'de yapılabilir.

1. LCS'de, ortam ayrıntıları sayfasında **Ortam özellikleri \> Perakende**'yi seçin.
2. Kurulum dağıtımı sayfasında, yeniden dağıtmak istediğiniz ölçek birimini seçin.
3. Ölçek biriminin çalışma menüsünde **Güncelleştir**'i seçin.
4. Kaydırıcıda, **Sürüm seç** açılan menüsünde **Sürüm seçin** seçeneğini belirleyin.
5. **Sürüm belirtin** altındaki metin kutusuna, **Geçerli sürüm** etiketinin yanı sıra ölçek biriminiz için gösterilen sürümü yazın.
6. **Güncelleştir** düğmesine tıklayın.

Bir ölçek birimi güncelleştirilirken ölçek birimine uygulanan son uzantı paketi otomatik olarak alındığından, uzantıları daha önce uygulamış olsanız bile **Uzantıları güncelleştir**'i seçmeniz gerekmez.

Birden çok ölçek biriminiz varsa, her ölçek birimi için yukarıdaki işlemi gerçekleştirmeniz gerekir. İsterseniz bu işlemleri paralel olarak gerçekleştirebilirsiniz.

## <a name="deploy-additional-commerce-scale-units-optional"></a>Ek Commerce Scale Units dağıtma (isteğe bağlı)

Commerce Scale Unit'i başlatmadan sonra, lisansınız size bunu yapma hakkı verirse ikinci bir Ölçek Birimini kendi kendine barındırılacak şekilde dağıtabilirsiniz. İkiden fazla Ölçek Birimi dağıtmak için bir destek isteği oluşturmanız gerekir. Destek isteğinde, ihtiyacınız olan Commerce Scale Unit sayısını, ortam adını ve istenen bölgeleri belirtin. Lisanslama hakkında daha fazla bilgi için bkz. [Dynamics 365 Lisanslama Kılavuzu](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409). 

Dağıttığınız her ek Commerce Scale Unit için bu adımları izleyerek ayrı bir kanal veritabanı grubu oluşturmanızı öneririz.

1. Commerce merkez ofisinde, **Retail ve Commerce > Retail Headquarters > Retail Planlayıcı kurulumu > Kanal veritabanı grubu**'na gidin.
2. Yeni bir kanal veritabanı grubu oluşturun.
3. **Retail ve Commerce > Retail Headquarters > Retail Planlayıcı kurulumu > Kanal veritabanı**'na gidin ve yeni oluşturulan Commerce Scale Unit'e karşılık gelen kanal veritabanını seçin.
4. **Düzenle**'yi seçin ve yeni kanal veritabanı grubunu seçin.
5. **Kaydet**'i seçin.
6. Seçili kanal veritabanı için **Tam veri eşitlemesini çalıştır**'ı seçin.

## <a name="additional-considerations-if-you-initialize-cloud-hosted-commerce-channel-components-in-an-existing-environment"></a>Bulutta barındırılan Commerce kanalı bileşenlerini mevcut bir ortamda başlatırsanız dikkat edilmesi gerkene ek noktalar

Bulutta barındırılan Commerce kanalı bileşenlerini bir ortamda zaten kullanıyorsanız Commerce Scale Unit'in başlatılması bu bileşenler güncelleştirildiğinde kapalı kalma süresini azaltmaya yardımcı olur. Commerce Scale Unit başlatılmadan önce ek planlama gereklidir.

Bulutta barındırılan Commerce kanalı bileşenlerini kullanan bir ortamda ilk Commerce Scale Unit'inizi açtığınızda, başlatma işlemi bulutta barındırılan kanal bileşenleriyle ilişkili kanallarınızı ilk ölçek birimine taşır. Mağaza Ölçeği birimleriyle ilişkili kanallar etkilenmez.

Aktarım işlemi kanallar için şeffaftır. Ölçek birimi başlatma işlemi başladıktan sonra, aşağıdaki işlemler otomatik olarak gerçekleştirilir:

1. Yeni bir Commerce Scale Unit oluşturulur ve ortam ile ilişkilendirilir.
2. Commerce Scale Unit, genel merkezde kullanılabilir bir Kanal Veritabanı olarak kaydedilecektir.
3. Genel merkezdeki **Varsayılan** kanal veritabanına eşlenen tüm kanallar, yeni Commerce Scale Unit ile eşlenecek şekilde güncelleştirilir.
4. Kanal verilerini yeni ölçek birimine getirmek için bir Commerce Data Exchange (CDX) tam veri eşitlemesi gerçekleştirilecektir.

**Commerce Scale Unit başlatma için planlama ve test** Genel bir kural olarak, Commerce Scale Unit'i başlatırken, mağaza işlemlerinin yanı sıra Retail Server veya Cloud Point of Sale kullanan tüm e-ticaret kanalı işlemleri için beş saatlik bir kapalı kalma süresi aralığı planlamanız gerekir.

1. Üretim ortamınızdan korumalı alan UAT ortamına veritabanı yenilemesi gerçekleştirin. 
2. Korumalı alan UAT ortamında Commerce Scale Unit'i başlatın. 
3. Commerce Scale Unit için tamamlanacak başlatma süresine dikkat edin. Bu, bu işlemin üretim ortamınızda sürdüğü ve mağaza operasyonlarının ve e-ticaret işlemlerinin kullanılamadığı süreyle karşılaştırılabilir.

Commerce Scale Unit'i başlatmadan önce aşağıdaki ek adımları gerçekleştirmelisiniz.

- **Tüm POS vardiyalarını kapatın** - Geçiş işleminden sonra POS kullanıcıları geçiş işlemi sırasında etkin olan vardiyaları kapatamaz.
- **Tüm P işlerinin başarıyla tamamlandığını doğrulayın** - Bekleyen hareketleri eşitlemek için P işlerinin CSU başlatılmadan önce tamamlanması önerilir.
- **Tüm POS cihazlarında oturumu kapatın** - Geçiş sırasında POS işlemleri desteklenmez.
- **POS'ta askıya alınan tüm hareketleri geri çağırın ve geçersiz kılın** - Askıya alınan hareketler, başlatmanın bir parçası olarak korunmaz.

> [!IMPORTANT]
> Commerce Scale Unit başlatmanın bir parçası olarak, önceki askıya alınan hareketler kaybolur ve geri çağrılamaz. 

Başlatma döneminde oluşanlar şunlardır:

- POS çevrimdışı özelliğini açmadığınız sürece bulutta barındırılan Commerce kanalları çalışmaz.
- Çevrimdışı özelliği açık olan POS cihazları daha az işlevselliğe sahip olacaktır.
- Retail Server'a bağımlı olan tüm e-Ticaret istemcileri kesintiye uğrar.
- Commerce Scale Units'te (kendi kendine barındırılan) barındırılan kanallar etkilenmez.
- Merkez ofis işlevselliği etkilenmez.

Başlatma tamamlandıktan sonra oluşanlar şunlardır:

- Etkinleştirilen tüm POS cihazlarının cihaz etkinleştirme durumu korunur, bu da cihazların yeniden etkinleştirilmesi gerekmeyeceği anlamına gelir.
- Bağımsız donanım istasyonu örnekleri çalışmaya devam eder.
- POS kanal tarafı raporları sıfırlanır ve başlatmadan önceki verileri göstermez.
- Günlük işlemini göster işlemi de sıfırlanır ve başlatmadan önceki verileri göstermez.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
