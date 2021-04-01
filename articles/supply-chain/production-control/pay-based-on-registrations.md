---
title: Kayıtlara dayalı ödeme
description: Bu konu ödemenin çalışan kayıtları temel alınarak nasıl hesaplanacağını açıklar.
author: johanhoffmann
manager: tfehr
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed2ee6c09f8b8a404d36c635eb5dbd9383653f81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250418"
---
# <a name="pay-based-on-registrations"></a>Kayıtlara dayalı ödeme

[!include [banner](../includes/banner.md)]

Bu konu ödemenin çalışan kayıtları temel alınarak nasıl hesaplanacağını ayrıntılarıyla açıklar. Hesaplama için kullanılan çeşitli kurulum seçenekleri kombinasyonlarının sonucu nasıl etkilediğini gösteren örnekler içerir. Ele alınacak alanlardan bazılarını aşağıda bulabilirsiniz:

- Esnek zaman
- Fazla mesai
- Molalar
- Geçiş kodları
- Ödeme maddeleri
- Ödeme sözleşmeleri
- Saat ve işe devam hesaplama parametreleri
- Devamsızlık

## <a name="the-use-of-flex-time"></a>Esnek zaman kullanımı

Esnek zaman dönemleri Saat ve işe devamda kullanılan zaman profillerinde ayarlanır. İki esnek profil türü vardır: **Esnek+** ve **Esnek-**. Bir çalışan için zaman Esnek+ döneminde kaydedildiğinde, çalışanın esnek bakiyesi çalıştığı saatlere göre artırılır. Çalışan Esnek+ döneminde çalışmış olduğu saatler için herhangi bir ücret almaz. Ancak, çalışan Esnek- dönemlerinde izin alabilir ve esnek bakiyesindeki saatler ile ücretlendirilir. Bu nedenle, esnek dönemlerdeki izinler sistem tarafından devamsızlık olarak dikkate alınır.

## <a name="scenarios-based-on-flex-periods"></a>Esnek dönemleri temel alan senaryolar

Aşağıdaki iki senaryo bir iş gününü temsil eden bir esnek profili temel almaktadır. Her iki senaryo için ödeme çalışanın giriş ve çıkış yaptığı esnek döneme göre hesaplanır.

### <a name="flex-profile-for-one-workday"></a>Bir iş günü için esnek profil

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Senaryo 1: Bir çalışan giriş saatini Esnek+ dönemde ve çıkış saatini Esnek- dönemde kaydeder

Çalışanın güne ilişkin kayıtları şu şekilde görünür.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 06:30 | 06:30 |
| Üretim işi            | 06:30 | 14:45 |
| Çıkış saati                 | 14:45 | 14:45 |

Çalışanın günlük kayıtları hesaplanır ve ödenmek üzere **Onay** sayfasına aktarılır (**Saat ve işe devam** &gt; **Gözden geçirme ve onaylama** &gt; **Onay**). Kayıtlar hesaplandıktan sonra hesaplamanın sonucu **Saatler** sekmesinde görülebilir. 

Bu senaryoyu anlamak için aşağıdaki alanlara bakın.

| Esnek + | Esnek - | Saat | Ödeme zamanı |
|--------|--------|------|----------|
| 0,50   | 0,75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Esnek+ hesaplaması

Esnek profile göre, 06:00 ile 07:00 arasındaki süre Esnek+ dönemdir. Bu nedenle çalışan 06:30'da giriş yaparsa 0,5 saat kazanır. Bu sürenin tutarı çalışanın esnek hesabına eklenir.

#### <a name="calculation-of-flex-"></a>Esnek- hesaplaması

Esnek profile göre Esnek- dönemi 14:30'da başlar ve 15:30'da biter. Bu nedenle çalışan 14:45'te çıkış yaparsa Esnek- döneminde kalan 45 dakika (0,75 saat) ödeme saati olarak kaydedilir ve aynı tutar çalışanın esnek hesabından düşülür. Çalışana Esnek- döneminde kalan 45 dakika için ödeme yapılacağından 45 dakika ödeme saatine dahil edilir. Çalışan Esnek- döneminde devamsızlık yaparsa, 45 dakika esnek hesabından düşülür.

#### <a name="calculation-of-time"></a>Saati hesaplama

Saat giriş saati ile çıkış saati arasında geçen süre olarak hesaplanır, bu da 06:30 ile 14:45 arasındaki 8,25 saate eşittir.

#### <a name="calculation-of-pay-time"></a>Ödeme saatini hesaplama

Ödeme saati çalışana ödeme yapılan süredir. Bu senaryoda, çalışan işte 8,25 saat kalır (**Saat**). Bununla birlikte, Esnek- dönemde çalışana çıkış yaptığı saatten sonra ödeme verildiği için **Ödeme saati** 8,50 olarak hesaplanır. Esnek+ saati çalışanın ödeme saatine değil esnek hesabına eklendiğinden ödeme saati planlanan çalışma saatine eşittir. Esnek- dönemindeki devamsızlık saati ödeme saati ile telafi edilir ve çalışanın esnek hesabından düşülür.

| Saat              | Kayıt türü | Ödeme saati (saat)      |
|-------------------|-------------------|-----------------------|
| 6:30 - 7:00 | Esnek+             | 0                     |
| 7:00 – 14:45 | Standart zaman     | 7,75                  |
| 14:45 – 15:30 | Esnek-             | 0,75 (Devamsızlık dönemi) |
|                   | Toplam             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Senaryo 2: Çalışan tam Esnek- dönemi boyunca çalışır ve ayrıca fazla mesai yapar

