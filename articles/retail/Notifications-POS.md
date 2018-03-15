---
title: "Satış Noktasında sipariş bildirimlerini görüntüleme"
description: "Bu konu, Satış Noktasında sipariş bildirimlerinin etkinleştirilmesini diğer işlemlere genişletilebilen bildirim çerçevesini açıklar."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: a1206aea3f78246951581c1dc6338e39a0942ea2
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="display-notifications-in-point-of-sale"></a>Satış Noktasında bildirimleri görüntüleme

[!include[banner](includes/banner.md)]

Bugünkü modern perakende ortamında, mağaza yetkilileri müşterilere yardım etme, hareketleri girme, stok sayımı yapma ve mağazada siparişleri alma gibi çeşitli görevlere atanmaktadır. Satış Noktası istemcisi, tek bir uygulamayla, mağaza yetkililerini bu görevleri gerçekleştirme ve çok daha fazlası için destekler. Gün içinde birçok görev yerine getiren çalışanların, dikkat etmelerini gerektiren bir konu olduğunda bildirim almaları gerekebilir. POS'taki bildirim çerçevesi, perakendecilere rol tabanlı bildirimler yapılandırma olanağı sunarak bu sorunu çözer. Uygulama güncelleştirmesi 5'e sahip Dynamics 365 for Retail'de bu bildirimler yalnızca POS işlemleri için yapılandırılabilir.

Şu anda sistem sipariş karşılama işlemi için bildirimleri görüntüleme olanağı sunmaktadır ancak çerçeve genişletilebilecek şekilde tasarlanmıştır. Bu sayede geliştiriciler gelecekte herhangi bir işlem için bildirim işleyici yazma ve bildirimleri POS'ta görüntüleme olanağına sahip olacaktır.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Sipariş karşılama işlemleri için bildirimleri etkinleştirme

Sipariş karşılama işlemleri için bildirimleri etkinleştirmek üzere aşağıdaki adımları uygulayın:

 - **İşlemler** sayfasına gidin (**Perakende** > **Kanal kurulumu** > **POS kurulumu** > **POS** > **İşlemler**).
 - Sipariş karşılama işlemini arayıp bu işlem için **Bildirimleri etkinleştir** onay kutusunu işaretleyin. Bu, bildirim çerçevesine sipariş karşılama işlemi için işleyiciyi dinlemesi gerektiğini belirtir. İşleyici uygulanırsa bildirimler POS'ta görüntülenecektir. Aksi takdirde, bu bildirimler bu işlem için görüntülenmeyecektir.
- Çalışanlarla ilişkili POS izinlerine gidin ve **Bildirimler** hızlı sekmesi altından"Görüntüleme sırası" 1 olacak şekilde Sipariş karşılama işlemini ekleyin. Birden fazla yapılandırılmış bildirim olması durumunda, görüntüleme sırası bildirimleri, 1 en üstte olacak şekilde yukarıdan aşağıya doğru düzenlemek için kullanılır. Bu işlemler yalnızca **Bildirimleri etkinleştir** onay kutusu seçili olduğunda eklenebilir. Ayrıca, bildirimler yalnızca buraya eklenmiş olan işlemler için ve işlemlerin ilgili POS izinlerine eklendiği çalışanlara gösterilir. 

> [!NOTE]
> Bildirimler çalışan kaydına gidilip **POS İzinleri** seçildikten sonra kullanıcının bildirim aboneliği düzenlenerek kullanıcı düzeyinde geçersiz kılınabilir.

 - **İşlev profili** sayfasına gidin (**Perakende** > **Kanal kurulumu** > **POS kurulumu** > **POS profilleri** > **İşlev profilleri**). **Bildirim aralığı** özelliğini güncelleştirerek bildirimlerin çekileceği aralığı dakika cinsinden ayarlayabilirsiniz. Merkezle gereksiz iletişimi önlemek için bu değeri 10 dakika olarak ayarlamanızı öneririz. Bildirim aralığının "0" olarak ayarlanması bildirimleri kapatır.  

 - **Perakende** > **Perakende BT** > **Dağıtım planı** öğesine gidin. Bildirim aboneliği ayarlarını eşitlemek için "1060-Personel" planını seçin ve ardından **Şimdi çalıştır**'a tıklayın. Sonra, "1070-Kanal yapılandırması"nı seçerek izin aralığını eşitleyin ve **Şimdi çalıştır**'a tıklayın. 

## <a name="view-notifications-in-pos"></a>POS'ta bildirimleri görüntüleme

Yukarıdaki adımlar tamamlandıktan sonra, kendileri için bildirimlerin ayarlandığı çalışanlar bildirimleri POS'ta görebilir. Bildirimleri görüntülemek için POS'taki başlık çubuğunda bulunan bildirim simgesine tıklayın. Bu, sipariş karşılama işlemi için bildirimleri içeren bildirim merkezini görüntüler. Bildirim merkezinin sipariş karşılama işlemi içinde aşağıdaki grupları görüntülemesi gerekir: 

- **Bekleyen siparişler** - Bu grup, bekleme durumunda olan, mağaza karşılama için gerekli izinlere sahip POS çalışanı tarafından kabul edilmesi gereken siparişler gibi siparişlerin sayısını görüntüler. Gruptaki sayıya tıklandığında **Sipariş karşılama** sayfası açılır. Bu sayfa, yalnızca karşılama için mağaza atanmış olan bekleme durumundaki siparişleri görüntüler. Siparişler mağaza için otomatik olarak kabul ediliyorsa, bu grup için sayı sıfır olacaktır.

- **Mağazadan çekme** - Bu grup teslimat modu **Çek** olan ve çekme işleminin geçerli mağaza için planlanmış olduğu siparişlerin sayısını gösterir. Gruptaki sayıya tıklandığında **Sipariş karşılama** sayfası açılır. Bu sayfa, yalnızca geçerli mağazadan çekilmek üzere ayarlanmış olan etkin siparişleri görüntüler.

- **Mağazadan sevkiyat** - Bu grup teslimat modu **Sevkiyat** olan ve sevkiyat işleminin geçerli mağaza için planlanmış olduğu siparişlerin sayısını gösterir. Gruptaki sayıya tıklandığında **Sipariş karşılama** sayfası açılır. Bu sayfa, yalnızca geçerli mağazadan sevk edilmek üzere ayarlanmış olan etkin siparişleri görüntüler.

Karşılama için mağazaya atanan yeni siparişler olduğunda, bildirim simgesi yeni bildirimleri gösterecek şekilde değişir ve ilgili grupların sayısı güncelleştirilir. Kullanıcı, grupların sayısını anında güncelleştirmek için işlem adının yanındaki yenile simgesine de tıklayabilir. Bu sayı önceden tanımlanan aralıklarla da güncelleştirilir. Geçerli çalışan tarafından görülmeyen ve yeni bir öğesi bulunan bir grup, bu grupta yeni bir öğe olduğunu belirtmek için bir patlama simgesi görüntüler. Bildirimlerdeki kutucuklara tıklandığında, bildirimin yapılandırıldığı işlem açılır. Yukarıdaki senaryolarda, bildirimler tıklandığında **Sipariş karşılama** sayfası açılacak ve uygun parametrelere geçilecektir: bekleyen siparişler, mağazadan çekme ve mağazadan sevkiyat. 

> [!NOTE]
> Bekleyen siparişler bildirimi, bir sonraki Dynamics 365 for Retail güncelleştirmesiyle etkinleştirilecektir. 


