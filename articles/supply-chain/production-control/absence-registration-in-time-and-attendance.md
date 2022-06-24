---
title: Saat ve işe devamda devamsızlık kaydı
description: Bu makale, Saat ve işe devamda devamsızlık kayıtlarının nasıl ele alınacağını açıklar.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a613edbe42d1bfb1d2ee43ee1cb2f1e0ab49a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890784"
---
# <a name="absence-registration-in-time-and-attendance"></a>Saat ve işe devamda devamsızlık kaydı

[!include [banner](../includes/banner.md)]

Bu makale devamsızlık kavramlarını tanımlar ve devamsızlığın Saat ve işe devamda nasıl ele alınacağını açıklar.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Normal çalışma saatlerine dayalı devamsızlık

Çalışanlar, normal çalışma saatleri içinde çalışmadıkları saatlerde yok sayılır. Normal çalışma saatleri bir çalışanın standart zaman profilinde tanımlanır.

Örneğin, bir çalışan girişin saat 07:00'de çıkışın saat 15:00'te olduğu bir gün profilinde çalışmaktadır. Çalışan 09:00'da giriş yaparsa, kendisi o gün saat 07:00 ile 09:00 arasında yok kabul edilir.

Bu durumda, çalışanlardan devamsızlık için bir neden girmesi istenir. Bir devamsızlık kodu seçerek bir neden belirtebilirsiniz.

## <a name="absence-codes"></a>Devamsızlık kodları

Devamsızlık kodları çeşitli devamsızlık türlerini tanımlar. Devamsızlık kodları şirket tarafından tanımlanır.

Devamsızlık kodlarına çeşitli kurallar uygulanabilir. Örneğin, bir devamsızlık kodu kesinti veya ödeme yapmak üzere yapılandırılabilir.

Örneğin, bir şirket çalışanlar geç geliyorsa ve iyi bir nedenleri yoksa bir **Geç** devamsızlık kodu tanımlar. Şirket ayrıca çalışanların dahili kurslara katılmak üzere harcadıkları zaman için kullanılan bir **Dahili kurs** devamsızlık kodu tanımlar. Bu devamsızlık kodları **Geç** bir çalışanın ödemesinden kesinti yapılacak ancak **Dahili kurs** bir çalışanın ödemesinden kesinti yapılmayacak şekilde ayarlanabilir.

Otomatik devamsızlık kodları ayarlayabilirsiniz. Bu devamsızlık kodları devamsızlık kaydı olmadığında bir çalışanın süresini hesaplamak için kullanılabilir. Çalışanın zaman profili, devamsızlık kodunun standart zaman veya esnek zaman için kullanılıp kullanılmadığını belirler.

### <a name="set-up-standard-time-and-flex-time"></a>Standart zaman ve esnek zaman ayarla

- **Zaman ve katılımcı parametreleri** sayfasındaki **Otomatik devamsızlık ekleme** ve **Otomatik Esnek ekleme-** seçeneklerini kullanarak standart zaman ve esnek zaman için parametreleri yapılandırın.

## <a name="absence-groups"></a>Devamsızlık grupları

Devamsızlık kodları, devamsızlık grupları olarak gruplandırılır. Devamsızlık gruplarını ortak özelliklere sahip devamsızlık kodlarını gruplandırmak için kullanırsınız. Örnekler arasında yasal devamsızlık veya doktor randevusu, jüri görevi veya çocuk hastalığı nedeniyle devamsızlık için devamsızlık kodları yer alır.

## <a name="planned-absence"></a>Planlanan devamsızlık

Bir çalışanın yaklaşmakta olan bir tatil nedeniyle belirli bir süre işe gelmeyeceğini biliyorsanız, planlanan devamsızlığı kullanabilirsiniz. Devamsızlık kodunu planlanan devamsızlığı dikkate alacak şekilde yapılandırarak planlanan devamsızlığı ayarlarsınız. Bir planlanan devamsızlık ayarladığınızda, kullanıcı zaman kayıtları hesaplandığında devamsızlık süresince bir devamsızlık kodu istenmez. Planlanan devamsızlık tek bir çalışan için tanımlanabilir veya çalışanlar için planlanan devamsızlığı toplu güncelleştirmek için bir toplu iş tanımlayabilirsiniz.

### <a name="set-up-planned-absence"></a>Planlanan devamsızlık ayarla