Çalışan için günlük kayıtlar şu şekilde görünür.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 06:30 | 06:30 |
| Üretim işi            | 06:30 | 17:00 |
| Çıkış saati                 | 17:00 | 17:00 |

Günlük kayıtlarını hesapladıktan sonra **Onay** sayfasındaki **Saatler** sekmesinde hesaplama sonucunu görebilirsiniz. Bu senaryoyu anlamak için aşağıdaki alanlara bakın.

| Esnek + | Esnek - | Saat  | Ödeme zamanı | Fazla mesai ödemesi |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 1,50         |

#### <a name="calculation-of-flex"></a>Esnek+ hesaplaması

Esnek profile göre, 06:00 ile 07:00 arasındaki süre Esnek+ dönemdir. Bu nedenle çalışan 06:30'da giriş yaparsa, esnek bakiyesinde 0,5 saat Esnek+ zaman kazanır.

#### <a name="calculation-of-flex-"></a>Esnek- hesaplaması

Çalışan Esnek- döneminde çalıştığından, Esnek- dönemi hesaplanmaz. Esnek- yalnızca çalışanın Esnek- döneminde devamsız olması durumunda hesaplanır. Ödeme açısından bakıldığında, çalışanın Esnek- döneminde çalışmış olması durumunda, çalışana standart zaman için tanımlanan ücret verilir. Çalışanın Esnek- döneminde devamsızlık yapmış olması durumunda, 45 dakika esnek hesabından düşürülür.

#### <a name="calculation-of-time"></a>Saati hesaplama

Saat 06:30 olan giriş saati ile 17:00 olan çıkış saati arasındaki zaman olaran veya 10,50 saat olarak hesaplanır.

#### <a name="calculation-of-pay-time"></a>Ödeme saatini hesaplama

Bu senaryoda, çalışan 10,50 saat işte kalır (**Saat**). Bununla birlikte, çalışana Esnek+ döneminde ödeme verilmediğinden **Ödenen saat** 10,00 saat olarak hesaplanır.

#### <a name="calculation-of-pay-overtime"></a>Fazla mesai ödemesini hesaplama

| Saat               | Kayıt türü | Ödeme saati (saat) |
|--------------------|-------------------|------------------|
| 6:30 - 7:00  | Esnek+             | 0                |
| 7:00 – 14:30  | Standart zaman     | 7,50             |
| 14:30 – 15:30  | Esnek-             | 1.00             |
| 15:30 – 17:00 | Fazla mesai          | 1,50             |
|                    | Toplam             | 10,00            |

### <a name="generation-of-pay-items"></a>Ödeme maddeleri oluşturma

Güne ilişkin çalışan kayıtları **Onay** sayfasından aktarılabilir. Aktarma sürecinde, ödeme maddeleri ve aktarılan kayıtlar oluşturulur. Ödeme maddeleri ödenen saatlerin standart saat, fazla mesai, ücretli mola saati gibi ödeme saatlerini gösteren dökümünü temsil eder.

Ödeme maddeleri listesini açmak için **Saat ve işe devam** &gt; **Gözden geçirme ve onaylama** &gt; **Onay** öğesini seçin. Sonra **Sorgula** &gt; **Aktarılan kayıtlar**'ı seçin.

Ödeme maddeleri bir çalışan yapılan ödemenin temelidir. Ödeme saatlerinden alınan bilgileri içeren bir dosyal oluşturup dosyayı bordro sistemine aktarabilirsiniz.

Aktarma işleminin bir parçası olarak, üretim ve proje faaliyetlerinden alınan zaman ve maliyet zaman ve maliyet harcamasını muhasebeleştirmek için üretim ve proje günlüklerine aktarılır. Aktarılan kayıtlar üretim emirleri ve projelere için zaman ve saat başına maliyet fiyatının temelidir. Aktarılan kayıtları **Onay** sayfasındaki **Sorgula** menüsünü kullanarak açabilirsiniz.

Örneğin, Senaryo 2 için aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret  | Toplam maliyet |
|---------------|----------|-----------|-------|------------|
| Standart zaman | 1201     | 10,0      | 10    | 100        |
| Fazla mesai      | 1301     | 1,50      | 5     | 7,50       |
|               |          |           | Toplam | 107,50     |

Standart saate ilişkin ödeme maddesinin ödeme birimi 10 saattir ve bu standart saati, Esnek- saati ve fazla mesaiyi kapsar. Standart saat, Esnek- saati ve fazla mesai tek bir ödeme maddesinde konsolide edilir. Bunun nedeni tüm türlerin **Hesaplama parametreleri** sayfasındaki parametresindeki varsayılan ayara göre (**Saat ve işe devam** &gt; **Kurulum** &gt; **Hesaplama parametreleri**) standart saat olarak hesaplanmasıdır. Fazla mesai, ilave 5 oranı kullanılarak standart saatin üzerinde hesaplanır.

Standart saat ile fazla mesaiyi açık bir şekilde ayırmak isterseniz (bu durumda ödeme türleri için ödeme birimleri yalnızca standart zaman ve fazla mesai için harcanan gerçek saatleri kapsar), standart saat için ödeme birimlerinin 8,50 ve fazla mesai için ödeme birimlerinin 1,50 olarak hesaplanması gerekir.

Sistemi standart saat ile fazla mesaiyi açıkça ayıracak şekilde yapılandırmak için, fazla mesaiyi standart saatin dışında bırakmanız gerekir. Ayrıca, fazla mesai için ödeme türü ayarını değiştirmeniz gerekir. Bu durumda, fazla mesai ödeme oranı fazla mesaide harcanan saatlere ilişkin tüm ödemeleri kapsar.

