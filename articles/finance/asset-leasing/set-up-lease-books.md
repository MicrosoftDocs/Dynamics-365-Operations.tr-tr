---
title: Kiralama defterlerini ayarlama
description: Bu konuda, kiralama defterlerinde saklanan bilgiler açıklanmaktadır. Kiralama defterleri sistemde kiralamanın nasıl hesaplandığını belirleyen muhasebe ilkelerini içerir.
author: moaamer
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ba442b3085593221e2182b848e6879a96bbca127
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727103"
---
# <a name="set-up-lease-books"></a>Kiralama defterlerini ayarlama

[!include [banner](../includes/banner.md)]

Kiralama defterleri sistemde kiralamanın nasıl hesaplandığını belirleyen muhasebe ilkelerini içerir. Nakit bazlı muhasebeye ek olarak Varlık kiralama aşağıdaki standartları destekler:

- ABD'deki Genel Kabul Görmüş Muhasebe İlkeleri (ABD GAAP)
- Muhasabe Standartları Kodlaması Konu 842 (ACS 842)
- ASC 840
- Uluslararası Mali Raporlama Standardı 16 (IFRS 16)
- Uluslararası Muhasebe Standardı 17 (IAS 17)

Yeni bir kiralama defteri oluşturmak için şu adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Kiralama defterleri**'ne gidin.
2. Defter eklemek için **Yeni**'yi seçin.
3. Aşağıdaki alanları ayarlayın.

    | Kuruluş adı                                     | Tanım |
    |------------------------------------------|-------------|
    | Deftere nakil katmanı                            | Kullanılacak deftere nakil katmanını seçin. Bir kiralamaya eklenen her defter, belirli bir nakil katmanı için ayarlanır. Her deftere nakil katmanı farklı bir deftere nakil amacına sahiptir. |
    | Kiralama türü                               | Kiralamanın otomatik olarak mı sınıflandırılacağını yoksa finansal kiralama veya işletme kiralaması olarak önceden tanımlanmış mı olacağını seçin. |
    | Muhasebe altyapısı                     | Defterle ilişkili çerçeveyi seçin. |
    | Kiralama süresi/Faydalı ömür Ayarlama          | Kiralama **Otomatik** olarak ayarlanmışsa ve varlığın faydalı ömrü üzerinden kiralama süresi bu alana girilen yüzdeye eşit veya bundan fazlaysa, sistem kiralamayı finansal olarak sınıflandıracaktır.  |
    | Bugünkü değer/Varlık adil değeri ayarı   | Kiralama türünü belirleyecek eşiği tanımlamak için bir tamsayı girin. Gelecekteki minimum kira ödemelerinin bugünkü değeri, defter kurulumundaki kullanıcı tanımlı değerden daha fazla ise ve defterin kiralama sınıflandırması otomatik olarak ayarlanmışsa sistem kiralamayı finansal kiralama olarak sınıflandırır. |
    | Kısa süre eşiği                     | Kısa süreli kiralamalar için bir eşik olarak kullanılacak ay sayısını girin. Kiralama süresi buraya girdiğiniz ay sayısından azsa veya bu sayıya eşitse sistem, kiralamayı kısa süreli kiralama olarak sınıflandıracaktır ve ertelenmiş kira işlemi uygulanacaktır. |
    | Düşük değer eşiği                      | Düşük değerli kiralamalar için eşik olarak kullanılacak bir tutar girin. Varlığın adil değeri buraya girdiğiniz değerden azsa veya bu değere eşitse sistem, kiralamayı düşük değerli kiralama olarak sınıflandıracaktır ve ertelenmiş kira işlemi uygulanacaktır. |
    | Satıcıya öde                            | Kiralama ödemelerinin, her kiralamada belirtilen satıcı hesabına fatura olarak nakledilmesine izin vermek için bu seçeneği **Evet** olarak ayarlayın. Kiralama ödemesi deftere nakledildiğinde satıcı hesabı alacaklandırılır. Bu seçenek **Hayır** olarak ayarlanırsa, bunun yerine **Kiralama deftere nakil parametreleri** sayfasındaki **Kira ödemesi** deftere nakil türü için beliritilen hesap alacaklandırılacaktır. |
    | Kiralama kuralı                       | Kiralamanın başlangıç tarihi kuralını seçin:<ul><li><b>Yok</b>: Kiralamanın başlangıç tarihini başlatma tarihi olarak kullanın.</li><li><b>Tam ay</b>: Kiralama başlangıç tarihinin, başlatma tarihi olarak bulunduğu ayın ilk gününü kullanın.</li></ul><p><b>Hiçbiri</b>'ni seçerseniz, pasif amostismanı ve varlık amortismanı zamanlamalarının, ay sonu yerine ayın ortasında tahakkuk edilmesi ve deftere nakil edilmesi riski vardır. <b>Tam ay</b> seçildiğinde, sistemin ayın ilk gününde kiralama muhasebesine başlayacak şekilde başlaması ve tüm ayın giderinin tahakkuk edip ayın son gününde deftere naklediğildiğinden emin olun.</p><p><strong>Not:</strong> Kiralama kuralları özelliği, Özellik yönetimi aracılığıyla açılmalıdır. <b>Özellik yönetimi</b> çalışma alanında, <b>Varlık kiralama için kiralama kuralı</b> özelliği olarak adlandırılan özelliği bulup seçin ve <b>Şimdi etkinleştir</b>'i seçin.</p> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
