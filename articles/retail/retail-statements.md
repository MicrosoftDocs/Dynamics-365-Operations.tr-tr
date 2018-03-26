---
title: Perakende ekstreleri
description: "Bu konu ekstrelerin nasıl oluşturulacağını ve deftere nakledileceğini açıklar."
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: ddceadb797af98f85670df72a335b2714fe2f01e
ms.contentlocale: tr-tr
ms.lasthandoff: 03/08/2018

---

# <a name="retail-statements"></a>Perakende ekstreleri

[!include[banner](includes/banner.md)]

Microsoft Dynamics 365 for Retail içerisinde, ekstre deftere nakletme işlemi, Bulut satış noktası (POS) veya Modern POS (MPOS) içerisinde gerçekleşen hareketlerin muhasebesini yapmak için kullanılır. Beyan deftere nakil işlemi, bir POS hareket kümesini merkez (HQ) istemcisine çekmek için dağıtım planlama kullanılır. **Perakende parametreleri** ve **Mağazalar** sayfalarında tanımlanan parametreler, tek tek ekstrelere çekilecek hareketleri seçmek için kullanılır.  

Aşağıdaki çizimde ekstre deftere nakletme işlemi gösterilmiştir. Bu işlemde, POS içerisinde kaydedilen hareketler, istemciye Perakende planlayıcısı kullanılarak aktarılır. İstemci hareketleri aldıktan sonra, mağaza için hareket ekstrelerinı oluşturabilir, hesaplayabilir ve deftere nakledebilirsiniz. 