### <a name="exclude-overtime-from-the-standard-time"></a>Fazla mesaiyi standart saatin dışında tutma

**Hesaplama parametreleri** sayfasında, profil özellik türü olarak **Fazla mesai**'yi seçin ve **Ödeme saati** seçeneğini burada gösterildiği gibi **Hayır** olarak ayarlayın.

| Kayıt belirtimi | Profil belirtim türü | Hesaplama   |     | Ücretli         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Çalışma zamanı       | Fazla mesai                   | Standart zaman | Evet | Ödeme zamanı     | Hayır  |
|                    |                            | Ödeme zamanı      | Evet | Fazla mesai ödemesi | Evet |

Hesaplama parametrelerini ayarladıktan sonra, aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret  | Toplam maliyet |
|---------------|----------|-----------|-------|------------|
| Standart zaman | 1201     | 8,50      | 10    | 85,0       |
| Fazla mesai      | 1301     | 1,50      | 15    | 22,50      |
|               |          |           | Toplam | 107,50     |

> [!NOTE]
> Hesaplama parametreleri önerilen standart ayara sahiptir. Genel olarak, bu parametreleri değiştirdirirken dikkatli olmanız gerekir. Önerilen standart ayarları geri yüklemek için **Hesaplama parametreleri** sayfasında **Değerleri geri yükle**'yi seçin.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Standart ödeme profillerinden sapmaya izin verme

**Profiller** sayfasında (**Saat ve işe devam** &gt; **Kurulum** &gt; **Saat profilleri** &gt; **Profiller**), geçiş kodlarını ve molaları içeren profil türlerini ayarlayabilirsiniz.

### <a name="switch-codes"></a>Geçiş kodları

Geçiş kodlarını çalışanlara farklı bir profil türüyle değişiklik yaparak profil türlerinden sapma yapma olanağı tanıyabilirsiniz. Örneğin, çalışana Esnek+ saatinden fazla mesaiye değişiklik yapma izni verebilirsiniz. Çalışan kayıt sırasında bir geçiş kodu ekleyebilir veya geçiş kodu ekleme görevini kayıtları onaylayan kişiye atayabilirsiniz.

Bir geçiş kodunun kullanılabilmesi için kodu dolaylı faaliyet türü olarak tanımlamanız gerekir. Profil türü değişikliğine izin vermek istediğiniz dönem için zaman profiline geçiş kodu eklemeniz gerekir. Örneğin, Esnek+ döneminin 06:00 ile 07:00 arasında fazla mesai olarak değiştirilmesine izin vermek üzere bir geçiş kodu oluşturmak için aşağıdaki adımları izleyin.

1. **OTBCI (Giriş saati öncesinde esneği fazla mesaiye dönüştürme)** adlı bir geçiş kodu oluşturun. **Saat ve işe devam** &gt; **Dolaylı faaliyetleri yönet** &gt; **Dolaylı faaliyetler**'i seçin.
2. **Geçiş kodu** sütununda OTBCI'yi zaman profilinde Esnek+ satırına ekleyin.
3. **İkincil** sütunda **Fazla mesai** profil türünü ekleyin.

Bir iş gününü gösteren aşağıdaki esnek profili göz önünde bulundurun.

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

Çalışanın günlük kayıtları aşağıdaki gibidir.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 06:30 | 06:30 |
| Üretim işi            | 06:30 | 14:45 |
| Çıkış saati                 | 17:00 | 17:00 |

Aşağıdaki ödeme maddeleri aktarımdan sonra oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret  | Toplam maliyet |
|---------------|----------|-----------|-------|------------|
| Standart zaman | 1201     | 8,50      | 10    | 85,0       |
| Fazla mesai      | 1305     | 1,50      | 15    | 22,50      |
|               |          |           | Toplam | 107,50     |

**Onay** sayfasında aktarımı geri alın ve daha sonra **Geçiş kodu** menüsünü kullanarak **OTBCI** geçiş kodunu uygulayın. Kayıtları ikinci kez aktardığınızda aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret  | Toplam maliyet |
|---------------|----------|-----------|-------|------------|
| Standart zaman | 1201     | 8,50      | 10    | 80,0       |
| Fazla mesai      | 1305     | 2.00      | 15    | 30,0       |
|               |          |           | Toplam | 107,50     |

> [!NOTE]
> Geçiş kodunu uyguladığınızda, fazla mesai 0,5 saat artarak 1,50'den 2,00'a yükselir. 0,5 saat, 06:30 ile 07:00 arasındaki fazla mesaiden kayıtlı olan Esnek+ saatine dönüşümdür.

### <a name="breaks"></a>Molalar

İşe verilen molalar çalışan ödemesi hesaplamasını etkiler. Molalar dolaylı faaliyet türü olarak tanımlanır. Molanın çalışanın ödemesine eklenmesini sağlamak üzere **Ücretli** veya molanın çalışanın ödemesine eklenmesini önlemek için **Ücretsiz** olarak tanımlanabilir. Bir mola ayrıca **Planlı** veya **Kayıtlı** olarak da tanımlanabilir.

#### <a name="planned-breaks"></a>Planlı molalar

Bir şirketin öğle yemeği molası gibi sabit mola süresi varsa, mola zaman profilinde önceden tanımlanabilir. Bu durumda, çalışanın molayı iş kartı sayfalarına kaydetmesi gerekmez. Bunun yerine, mola çalışanın kayıtları **Onay** sayfasında hesaplanırken otomatik olarak dikkate alınır.