1. **İnsan kaynakları** &gt; **Çalışanlar** &gt; **Personel** seçin ve bir personel seçin.
2. **Zaman** &gt; **Zaman atamaları** &gt; **Zaman Devamsızlık kaydı** seçin ve planlanan devamsızlığı ayarlayın.

## <a name="interrupted-planned-absence"></a>Durdurulmuş planlanan devamsızlık

Bir planlanan devamsızlık ayarladığınızda **Durdur** seçeneğini uygularsanız, çalışan planlanan devamsızlık süresince işe gelirse planlanan devamsızlık durdurulur. Planlanan devamsızlık **Durduruldu** olarak işaretlenir ve gelecekteki hesaplamalar üzerinde hiçbir etkisi olmaz.

### <a name="set-up-a-planned-absence-for-interruption"></a>Durdurmak için bir planlanan devamsızlık ayarla

1. Planlanan devamsızlık ayarlama prosedüründe açıklandığı gibi **Zaman devamsızlık kaydı** sayfasını açın.
2. **Durdur** öğesini seçin.

**Durdur** seçeneği zaman mağaza katı terminali veya mağaza katı cihazı aracılığıyla kaydedildiğinde uygulanır. Kayıtlar hesaplama ve onay sayfalarına veya **Elektronik zaman kartı** sayfasına girilmişse, bu seçenek kullanılmaz.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Esnek profilde, devamsızlık kullanım örnekleri

Aşağıdaki üç örnekte esnek dönemleri olan bir profilde devamsızlığın nasıl hesaplandığı gösterilmektedir.

Örneklerde aşağıdaki profil kullanılır.

| Giriş saati | Standart zaman    | Mola             | Standart zaman | Esnek-        | Çıkış saati | Esnek+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 08:00     | 09:00 - 11:30 | 11:30 - 00:00 | 00:00 - 15:00 | 15:00 - 16:00 | 16:00      | 16:00 - 18:00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Örnek 1: Bir Esnek dönemde çıkış yapma

Çalışan saat 08:00'de giriş ve saat 15:30'da çıkış yapıyor. Bu durumda, çalışan Esnek bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesinden yarım saat kesilir.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Örnek 2: Standart zaman döneminde çıkış yapma

Çalışan saat 08:00'de giriş ve saat 14:30'da çıkış yapıyor. Bu durumda, çalışan Standart zaman döneminde çıkış yaptığından, devamsızlık 14:30 ile 16:00 saatleri arasında hesaplanır ve 1,5 saatlik bir devamsızlık dönemi kaydedilir. Bu döneme ait devamsızlık kodu gereklidir.

### <a name="example-3-signing-out-during-a-flex-period"></a>Örnek 3: Bir Esnek+ dönemde çıkış yapma

Çalışan saat 08:00'de giriş ve saat 16:30'da çıkış yapıyor. Bu durumda, çalışan Esnek+ bir dönemde çıkış yaptığından, devamsızlık hesaplanmaz ve çalışanın esnek bakiyesine yarım saat eklenir.

## <a name="absence-in-the-calculation-and-approval-process"></a>Hesaplama ve onay işleminde devamsızlık

Bordro sistemine ödeme maddeleri olarak aktarmadan önce çalışan zaman kayıtlarının hesaplanması ve onaylanması gerekir.

Bir onaylayan çalışanın zaman kayıtlarını değiştirebilir. Onaylayan çalışanın kaydolduğu bir devamsızlığı da değiştirebilir. Onaylayan el ile bir devamsızlık koduna sahip bir süre girerse, bu döneme ait devamsızlık kodu Zaman ve katılımcı parametrelerinden varsayılan devamsızlık kodu tarafından geçersiz kılınmaz.

Örneğin, bir çalışan 10:00'da giriş yapıyor ve geç geldiğini belirten bir devamsızlık kodunu seçiyor. Daha sonra çalışan yöneticisine saat 08:00 ile 10:00 arasında bir doktor randevusu olduğunu bildiriyor. Doktor randevusu çalışanın ödemesinden kesinti yapılmasına neden olmamalıdır. Bu nedenle, bu durumda, yönetici iki saat süreyle hastalığı belirten bir devamsızlık kodunu el ile girerek saat 08:00 ile 10:00 arasında iki saatlik devamsızlık ayarlayabilir.

### <a name="calculate-and-approve-absence"></a>Devamsızlığı hesapla ve onayla

- **İşe devam zamanı** &gt; **Gözden geçirme ve onaylama** &gt; **Onaylama veya Hesaplama** öğelerini seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]