[![Beyan deftere nakletme işlemi](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>ekstreleri oluşturmak ve deftere nakletmek
Bir ekstreyi el ile veya periyodik olarak gün içinde çalışmak üzere ayarlamış olduğunuz toplu iş işlemlerini kullanarak oluşturabilirsiniz. Her iki durumda da, aşağıdaki adımlar ekstreleri oluşturmak ve deftere nakletmek için kullanılır.

###  <a name="create-the-statement"></a>Ekstre oluşturma
Bu adım, ekstrenin el ile oluşturulduğu mağazayı tanımlar. Bir toplu iş işlemini yapılandırırsanız, tüm bu mağazalar için otomatik olarak ekstreleri, belirlediğiniz plana uygun olarak oluşturabilirsiniz. 

### <a name="calculate-the-statement"></a>Ekstreyi hesaplama
Bu adımda, hareket satırları **Perakende parametreleri** ve **Mağazalar** sayfalarında tanımlanan her bir mağaza için ölçüte dayalı olarak seçilir. Bu sayfalarda, hareketleri tanımlarsınız ve hareketlerin nasıl hesaplandığını belirtirsiniz. Ekstreyi hesaplamadan önce ekstreye dahil edilmiş olan hareketlerin bir listesini görüntülemek için, **Hareketler** sayfasını kullanın. 

Ekstre hesaplaması, kasalardan sayımlarında sayılan tutar beyanlarını kullanır. Ayrıca, düzeltilen tutarı el ile de girebilirisiniz. Ekstre, tüm ödeme tiplerindeki hareket için satış tutarı ve gerçek hesaplanan tutar arasındaki farkı gösterir. Ekstre, yalnızca bu fark mağaza için tanımlanan maksimum seçilen deftere nakil farkından az ise deftere nakledilir. 

> [!NOTE]
> Ekstre hesaplama işlemi genel numara sırasını kullanır.

Bir ekstreyi hesapladığınızda, hesaplama aşağıdaki görevleri içerir:

- Seçilen bir veri aralığı için, önceki ekstre hesaplamasına dahil edilmemiş olan hareketleri işaretleyin. 
- Seçili hareketlerde sayılan toplam tutarları hesaplayın. Sonuçlar ekstre satırlarında, ekstre yöntemine bağlı olarak gösterilir:

  - Ekstre yöntemi **Toplam** ise, seçilen hareketlerdeki her bir ödem yöntemi için bir satır oluşturulur. 
  - Ekstre yöntemi **Personel** ise, seçilen personel üyesi tarafından gerçekleştirilen hareketlerdeki her ödeme türü için bir satır oluşturulur. 
  - Ekstre yöntemi **POS Terminali** ise, seçilen kayıt üzerinde gerçekleştirilen hareketlerdeki her ödeme yöntemi için bir satır oluşturulur. 
  - Ekstre yöntemi **Vardiya** ise, vardiya sırasında gerçekleştirilen hareketlerdeki her ödeme yöntemi için bir satır oluşturulur.

**Ekstre yöntemine göre böl** onay kutusu **Mağazalar** sayfasında seçilmişse, **Ekstre yöntemi** alanında seçilmiş olan değere dayanarak ayrı bir ekstre oluşturulur.

Mağazanızın çalışma saatleri gece yarısını geçiyorsa, ekstre deftere nakillerini, takvim gününün sonuna değil, iş gününün sonuna dayanacak şekilde yapılandırabilirsiniz. 

**Mağazalar** sayfasında **Ekstre/kapatma** hızlı sekmesinde, **İş günü sonu** alanında, son hareketin kaydedilmesi ve iş gününü ekstresine dahil edilmesi gereken saati seçin. **İş günü olarak deftere naklet** onay kutusunu, hareketleri aynı iş gününde deftere nakletmek için seçin. Ekstre deftere nakledildiğinde, aynı iş günü içerisinde kaydedilmiş olan hareketler aynı satış siparişlerine dahil edilebilir, bazı hareketler gece yarısından önce, bazıları da gece yarısından sonra gerçekleşseler bile. 

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Örnek: İki takvim gününü aşan bir iş günü için bir ekstre deftere nakledin 

Bir mağaza 08:00 ve 03:00 arasında açıktır, ve **İş günü olarak deftere naklet** onay kutusu, mağazanın yapılandırmasında seçilidir. 31 Mayıs'ta, mağaza 08:00 ve gece yarısı arasında hareketleri kaydeder. Mağaza ayrıca 1 Haziran 00:01 ve 03:00 arasındaki hareketleri de kaydeder. 

Mağaza, iş gününün kapanışı için ekstresini deftere naklettiğinde, oluşturulan satış siparişi 08:00 ve 03:00 iş saatleri arasında kaydedilen tüm hareketleri içerir; hareketler iki gün içerisinde oluşmuş olsa bile, 31 Mayıs ve 1 Haziran. 

**Bir iş günü olarak deftere naklet** onay kutusu aynı mağaza için işaretli değilse, mağaza ekstresini iş gününün sonunda deftere naklettiğinde ayrı satış siparişleri oluşturulur. Bir satış siparişi, iş saatleri 08:00 ve 31 Mayıs gece yarısı arasında kaydedilen hareketleri içerir, diğer satış siparişi, iş saatleri 00:01 ve 03:00 1 Haziran'da kaydedilen hareketleri içerir.
 
> [!NOTE]
> Ekstreler oluşturabilmeden önce, ekstre dönemindeki vardiyaları kapatmanız gerekir. 

### <a name="post-the-statement"></a>Ekstreyi deftere nakletme
Bir ekstreyi deftere naklettiğinizde, satış siparişleri ve faturalar, ekstre içindeki perakende satışlar için oluşturulur.

- Peşin alışveriş satışlar bir satış siparişinde toplanır ve mağazaya atanmış olan varsayılan kullanıcıya faturalanır. 
- Microsoft Dynamics 365 for Retail POS içerisinde bir harekete bir müşterinin eklenmiş olduğu perakende satışları, her bir benzersiz müşteri için ayrı satış siparişleri ve faturalar oluşturur. 

Ödeme günlükleri, ekstredeki ödemeler için otomatik olarak oluşturulur ve stok, POS mağazası için güncelleştirilir.