#### <a name="registered-breaks"></a>Kayıtlı molalar

Bir şirket planlı molaları kullanmıyorsa, çalışanlar iş günü boyunca molaları kaydedebilir. Kayıtlı molalar örneğin, bir çalışanın tanımlanmış giriş ve çıkış saatleri olmayan bir esnek zaman profiline karşı çalışması durumunda kullanılabilir. Kayıtlı molalar dolaylı faaliyet türündedir. Çalışan molayı **İş kartı** terminal sayfasına veya **İş kartı** cihaz sayfasına kaydeder. Her iki sayfada da kullanıcı önceden tanımlanmış mola faaliyetleri listesinden mola türünü seçebilir.

#### <a name="paid-and-unpaid-breaks"></a>Ücretli ve ücretsiz molalar

Mola faaliyetleri **Ücretli** veya **Ücretsiz** olarak ayarlanabilir. Ücretli mola ödenen saat hesaplamasına eklenir ve sistem **Mola** kayıt türüne ilişkin ödeme sözleşmesine tanımlanan ödeme türünü kullanır.

### <a name="example-of-a-planned-break"></a>Planlı mola örneği

Öğle yemeği için ücretsiz mola içeren aşağıdaki zaman profilini göz önünde bulundurun.

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 12:00 | Pazartesi  |
| Mola         | 12:00 | 12:30 | Pazartesi  |
| Standart zaman | 12:30 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

Çalışanın günlük kayıtları aşağıdaki gibidir.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 06:30 | 06:30 |
| Üretim işi            | 06:30 | 14:45 |
| Çıkış saati                 | 17:00 | 17:00 |

Günlük kayıtlarını hesapladıktan sonra **Onay** sayfasındaki **Saatler** sekmesinde hesaplama sonucunu görebilirsiniz. Bu senaryoyu anlamak için aşağıdaki alanlara bakın.

| Esnek + | Esnek - | Saat  | Ödeme zamanı | Ücretsiz mola süresi | Fazla mesai ödemesi |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1,50         |

> [!NOTE] 
> Sistem 0,5 saatlik ücretsiz mola süresi hesapladı ve bu süre ödenen saatin bir parçası değil.

### <a name="example-of-a-registered-break"></a>Kayıtlı mola örneği

Öğle yemeği için planlı mola içermeyen aşağıdaki zaman profilini göz önünde bulundurun.

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

Çalışanın günlük kayıtları aşağıdaki gibidir.

| Günlük kaydı türü | Başlat    | Bitir      |
|---------------------------|----------|----------|
| Giriş saati                  | 06:30 | 06:30 |
| Üretim işi            | 06:30 | 17:00 |
| Mola                     | 12:03 | 12:32 |
| Çıkış saati                 | 17:00 | 17:00 |

Kayıtlar hesaplanırken, faaliyetler için süre hesaplanır.

| Günlük kaydı türü | Başlat    | Bitir      | Saat  |
|---------------------------|----------|----------|-------|
| Giriş saati                  | 06:30 | 06:30 |       |
| Üretim işi            | 06:30 | 17:00 | 10,00 |
| Mola                     | 12:03 | 12:32 | 0,50  |
| Çıkış saati                 | 17:00 | 17:00 |       |

> [!NOTE]
> Mola zamanı faaliyet zamanıyla paralel olarak çalışır (örneğin bir üretim işi). Bu davranış her zaman mola faaliyetleri için kullanılır. Kayıtlar hesaplanırken, mola zamanı faaliyet zamanından çıkarılır. Bu durumda, üretim işinin süresi 10,50 saattir ancak zaman 10 olarak hesaplanır çünkü 0,5 saatlik mola zamanı faaliyet zamanından çıkarılır.

Günlük kayıtlarını hesapladıktan sonra **Onay** sayfasındaki **Saatler** sekmesinde hesaplama sonucunu görebilirsiniz. Bu senaryoyu anlamak için aşağıdaki alanlara bakın.

| Esnek + | Esnek - | Saat  | Ödeme zamanı | Ücretsiz mola süresi | Fazla mesai ödemesi |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1,50         |

Planlanan mola ücretsiz yerine ücretli olursa, hesaplama sonucu aşağıdaki gibi görünür.

| Esnek + | Esnek - | Saat  | Ödeme zamanı | Ücretli mola süresi | Fazla mesai ödemesi |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 0,5             | 1,50         |

### <a name="pay-items-and-paid-breaks"></a>Ödeme maddeleri ve ücretli molalar

**Onay** sayfasında kayıtları aktardığınızda, ödeme maddeleri oluşturulur. Ücretli molalar için ayrı bir ödeme maddesi oluşturulur.

Bir ücretli molanın ödeme oranı molaya ilişkin ödeme sözleşmelerinde ayarlanan ödeme türüne göre belirlenir. Bir ödeme türü kullanmak yerine, belirli bir tarih aralığı için molada saat başına maliyet fiyatı ayarlayabilirsiniz.

Aşağıdaki zaman profilini dikkate alın.

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

Çalışanın günlük kayıtları aşağıdaki gibidir.

| Günlük kaydı türü | Başlat    | Bitir      | Saat |
|---------------------------|----------|----------|------|
| Giriş saati                  | 07:00 | 07:00 |      |
| Üretim işi            | 07:00 | 15:00 | 7,5  |
| Mola (Ücretli)              | 12:00 | 12:30 | 0,5  |
| Çıkış saati                 | 15:00 | 15:00 |      |

