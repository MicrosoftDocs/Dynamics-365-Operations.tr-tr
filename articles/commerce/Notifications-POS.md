---
title: Satış noktasında (POS) sipariş bildirimlerini görüntüleme
description: Bu konu, satış noktasında sipariş bildirimlerinin etkinleştirilmesini ve bildirim çerçevesini açıklar.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: e663a5dca76d570217b7e02444689a2e2d312c41
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416335"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Satış noktasında (POS) sipariş bildirimlerini görüntüleme

[!include [banner](includes/banner.md)]

Modern perakende ortamında, mağaza yetkilileri müşterilere yardım etme, hareketleri girme, stok sayımı yapma ve mağazada siparişleri alma gibi çeşitli görevlere atanmaktadır. Satış noktası (POS) istemcisi, tek bir uygulamayla, mağaza yetkililerini bu görevleri gerçekleştirme ve çok daha fazlası için destekler. Gün içinde birçok görev yerine getiren çalışanların, dikkat etmelerini gerektiren bir konu olduğunda bildirim almaları gerekebilir. POS'taki bildirim çerçevesi, perakendecilere rol tabanlı bildirimler yapılandırma olanağı sunarak yardımcı olur. Dynamics 365 for Retail içinde uygulama güncelleştirmesi 5 ile, bu bildirimler yalnızca POS işlemleri için yapılandırılabilir.


Şu anda sistem bildirimleri yalnızca sipariş karşılama işlemleri için gösterir. Ancak, çerçeve genişletilebilir olması için tasarlanmış olduğundan, geliştiricilerin zaman içinde herhangi bir işlem için bir bildirim işleyicisi yazmaları ve bu işlem için bildirimi POS'ta göstermeleri söz konusudur.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Sipariş karşılama işlemleri için bildirimleri etkinleştirme

Sipariş karşılama işlemleri için bildirimleri etkinleştirmek üzere aşağıdaki adımları uygulayın.

1. **Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Operasyonlar** öğelerini seçin.
2. **Sipariş karşılama** işlemini bulun ve **Bildirimleri etkinleştir** onay kutusunu seçerek bildirim çerçevesinin bu işlem için işleyiciyi dinlemesi gerektiğini belirtin. İşleyicisi uygulanıyorsa, bu işlem için bildirimler POS'ta görüntülenir.
3. **Perakende ve Ticaret** &gt; **Personel** &gt; **Çalışanlar** &gt;'a gidin, Ticaret sekmesi altından çalışanla ilişkili POS izinlerini açın. **Bildirimler** hızlı sekmesini genişletin, **Sipariş karşılama** işlemini ekleyin ve **Görüntüleme sırası** alanını **1** olarak ayarlayın. Birden fazla bildirim yapılandırılmışsa, bu alan bildirimleri düzenlemek için kullanılır. Daha düşük **Görüntüleme sırası** değeri olan bildirimler daha yüksek bir değere sahip bildirimlerin üzerinde görünür. **Görüntüleme sırası** değeri **1** olan bildirimler en üstte olur.

    Bildirimler yalnızca **Bildirimler** hızlı sekmesinde eklenen işlemler için gösterilir ve işlemleri buraya yalnızca **Bildirimleri etkinleştir** onay kutusunun bu işlemler için **POS işlemleri** sayfasında işaretlenmiş olması durumunda ekleyebilirsiniz. Ayrıca, bir işlem için bildirimler çalışanlara yalnızca işlemin bu çalışanlar için POS izinlerine eklenmiş olması durumunda gösterilir.

    > [!NOTE]
    > Bildirimler kullanıcı düzeyinde geçersiz kılınabilir. Çalışan kaydını açın, **POS izinleri**'ni seçin ve ardından kullanıcının bildirim aboneliğini düzenleyin.

4. **Perakende ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **İşlevsellik profilleri** öğesine tıklayın. **Bildirim aralığı** alanında, bildirimlerin çekilme sıklığını belirtin. Bazı bildirimler için POS'un arka ofis uygulamasına gerçek zamanlı çağrılar yapması gerekir. Bu çağrılar, arka ofis uygulamanızın bilgi işlem kapasitesini tüketir. Bu nedenle, bildirim aralığı ayarladığınızda, hem iş gereksinimlerinizi hem de arka ofis uygulamasına yapılan gerçek zamanlı çağrıların etkisini düşünün. **0** (sıfır) değeri bildirimleri kapatır.
5. **Retail ve Commerce** &gt; **Retail ve Commerce BT** &gt; **Dağıtım planı**'na gidin. Bildirim abonelik ayarlarını eşitlemek için **1060** (**Personel**) planını ve arından **Şimdi çalıştır**'ı seçin. Sonra, **1070** (**Kanal yapılandırması**) planını seçerek izin aralığını eşitleyin ve **Şimdi çalıştır**'a tıklayın.

