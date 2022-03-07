---
title: Satış noktasında (POS) sipariş bildirimlerini görüntüleme
description: Bu konu, satış noktasında sipariş bildirimlerinin etkinleştirilmesini ve bildirim çerçevesini açıklar.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7166afdb43c7e835170c5768a0767f2943222b19c00c7d0aaf067263845651f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714150"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Satış noktasında (POS) sipariş bildirimlerini görüntüleme

[!include [banner](includes/banner.md)]

Mağaza çalışanlarına, siparişleri yerine getirmek veya stok girişi veya stok sayımları gerçekleştirmek gibi çeşitli görevler atanabilir. Satış noktası (POS) istemcisi, tek bir uygulamayla, mağaza yetkililerini bu görevlerle ilgili bilgilendirir. POS'taki bildirim çerçevesi, perakendecilere rol tabanlı bildirimler yapılandırma olanağı sunarak yardımcı olur. Dynamics 365 Retail içinde uygulama güncelleştirmesi 5 ile başlayarak, bu bildirimler POS işlemleri için yapılandırılabilir.

Sistem *sipariş karşılama* işlemi için bildirimler gösterebilir ve Commerce 10.0.18 sürümünden başlayarak bildirimleri, *sipariş geri çekme* işlemi için de gösterebilir. Ancak, çerçeve genişletilebilir olması için tasarlanmış olduğundan, geliştiricilerin herhangi bir işlem için bir [bildirim işleyicisi yazmaları](dev-itpro/extend-pos-notification.md) ve bu işlem için bildirimi POS'ta göstermeleri söz konusudur.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Sipariş karşılama veya sipariş geri çekme işlemleri için bildirimleri etkinleştirme

Sipariş karşılama veya sipariş geri çekme işlemleri için bildirimleri etkinleştirmek üzere aşağıdaki adımları uygulayın.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Operasyonlar** öğelerini seçin.
1. **Sipariş karşılama** veya **Sipariş geri çekme** işlemini arayın ve **Bildirimleri etkinleştir** onay kutusunu seçerek bildirim çerçevesinin bu işlem için işleyiciyi dinlemesi gerektiğini belirtin. İşleyicisi uygulanıyorsa, bu işlem için bildirimler POS'ta görüntülenir.
1. **Retail ve Commerce \> Personel \> Çalışanlar** menüsüne gidin.
1. **Commerce** sekmesini seçin, bir çalışan satırı seçin ve sonra **POS izinleri**'ni seçin. Bunu genişletmek için **bildirimler** hızlı sekmesini seçin ve sonra bildirimleri etkinleştirmiş olduğunuz operasyonları ekleyin. Bir çalışan için tek bir bildirim yapılandırıyorsanız **görüntüleme sırası** değerinin **1** olarak ayarlandığından emin olun. Birden fazla işlem yapılandırıyorsanız **görüntüleme sırası** değerlerini bildirimlerin görüntüleneceği sırayı gösterecek şekilde ayarlayın. 

      Bildirimler yalnızca **Bildirimler** hızlı sekmesinde eklenen operasyonlar için gösterilir. Yalnızca **POS işlemleri** sayfasında bu işlemler için **bildirimleri etkinleştir** onay kutuları işaretliyse buraya işlem ekleyebilirsiniz. Ayrıca, bir işlem için bildirimler çalışanlara yalnızca işlemin bu çalışanlar için POS izinlerine eklenmiş olması durumunda gösterilir.

    > [!NOTE]
    > Bildirimler kullanıcı düzeyinde geçersiz kılınabilir. Bunu yapmak için çalışan kaydını açın, **POS izinleri**'ni seçin ve ardından kullanıcının bildirim aboneliğini düzenleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS profilleri \> İşlevsellik profilleri** öğesine tıklayın. **Bildirim aralığı** alanında, bildirimlerin çekilme sıklığını belirtin. Bazı bildirimler için POS'un arka ofis uygulamasına gerçek zamanlı çağrılar yapması gerekir. Bu çağrılar, arka ofis uygulamanızın bilgi işlem kapasitesini tüketir. Bu nedenle, bildirim aralığı ayarladığınızda, hem iş gereksinimlerinizi hem de arka ofis uygulamasına yapılan gerçek zamanlı çağrıların etkisini düşünün. **0** (sıfır) değeri bildirimleri kapatır.
1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin. Bildirim abonelik ayarlarını eşitlemek için **1060** (**Personel**) planını ve arından **Şimdi çalıştır**'ı seçin. Sonra, **1070** (**Kanal yapılandırması**) planını seçerek izin aralığını eşitleyin ve **Şimdi çalıştır**'a tıklayın.

## <a name="view-notifications-in-the-pos"></a>POS'ta bildirimleri görüntüleme

Yukarıdaki adımları tamamladıktan sonra çalışanlar POS'ta bildirimleri görüntüleyebilir. Bildirimleri görüntülemek için POS'un sağ üst kenarındaki bildirim simgesini seçin. Bir bildirim paneli görünür ve çalışan için yapılandırılan işlemlerle ilgili bildirimleri gösterir. 

**Sipariş karşılama** işlemi için bildirim paneli şu grupları görüntüler:

- **Mağazadan çekme**: Bu grup çekme işleminin geçerli mağaza için planlanmış olduğu tek tek sipariş satırlarının sayısını gösterir. **Sipariş karşılama** işlemini bir filtreyle açmak için gruptaki numarayı seçebilirsiniz böylece yalnızca geçerli mağazadan malzeme çekme için ayarlanan etkin sipariş satırları görüntülenir.
- **Mağazadan seviyat**: Bu grup, kullanıcının geçerli mağazasından sevk edilmek üzere yapılandırılan tek tek sipariş satırı sayısını gösterir. **Sipariş karşılama** işlemini bir filtreyle açmak için gruptaki numarayı seçebilirsiniz böylece yalnızca geçerli mağazadan sevk edilmek için ayarlanan etkin sipariş satırları görüntülenir.

**Sipariş geri çekme** işlemi için bildirim paneli şu grupları görüntüler:

- **Karşılanacak siparişler**: Bu grup, kullanıcının geçerli mağazası için sipariş çekme veya sevkiyat karşılama için yapılandırılan sipariş sayısını gösterir. **Sipariş geri çekme** işlemini yalnızca kullanıcının geçerli mağazası tarafından mağazadan çekme ya da mağazadan sevk senaryosu için karşılanması gereken açık siparişleri gösteren filtreli bir görünümle açmak için gruptaki numarayı seçebilirsiniz.
- **Çekilecek siparişler**: Bu grup çekme işleminin geçerli mağaza için planlanmış olduğu siparişlerin sayısını gösterir. **Sipariş geri çekme** işlemini yalnızca kullanıcının geçerli mağazasından müşteri teslim alması için karşılanması gereken açık siparişleri gösteren filtreli bir görünümle açmak için gruptaki numarayı seçebilirsiniz.
- **Sevk edilecek siparişler**: Bu grup, kullanıcının geçerli mağazasından sevk edilecek siparişlerin sayısını gösterir. **Sipariş geri çekme** işlemini yalnızca kullanıcının geçerli mağazasından sevkiyat için karşılanması gereken açık siparişleri gösteren filtreli bir görünümle açmak için gruptaki numarayı seçebilirsiniz.

Hem sipariş karşılama hem de sipariş geri çekme bildirimleri için, yeni siparişler işlem tarafından alındığında bildirim simgesi yeni bildirimleri gösterecek şekilde değişir ve ilgili grupların sayısı güncelleştirilir. Gruplar düzenli aralıklarla yenilenmesine karşın POS kullanıcıları istedikleri zaman grubun yanındaki **Yenile** düğmesini seçerek grupları el ile yenileyebilir. Son olarak, bir grupta geçerli çalışanın görüntülemediği yeni bir madde olması durumunda, grup yeni içeriği göstermek üzere bir simge gösterir.

## <a name="enable-live-content-on-pos-buttons"></a>POS düğmelerinde canlı içeriği etkinleştirme

POS düğmeleri artık çalışanların hangi görevlerle hemen ilgilenilmesi gerektiğini kolayca belirlemesine yardımcı olan bir sayı gösterir. Bu sayıyı POS düğmesine göstermek için bu konuda daha önce açıklanan bildirim ayarını tamamlamanız gerekir (bir işlem için bildirimleri etkinleştirmeniz, bir bildirim aralığı ayarlamanız ve çalışan için POS izin grubunu güncelleştirmeniz gerekir). Ayrıca, düğme grubu tasarımcısını açmanız, düğmenin özelliklerini görüntülemeniz ve **Canlı içeriği etkinleştir** onay kutusunu seçmeniz gerekir. **İçerik hizalama** alanında, sayının düğmenin sağ üst köşesinde mi (**Sağ üst**) yoksa ortasında mı (**Merkez**) görüntüleneceğini seçebilirsiniz.

> [!NOTE]
> Canlı içerik **Bildirimleri etkinleştir** onay kutusunun işlemler için daha önce açıklandığı şekilde **POS işlemleri** sayfasından seçilmiş olması durumunda işlemler için seçilebilir.

Aşağıdaki örnek düğme grubu tasarımcısındaki canlı içerik ayarlarını göstermektedir.

![Düğme grubu tasarımcısında canlı içerik ayarları.](./media/ButtonGridDesigner.png "Düğme grubu tasarımcısında canlı içerik ayarları")

Bir düğmedeki bildirim sayımını göstermek için, doğru ekran düzeninin güncelleştirilmesini sağlamanız gerekir. POS tarafından kullanılan ekran düzenini belirlemek için, sağ üst köşedeki ayarlar **Ayarlar** simgesini seçin ve **Ekran düzeni kodunu** ve **Düzen çözünürlüğünü** not edin. Şimdi Edge tarayıcısını kullanarak **Ekran düzeni** sayfasına gidin, yukarıda tanımlanan **Ekran düzeni kimliği** ile **Düzen çözünürlüğü** öğelerini bulun ve **Canlı içeriği etkinleştir** onay kutusunu seçin. **Perakende ve Ticaret \> Perakende ve Ticaret BT \> Dağıtım zamanlaması**'na gidin ve düzen değişikliklerini eşitlemek için 1090 (Kayıtlar) işini çalıştırın.

![POS 'un kullandığı ekran düzenini bulma.](./media/Choose_screen_layout.png "Ekran düzenini bulun")

Aşağıdaki örnekte, farklı boyuttaki düğmeler için **İçerik hizalama** alanında **Sağ üst** ve **Merkez** seçimlerinin etkisini göstermektedir.

![POS düğmelerinde canlı içerik.](./media/ButtonsWithLiveContent.png "POS düğmelerinde canlı içeriği")

[!INCLUDE[footer-include](../includes/footer-banner.md)]