Bu örnekte, standart zaman için ödeme türü **1201** olarak ayarlanmıştır ve ödeme sözleşmesinde ayarlanan ödeme oranı **10**'dur. Ücretli molanın ödeme türü **1301** ve ödeme oranı **8**'dir. Kayıtlar aktarıldığında aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 7,50      | 10   |
| Esnek-         | 1201     | 0,50      | 10   |
| Mola (Ücretli)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Ücretli molaların maliyetini projelere ve üretim emirlerine tahsis etme

Proje faaliyetlerindeki ve üretim işlerindei saatlik maliyet, Saat ve işe devamda hesaplanan ödeme oranları veya faaliyetler için tanımlanan maliyet kategorileri tarafından belirlenecek şekilde ayarlanabilir.

Maliyet kategorisini ayarlamak için **Üretim denetimi** &gt; **Kurulum** &gt; **Üretim yürütme** &gt; **Üretim emri varsayılanları**'nı seçin ve **Maliyet kategorisi** alanını **Evet** veya **Hayır** olarak ayarlayın.

- **Hayır** – Maliyet Saat ve işe devam kayıt türleri için tanımlanan ödeme oranlarını temel alınarak hesaplanır.
- **Evet** – Maliyet üretim ve proje faaliyetlerine ilişkin maliyet kategorileri temel alınarak hesaplanır.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Saat ve işe devamda hesaplanan ödeme oranlarını temel alan maliyet hesaplaması

Aşağıdaki örnek, maliyet ödeme oranlarını temel alarak hesaplanaca şekilde ayarlandığında saatli maliyetin nasıl hesaplandığını gösterir.

Üretim emirleri ve projeler için kullanılan saatlik maliyet oranı aktarım süreci sırasında hesaplanır. Faaliyet başına saatlik ücreti görmek için Saat ve işe devamda **Onayla** sayfanını açın ve **Sorgula** &gt; **Aktarılan kayıtlar**'ı seçin. Her kayıt için saatlik maliyet oranını **Maliyet fiyatları** sekmesinde bulabilirsiniz.

Önceki örnekle aynı zaman profilini kullanan aşağıdaki kayıtları göz önünde bulundurun.

| Günlük kaydı türü | Başlat    | Bitir      | Saat |
|---------------------------|----------|----------|------|
| Giriş saati                  | 07:00 | 07:00 |      |
| İşlem (Sipariş: 4711)     | 07:00 | 11:00 | 4    |
| İşlem (Sipariş: 4712)     | 11:00 | 15:00 | 3,50 |
| Mola (Ücretli)              | 12:00 | 12:30 | 0,50 |
| Çıkış saati                 | 15:00 | 15:00 |      |

Kayıtlar aktarıldıktan sonra aşağıdaki aktarılan kayıtlar oluşturulur.

| Kayıt türü     | Saat | Saatlik maliyet fiyatı |
|-----------------------|------|---------------------|
| Giriş saati              | 0,00 | 0,00                |
| İşlem (Sipariş: 4711) | 4,00 | 10,00               |
| İşlem (Sipariş: 4712) | 3,50 | 11,14               |
| Mola (Ücretli)          | 0,50 | 0,00                |
| Çıkış saati             | 0,00 | 0,00                |

Ücretli mola için saat başına maliyet fiyatı hesaplaması doğrudan bordro maliyetleri ayarına bağlıdır. **Saat ve işe devam** &gt; **Kurulum** &gt; **Saat ve işe devam parametreleri**'ni seçin. **Doğrudan bordro maliyetleri** altındaki **Maliyet fiyatı** sekmesinde bulunan **Standart zaman** alanında **Evet**, **Hayır** veya **Tahsisat**'ı seçebilirsiniz.

- **Evet** – Bu değer önceki örnek için kullanılır. Maliyet, ücretli mola faaliyetiyle paralel çalışan üretim veya proje faaliyetine tahsis edilir. Örnekte, bu faaliyet sipariş 4712 için üretim işidir. Gördüğünüz gibi, ücretli mola için saat başına maliyet fiyatı 0'dır (sıfır) ve molayla paralel çalışan işe tahsis edilmiştir.

    Ücretli mola süresi 0,5 saat ve ödeme oranı 8'dir. Bu nedenle, ücretli mola toplam maliyeti 4'tür. Toplam maliyet 3,5 saatlik işleme işine tahsis edilir. Bu nedenle, ücretli mola maliyete saat başına 1,14 (4 ÷ 3.5 = 1,14) katkıda bulunur.

- **Tahsisat** – Ücretli mola gün için kaydedilen işlere eşit olarak dağıtılır. Bu değer önceki örnek için kullanılırsa, aşağıdaki aktarılan kayıtlar oluşturulur.

    | Kayıt türü     | Saat | Saatlik maliyet fiyatı |
    |-----------------------|------|---------------------|
    | Giriş saati              | 0,00 | 0,00                |
    | İşlem (Sipariş: 4711) | 4,00 | 10,53               |
    | İşlem (Sipariş: 4712) | 3,50 | 10,53               |
    | Mola (Ücretli)          | 0,50 | 0,00                |
    | Çıkış saati             | 0,00 | 0,00                |

    İki üretim işi için toplam işlem süresi 7,5 saattir ve ücretli molanın toplam maliyeti 4'tür. Bu nedenle, mola maliyeti 0,53 (4 ÷ 7,5 =) olarak hesaplanır.

