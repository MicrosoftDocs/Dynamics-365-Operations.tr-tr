---
title: Kiralama defterlerini ayarlama
description: Bu konuda, kiralama defterlerinde saklanan bilgiler açıklanmaktadır. Kiralama defterleri sistemde kiralamanın nasıl hesaplandığını belirleyen muhasebe ilkelerini içerir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449012"
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