## <a name="view-notifications-in-the-pos"></a>POS'ta bildirimleri görüntüleme

Yukarıdaki adımları tamamladıktan sonra çalışanlar POS'ta bildirimleri görüntüleyebilir. Bildirimleri görüntülemek için POS'un sağ üst kenarındaki bildirim simgesine tıklayın. Bir bildirim merkezi açılır ve sipariş karşılama işlemi için bildirimleri görüntüler. Bildirim merkezinin sipariş karşılama işlemi içinde aşağıdaki grupları görüntülemesi gerekir:

- **Mağazadan çekme** - Bu grup teslimat modu **Çek** olan ve çekme işleminin geçerli mağaza için planlanmış olduğu siparişlerin sayısını gösterir. **Sipariş karşılama** sayfasını açmak için gruptaki numaraya basabilirsiniz. Bu durumda, sayfa filtrelenir ve yalnızca geçerli mağaza için malzeme çekme ayarlanan etkin siparişleri gösterir.
- **Mağazadan sevkiyat** - Bu grup teslimat modu **Sevkiyat** olan ve sevkiyat işleminin geçerli mağaza için planlanmış olduğu siparişlerin sayısını gösterir. **Sipariş karşılama** sayfasını açmak için gruptaki numaraya basabilirsiniz. Bu durumda, sayfa filtrelenir ve yalnızca geçerli mağazadan sevkiyatı ayarlanan etkin siparişleri gösterir.

Karşılama için mağazaya atanan yeni siparişler olduğunda, bildirim simgesi yeni bildirimleri gösterecek şekilde değişir ve ilgili grupların sayısı güncelleştirilir. Gruplar düzenli aralıklarla yenilenmesine karşın POS kullanıcıları istedikleri zaman grubun yanındaki **Yenile** düğmesini seçerek grupları el ile yenileyebilir. Son olarak, bir grupta geçerli çalışanın görüntülemediği yeni bir madde olması durumunda, grup yeni içeriği göstermek üzere bir simge gösterir.

## <a name="enable-live-content-on-pos-buttons"></a>POS düğmelerinde canlı içeriği etkinleştirme

POS düğmeleri artık çalışanların hangi görevlerle hemen ilgilenilmesi gerektiğini kolayca belirlemesine yardımcı olan bir sayı gösterir. Bu sayıyı POS düğmesine göstermek için bu konuda daha önce açıklanan bildirim ayarını tamamlamanız gerekir (bir işlem için bildirimleri etkinleştirmeniz, bir bildirim aralığı ayarlamanız ve çalışan için POS izin grubunu güncelleştirmeniz gerekir). Ayrıca, düğme grubu tasarımcısını açmanız, düğmenin özelliklerini görüntülemeniz ve **Canlı içeriği etkinleştir** onay kutusunu seçmeniz gerekir. **İçerik hizalama** alanında, sayının düğmenin sağ üst köşesinde mi (**Sağ üst**) yoksa ortasında mı (**Merkez**) görüntüleneceğini seçebilirsiniz.

> [!NOTE]
> Canlı içerik **Bildirimleri etkinleştir** onay kutusunun işlemler için daha önce açıklandığı şekilde **POS işlemleri** sayfasından seçilmiş olması durumunda işlemler için seçilebilir.

Aşağıdaki örnek düğme grubu tasarımcısındaki canlı içerik ayarlarını göstermektedir.

![Düğme grubu tasarımcısında canlı içerik ayarları](./media/ButtonGridDesigner.png "Düğme grubu tasarımcısında canlı içerik ayarları")

Bir düğmedeki bildirim sayımını göstermek için, doğru ekran düzeninin güncelleştirilmesini sağlamanız gerekir. POS tarafından kullanılan ekran düzenini belirlemek için, sağ üst köşedeki ayarlar **Ayarlar** simgesini seçin ve **Ekran düzeni kodunu** ve **Düzen çözünürlüğünü** not edin. Şimdi Edge tarayıcısını kullanarak **Ekran düzeni** sayfasına gidin, yukarıda tanımlanan **Ekran düzeni kimliği** ile **Düzen çözünürlüğü** öğelerini bulun ve **Canlı içeriği etkinleştir** onay kutusunu seçin. **Perakende ve Ticaret \> Perakende ve Ticaret BT \> Dağıtım zamanlaması**'na gidin ve düzen değişikliklerini eşitlemek için 1090 (Kayıtlar) işini çalıştırın.


![POS 'un kullandığı ekran mizanpajını bul](./media/Choose_screen_layout.png "Ekran düzenini bulun")

Aşağıdaki örnekte, farklı boyuttaki düğmeler için **İçerik hizalama** alanında **Sağ üst** ve **Merkez** seçimlerinin etkisini göstermektedir.

![POS düğmelerinde canlı içeriği](./media/ButtonsWithLiveContent.png "POS düğmelerinde canlı içeriği")