- **Hayır** - Ücretli mola maliyeti işleme faaliyetlerinin saatlik maliyetini artırmaz.

    | Kayıt türü     | Saat | Saatlik maliyet fiyatı |
    |-----------------------|------|---------------------|
    | Giriş saati              | 0,00 | 0,00                |
    | İşlem (Sipariş: 4711) | 4,00 | 10,00               |
    | İşlem (Sipariş: 4712) | 3,50 | 10,00               |
    | Mola (Ücretli)          | 0,50 | 0,00                |
    | Çıkış saati             | 0,00 | 0,00                |

## <a name="absence"></a>Devamsızlık

Çalışanın devamsızlık dönemini kaydetmek için bir devamsızlık kodu kullanılır. Molalar ve geçiş kodları gibi, devamsızlık kodu da dolaylı faaliyet türündedir. Devamsızlık süresi planlı veya kayıtlı olabilir ve devamsızlık geçerli veya geçersiz olabilir. Geçerli devamsızlık örnekleri doktor randevusu, seminer veya jüri görevini içerir. Geçersiz devamsızlık, bir çalışanın işe geç kalması gibi iyi bir nedeni bulunmayan devamsızlıktır. Genellikle, geçerli devamsızlık çalışana yapılan ödemeden kesintiye neden olmazken geçersiz devamsızlık kesintiye yol açar.

### <a name="planned-absence"></a>Planlanan devamsızlık

Çalışanlar için **Planlı devamsızlık oluştur** sayfasından planlı devamsızlık oluşturabilirsiniz (**Saat ve işe devam** &gt; **Planlı devamsızlık oluştur**). Burada, planlı devamsızlık belirli bir tarih ve zaman aralığı için bir devamsızlık işi olarak kaydedilir.

İş bir sorguyu temel alır. Bu nedenle, aynı hesaplama grubuna ait çalışanlar gibi birden çok çalışan için planlı izin oluşturabilirsiniz. Planlı devamsızlık tek bir çalışan için ise, kayıt **İşe devam** sayfasından veya **Zaman kaydı çalışanlar** sayfasından girilebilir.

- **İşe devam** sayfasından devamsızlık girmek için **Saat ve işe devam** &gt; **Sorgular ve raporlar** &gt; **İşe devam** &gt; **İşe devam** ve ardından **Devamsızlık kaydı**'nı seçin.
- *<strong><em>Zaman kaydı çalışanlar</em></strong>* sayfasından bir devamsızlık kaydı girmek için <strong>Saat ve işe devam</strong> &gt; <strong>Kurulum</strong> &gt; <strong>Zaman kaydı çalışanlar</strong>'ı ve daha sonra <strong>Zaman</strong> sekmesinde <strong>Zaman atama</strong> altından <strong>Devamsızlık kayıtları</strong>'nı seçin.

Çalışanlar için planlı devamsızlıkların özetini görmek için **Planlı devamsızlıklar** raporunu kullanabilirsiniz. Bu raporu açmak için **Saat ve işe devam** &gt; **Sorgular ve raporlar** &gt; **Devamsızlık raporları** &gt; **Planlı devamsızlıklar**'ı seçin.

### <a name="registered-absence"></a>Kayıtlı devamsızlık

Genel olarak, çalışanlar planlanan giriş ve çıkış saatleri arasında işte olmadıklarında devamsız olarak kabul edilir. Çalışanlar planlanan süreden sonra giriş yaparsa veya planlanandan erken çıkış yaparsa, devamsızlığın nedenini belirtmek için bir devamsızlık kodu seçmeleri istenir. Devamsızlık kodu kayda uygulanabilir olacak şekilde ayarlanabilir. Yalnızca geçerli kodları seçim listesinde kullanılabilir olur.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>İş saati kayıtlarının çeşitli kombinasyonlarını temel alan senaryolar

Aşağıdaki senaryolar, kayıtları temel alınarak çalışanlar için oluşturulan onaylanacak girişleri ve ödeme maddelerini gösterir. Tüm senaryolar aşağıdaki zaman profiline dayanırlar:

| Profil türü  | Başlat    | Bitir      | Gün     |
|---------------|----------|----------|---------|
| Fazla mesai     | 00:00 | 06:00 | Pazartesi  |
| Esnek+         | 06:00 | 07:00 | Pazartesi  |
| Giriş saati      | 07:00 | 07:00 | Pazartesi  |
| Standart zaman | 07:00 | 14:30 | Pazartesi  |
| Esnek-         | 14:30 | 15:30 | Pazartesi  |
| Çıkış saati     | 15:30 | 15:30 | Pazartesi  |
| Fazla mesai     | 15:30 | 06:00 | Salı |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Senaryo 1: Çalışan planlandan geç giriş yapar

Çalışan saat 08:30'da giriş yapar. Planlanan giriş saati 07:00 olduğundan işe 1,50 saat geç kalmıştır. 1,50 saat devamsızlık süresi olarak değerlendirildiğinden çalışandan bir devamsızlık kodu seçmesi istenir. Çalışan planlanan çıkış saat olan 15:30'da işten ayrılır. Çalışanın kayıtları hesaplanıp onaylandığında, çalışanın giriş yaparen seçtiği devamsızlık koduyla birlikte devamsızlık kaydı 07:00 ile 08:30 arasındaki süre için görüntülenir.

Zaman profilinde, **Giriş saati** kayıt türünü çalışanlar işe geç kaldığında bir tolerans olacak şekilde ayarlayabilirsiniz. Örneğin 5 seviyesinde bir tolerans ayarlarsanız, çalışandan yalnızca 07:05'den sonra giriş yapması durumuna bir devamsızlık kodu istenir.

