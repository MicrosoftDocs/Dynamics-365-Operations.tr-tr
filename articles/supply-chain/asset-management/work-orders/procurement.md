---
title: Tedarik
description: Bu konuda Kıymet Yönetimi'ndeki tedarikleri açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875943"
---
# <a name="procurement"></a>Tedarik


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kıymet yönetiminde, iş emirleriyle ilgili satınalma taleplerinin ve satınalma siparişlerinin genel görünümünü alabilirsiniz. Bir iş emrinden bir satınalma siparişi veya satınalma talebi de oluşturulabilir.

**İş emri satınalma talebi** listesinde (**Kıymet yönetimi** > **Ortak** > **Tedarik** > **İş emri satınalma talebi**), iş emirleriyle ilgili satınalma taleplerinin listesini görürsünüz.

- **İş emri satınalma talebi** listesinden bir iş emri işi seçin ve ilgili satınalma talebini açmak için **Satınalma talebi** düğmesine tıklayın.  
- **İş emri satınalma talebi** listesinden bir iş emri işi seçin ve ilgili iş emrini açmak için **İş emri** düğmesine tıklayın.  
- **İş emri satınalma talebi** listesinde bir iş emri seçin ve seçili satırdaki öğenin Kıymet Yönetimi'nde kıymetler, bakım işi türü varsayılanları, yedek parçalar ve iş emirleri ile ilgili olarak nerede kullanıldığına ilişkin bir genel bakış elde etmek için **Kullanıldığı madde**'ye tıklayın. 

![Şekil 1](media/08-work-orders.png)


**İş emri satınalma talebi** listesinde (**Kurumsal varlık yönetimi** > **Ortak** > **Tedarik** > **İş emri satınalma talebi**), iş emirleriyle ilgili satınalma siparişlerimim listesini görürsünüz.

- **İş emri satınalma** listesinden bir iş emri işi seçin ve ilgili satınalma emrini açmak için **Satınalma emri** düğmesine tıklayın.  
- **İş emri satınalma** listesinden bir iş emri işi seçin ve ilgili iş emrini açmak için **İş emri** düğmesine tıklayın.  
- **İş emri** satınalma listesinde bir iş emri seçin ve seçili satırdaki öğenin Kıymet Yönetimi'nde kıymetler, bakım işi türü varsayılanları, yedek parçalar ve iş emirleri ile ilgili olarak nerede kullanıldığına ilişkin bir genel bakış elde etmek için **Kullanıldığı madde**'ye tıklayın. 

![Şekil 2](media/09-work-orders.png)


Yukarıda gösterilen listelerde, teslimat tarihi denetimiyle ilgili bir simge her satırın sağına yerleştirilir. Simge kırmızı daire içinde bir ünlem işareti gösteriyorsa, ilgili satınalma talebinde veya satınalma siparişinde teslimat gecikebilir.

Bir satınalma talebinde, olası gecikmeyi hesaplamak için kullanılan tarih **Satınalma talepleri** form > **Satınalma talebi başlığı** hızlı sekme > **Talep tarihi** alanında bulunur. Bu tarih, satınalma siparişi tarihiyle aynı şekilde iş emri veya iş emri işinde kullanılabilir tarihle karşılaştırılır.

Bir satınalma siparişinde, olası gecikmeyi hesaplamak için kullanılan tarih, **Satınalma siparişi** form > satınalma sipariş satırı seçme > **Satır ayrıntıları** Hızlı sekme > **Kurulum** sekme > **Onaylanan teslimat tarihi** alanında gösterilen satınalma siparişi satırıyla ilgili tarihtir. Bu alan doldurulmamışsa **Satınalma siparişi başlığı** hızlı sekmesindeki **Teslim tarihi** alanında bulunan tarih kullanılır. Bu tarihlerden biri, iş emri veya iş emri işindeki mevcut tarihle aşağıdaki sırayla karşılaştırılır:

- İş emri üzerindeki gerçek başlangıç tarihi veya  

- İlgili iş emri işi üzerinde planlanan başlangıç tarihi veya  

- İş emri üzerindeki zamanlanan başlangıç tarihi veya  

- İş emri üzerindeki beklenen başlangıç tarihi  


## <a name="create-purchase-order-from-a-work-order"></a>İş emri satınalma siparişi oluşturma

**Tüm iş emirleri**'nde, bir iş emri işi seçer ve ilgili satınalma siparişi veya satınalma talebini oluşturursunuz. Bu işlem, satınalma siparişi veya satınalma talebi ile çalışma siparişi arasında proje ilişkileri sağlamak için yapılır.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. **Tüm iş emirleri** veya **Etkin iş emirleri** listesinde, satınalma siparişi oluşturmak istediğiniz iş emrini seçin ve **Düzenle**'ye tıklayın.

3. **İş emri** formu > **İş emri bakım işleri** hızlı sekmesinde, satınalma siparişi oluşturmak istediğiniz iş emri işini seçin.

4. **Madde görevleri** > **İş emri işinden satınalma siparişi**'ne tıklayın.

5. **Proje satınalma siparişleri** listesi sayfasında, **Yeni**'ye tıklayın.

6. Satınalma siparişi oluşturun.

>[!NOTE]
>Satınalma talebi oluşturmak, bir satınalma siparişi oluşturmakla neredeyse aynıdır. Yukarıdaki yordamda, adım 2'de iş siparişi işinden **Madde görevleri** > **Bir iş emri işinden satınalma siparişi**'ne tıklayın.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>İş siparişi ve satınalma siparişi veya satınalma talebi arasındaki proje ilişkisi

Satınalma siparişi satırı veya satınalma talebi satırı, iş emri ile ilgili proje faaliyet numarası aracılığıyla iş emri işiyle ilgilidir. Bir iş emri işinden satınalma siparişi veya satınalma talebi oluşturduğunuzda, ilgili proje faaliyet numarası zorunludur. İlgili iş emri aynı bakım işi türünü kullanan iş siparişi işlerini içeriyorsa, proje faaliyet numarası bir satınalma siparişine veya satınalma talebine otomatik olarak eklenir. İş emri işleri farklı bakım işi tipleri içeriyorsa, proje faaliyet numarası el ile eklenmelidir.

Bir satınalma siparişi satırı ile ilgili faaliyet numarasını görmek veya eklemek için **İş emri satın alma** > satınalma siparişi kaydını seçin > **Satınalma siparişi** sütununda > **Satır ayrıntıları** hızlı sekmesinde > **Proje** sekmesinde > **Etkinlik numarası** alanındaki satınalma siparişine tıklayın.


![Şekil 3](media/10-work-orders.png)


Benzer şekilde bir iş emrisatınalma talebi satırı ile ilgili faaliyet numarasını görmek veya eklemek için **İş emri satın alma talebi** > satınalma siparişi kaydını seçin > **Satınalma talebi** sütununda > **Satır ayrıntıları** hızlı sekmesinde > **Proje** sekmesinde > **Etkinlik numarası** alanındaki satınalma talebine tıklayın.