Bu durumda, çalışanın işe geç kalmış olmak için iyi bir nedeni bulunmadığından, geçersiz devamsızlık için tanımlanan bir devamsızlık kodu seçer. Bir devamsızlık kodu, fazla mesai kesintisi ayarının devamsızlık kodunun ait olduğu devamsızlık grubu için etkinleştirilmiş olması durumunda geçersiz devamsızlığa uygun olarak kabul edilir. Ayarı ayarlamak için **Saat ve işe devam** &gt; **Kurulum** &gt; **Gruplar** &gt; **Devamsızlık grupları**'nı ve ardından **Fazla mesaiyi düş** onay kutusunu seçin.

Hesaplamadan sonra **Onay** sayfasında güne ilişkin çalışan kayıtları şu şekilde görünür.

| Günlük kaydı türü         | Başlat    | Bitir      | Saat |
|-----------------------------------|----------|----------|------|
| Devamsızlık (geçersiz - işe gecikme) | 07:00 | 08:30 | 1.5  |
| Giriş saati                          | 08:30 | 08:30 |      |
| Üretim işi                    | 07:30 | 15:30 | 7.0  |
| Çıkış saati                         | 15:30 | 15:30 |      |

Kayıtlar aktarıldıktan sonra ortaya çıkan ödeme maddesi şu şekildedir.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 7.00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Senaryo 2: Çalışan standart saat dönemi sırasında planlanan çıkış saatinden önce çıkış yapar.

Çalışan saat 07:00'de giriş yapar ve saat 13:00'da erken çıkış yapar. 13:00 planlı çıkış saati olan 15:30'dan önce olduğu ve 01:00 standart saat döneminde bulunduğu için çalışandan bir devamsızlık kodu seçmesi istenir. Çalışan geçerli devamsızlık olarak tanımlanan doktor randevusu için devamsızlık kodu seçer. Geçerli devamsızlık için ödeme oranı **Devamsızlık** kayıt türü ödeme sözleşmelerinde tanımlanır (**Saat ve işe devam** &gt; **Kurulum** &gt; **Bordro** &gt; **Ödeme sözleşmeleri**).

Hesaplamadan sonra **Onay** sayfasında güne ilişkin çalışan kayıtları şu şekilde görünür.

| Günlük kaydı türü              | Başlat    | Bitir      | Saat |
|----------------------------------------|----------|----------|------|
| Giriş saati                               | 07:00 | 07:00 |      |
| Üretim işi                         | 07:00 | 13:00 | 4,0  |
| Çıkış saati                              | 13:00 | 13:00 |      |
| Devamsızlık (geçerli – doktor randevusu) | 13:00 | 15:30 | 3.5  |

Kayıtlar aktarıldıktan sonra ortaya çıkan ödeme maddesi şu şekildedir.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Senaryo 3: Çalışan Esnek- dönemi sırasında planlanan çıkış saatinden önce çıkış yapar.

Çalışan 07:00'da giriş yapar ve planlanan Esnek- döneminde bulunan 14:15'te çıkış yapar. Gerçek çıkış zamanı ile planlı çıkış saati arasındaki süre devamsızlık olarak değerlendirilmez ve çalışandan bir devamsızlık kodu girmesi istenmez. Tutar çalışanın esnek hesabından düşülür ve çalışana Esnek- döneminin kalan bölümü süresince (14:15 ile 15:30 arası) ödeme yapılır.

Hesaplamadan sonra **Onay** sayfasında güne ilişkin çalışan kayıtları şu şekilde görünür.

| Günlük kaydı türü | Başlat    | Bitir      | Saat |
|---------------------------|----------|----------|------|
| Giriş saati                  | 07:00 | 07:00 |      |
| Üretim işi            | 07:00 | 14:15 | 7,25 |
| Çıkış saati                 | 14:15 | 14:15 |      |

Kayıtlar aktarıldıktan sonra ortaya çıkan ödeme maddesi şu şekildedir.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Senaryo 4: Çalışan geç giriş yapar ve fazla mesai dönemi sırasında planlanan çıkış saatinden sonra çıkış yapar.

Çalışan 09:30'da geç giriş yapar ve işe geç geldiği bu süreyi telafi etmek için fazla mesai yaparak 17:00'de işten çıkar. Çalışan işe geç geldiği ve daha uzun süre çalışarak bu süreyi telafi ettiği için şirket, bu süre zaman profilinde fazla mesai olarak görünmesine karşın, çalışana planlanan çıkış saati olan 15:30 ile gerçek çıkış saati olan 17:00 arasındaki çalışma için ödeme yapmak istemez.

Bu senaryoyu işlemek için, devamsızlık kodu, çalışanın aynı gün içinde yaptığı geçersiz devamsızlık saatlerinden fazla mesai saatlerini düşürmek amacıyla ayarlanabilir. Fazla mesaiyi geçersiz devamsızlık saatlerinden düşürmek için **Saat ve işe devam** &gt; **Kurulum** &gt; **Gruplar** &gt; **Devamsızlık grupları**'nı ve ardından **Fazla mesaiyi düş** onay kutusunu seçin.

Hesaplamadan sonra **Onay** sayfasında güne ilişkin çalışan kayıtları şu şekilde görünür.

| Günlük kaydı türü         | Başlat    | Bitir      | Saat |
|-----------------------------------|----------|----------|------|
| Devamsızlık (geçersiz - işe gecikme) | 07:00 | 09:30 | 1.5  |
| Giriş saati                          | 09:30 | 09:30 |      |
| Üretim işi                    | 09:30 | 17:00 | 7,5  |
| Çıkış saati                         | 17:30 | 17:30 |      |

**Fazla mesaiyi düş** onay kutusu seçili devamsızlık kodu için seçilirse, fazla mesai ödemesi çalışanın geçersiz olarak devamsızlık yaptığı saat kadar düşürülür. Bu durumda, kayıtlar aktarıldıktan sonra aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 9,00      | 10   |
| Fazla mesai      | 1301     | 0,5       | 15   |

Burada, 07:00 ile 09:30 arasındaki 1,5 saatlik geçersiz devamsızlık, 15:30 ile 17:30 arasındaki 2,0 saatlik fazla mesaiden düşülür. Kaydın sonucu 1,5 saat standart saat ve 0,5 saat fazla mesai olur.

Bunun tersine, **Fazla mesaiyi düş** onay kutusu seçili devamsızlık kodu için işaretlenmediğinde, geç kalmış ve geçersiz bir devamsızlık yapmış olmasına karşın fazla mesai çalışana ödenir. Bu durumda, kayıtlar aktarıldıktan sonra aşağıdaki ödeme maddeleri oluşturulur.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 7,50      | 10   |
| Fazla mesai      | 1301     | 2,0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Senaryo 5: Çalışan planlanan çıkış saatinden önce çıkış yapar ve devamsızlık dönemini Esnek- dönemine dönüştürebilir

Aşağıdaki örnek, bir çalışanın esnek hesabının devamsızlık dönemi Esnek- dönemine dönüştürülerek nasıl düşürülebileceğini gösterir.

Çalışan saat 07:00'de giriş ve saat 13:00'da çıkış yapar. Bu saatleri esnek hesabından düşmesi durumunda hafta sonu için eve gidebileceği konusunda yöneticisiyle bir anlaşmaya varmıştır. İlgili iş gününün kalan kısmı için devamsızlık dönemi çalışan planlı Esnek- döneminde olmadığından çalışan 13:00'da çıkış yaptığında bir devamsızlık kodu seçmesi istenir. İş gününün kalan kısmını Esnek- dönemine çevirmek için çalışan esnek hesabından düşülmek üzere ayarlanmış bir devamsızlık kodu seçebilir.

Bir iş gününde devamsızlık kaydeden çalışanlar için esnek saatlerin bakiyesini azaltmak üzere **Saat ve işe devam** &gt; **Kurulum** &gt; **Gruplar** &gt; **Devamsızlık grupları**'nı ve **Esnek azalt** onay kutusunu seçin.

Hesaplamadan önce **Onay** sayfasında güne ilişkin çalışan kayıtları şu şekilde görünür.

| Günlük kaydı türü | Başlat    | Bitir      | Saat |
|---------------------------|----------|----------|------|
| Giriş saati                  | 07:00 | 07:00 |      |
| Üretim işi            | 07:00 | 13:00 | 6,0  |
| Çıkış saati                 | 13:00 | 13:00 |      |

Çalışan geçersiz bir devamsızlık için devamsızlık kodu seçerse, kayıt aktarıldıktan sonra ortaya çıkan ödeme maddesi aşağıdaki gibi görünür.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 6,00      | 10   |

Çalışan geçerli devamsızlık için devamsızlık kodu seçerse ve devamsızlık kodu esnek hesabından düşülmek üzere ayarlanırsa, kayıtlar aktarıldıktan sonra elde edilen ödeme maddeleri aşağıdaki gibi görünür.

| Ücret türü     | Ödeme türü | Ödeme birimleri | Ücret |
|---------------|----------|-----------|------|
| Standart zaman | 1201     | 8,50      | 10   |

Bu durumda, çalışanın esnek bakiyesi gerçek çıkış saati ile planlanan çıkış saati arasındaki saat kadar azaltılır (bu da 13:00 ile 15:30 arasındaki 2,5 saattir).

> [!NOTE]
> Bir devamsızlık kodu için hem **Esnek azalt** onay kutusunu hem de **Fazla mesaiyi düş** onay kutusunu seçmenizi önermeyiz çünkü ayar geçersiz saatleri çalışanın fazla mesai saatlerinden düşer ve aynı zamanda çalışanın esnek hesabından da azaltma yapar.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Senaryo 6: Gün için planlı devamsızlık ve çalışan işe devamı yoktur

Çalışan bir iş gününde işe gelmezse ve söz konusu günde çalışan için planlı bir devamsızlık yoksa, çalışanın kayıtlarının hesaplanması için varsayılan devamsızlık kodu kullanılır. Varsayılan devamsızlık kodlarını tanımlamak için **Saat ve işe devam** &gt; **Saat ve işe devam parametreleri**'ni seçin. Daha sonra aşağıdaki alanlardan bir devamsızlık kodu seçebilirsiniz:

- Otomatik Esnek- ekleme
- Devamsızlığı otomatik ekle

Esnek saatler için etkinleştirilen bir çalışan için günlük kayıtlar hesaplanırken, **Otomatik esnek- ekleme** alanında belirtilen devamsızlık kodu varsayılan devamsızlık kodu olarak kullanılır. Çalışanın esnek saatler için etkinleştirilmemişse, **Otomatik devamsızlık ekleme** alanında belirtilen devamsızlık kodu kullanılır. Bir şirkette hem esnek saatler için etkinleştirilmiş hem de esnek saatler için etkinleştirilmemiş çalışanlar varsa, her iki parametrenin de ayarlanması gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]