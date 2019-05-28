---
title: Erişilebilirlik özellikleri
description: Bu konu, çeşitli engelleri bulunan kullanıcıların Dynamics 365 for Finance and Operations, Dynamics 365 for Retail ve Dynamics 365 for Talent kullanmalarına yardımcı olacak işlevleri açıklar.
author: TLeforMicrosoft
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: f88b485b0bdbf66532adff530e399bdd9d5b0ed5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565242"
---
# <a name="accessibility-features"></a>Erişilebilirlik özellikleri

[!include [banner](../includes/banner.md)]

Bu konu, çeşitli engelleri bulunan kullanıcıların Dynamics 365 for Finance and Operations, Dynamics 365 for Retail ve Dynamics 365 for Talent kullanmalarına yardımcı olacak işlevleri açıklar. Örneğin, Microsoft Windows Ekran Okuyucusu gibi yardımcı görme teknolojileri kullanan kişilere yönelik özellikler vardır.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Ekran Okuyucusu ve yalnızca klavye erişimi

Her alan ve denetimde bir etiket ve ilgili kısayola ilişkin bir açıklama vardır. Ekran okuyucu etiket ve açıklamayı okuyabilir.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>En sık gerçekleştirilen eylemler için kısayollar

Çoğu kullanıcı için, günlük sistem kullanımı çok sayıda veri girişi ve klavye etkileşimi içerir. Kullanıcı deneyimini geliştirmek için ekranda "atlama" yapmanıza yardımcı olacak kısayollar ve özel eylemler için kısayollar oluşturduk. Daha fazla bilgi için bkz. [Klavye kısayolları](shortcut-keys.md).

## <a name="navigation-search"></a>Gezinti araması

En soldaki bölme olan Gezinti bölmesi menüsünü kullanarak erişilen her sayfa **Arama** kutusundan da bulunabilir. **Arama** kutusuna gitmek için Alt+G tuşlarına basın ve sonra sayfa açıklamasını veya adı yazın.

![Arama kutusuna girilen "Banka hesapları"](media/6d08b0be32808221023e2aa92d69fd70.png "Arama kutusuna girilen \"banka hesapları\"")

Daha fazla bilgi için bkz. [Gezinti araması](navigation-search.md).

> [!NOTE]
> Doğrudan yalnızca üst düzey sayfalara gidebilirsiniz. İkincil sayfalar kendi ana sayfalarındaki bilgileri veya bağlamı kullanır.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Yalnızca klavye kullanıcıları ve baş aşağıda veri girişi için eylem arama

Bir sayfada yer alan her eyleme seklem sırası aracılığıyla klavyeden erişilebilir. Bu konunun ilerleyen bölümlerinde sekme sırası hakkında bilgi verilmektedir. Eylemleri daha doğrudan çalıştırmak için eylem arama işlevini kullanabilirsiniz.

### <a name="example"></a>Örnek

Eylem Bölmesindeki **Satış siparişi** sekmesinde yer alan **E-posta bildirimi** grubunda görüntülenen **E-posta bildirimi günlüğü** eylemini çalıştırmak istiyorsunuz.

![Eylem bölmesinde e-posta bildirimi günlük eylemi](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "Eylem bölmesinde e-posta bildirimi günlük eylemi")

Seçeneklerden biri klavyenizi kullanmaktır. Odağı Eylem Bölmesine taşımak için CTRL+F6 tuşuna basın ve **E-posta bildirimi günlüğü** üzerine gelene kadar Sekme tuşuna art arda basarak tük sekmelerin ve eylemlerin üzerinden geçin.

Ancak, eylemi daha doğrudan da çalıştırabilirsiniz. Sayfadaki herhangi bir konumdan Ctrl + Kesme işareti (') tuşuna basarak eylemleri arama kutusunu görüntüleyin.

![Eylemler için arama kutusu](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Eylemler için arama kutusu")

Arama kutusuna eylemi açıklayan sözcükleri yazın. Eylem kullanılabilir duruma gelir ve doğrudan çalıştırabilirsiniz. Örneğin **e-posta**, **bildir** (sözcüğün bir kısmı) veya **günlük** yazarak "E-posta bildirimi günlüğü" işlevine "atlayabilirsiniz".

![Arama kutusuna girilen "E-posta"](media/image4.png "Arama kutusuna girilen \"e-posta\"")

![Arama kutusuna girilen "Bildirim"](media/image5.png "Arama kutusuna girilen \"bildirim\"")

![Arama kutusuna girilen "Günlük"](media/image6.png "Arama kutusuna girilen \"günlük\"")

İşlemi tamamladığınız zaman Ctrl+Kesme işareti tuşuna yeniden basarak eylem aramasını çalıştırmadan önce çalıştığınız alana geri dönebilirsiniz.

Daha fazla bilgi için bkz. [Eylem araması](action-search.md).

## <a name="tab-sequence"></a>Sekme sırası

Sistem günlük kullanımında, genel görevleri gerçekleştirmek için her alan gerekli değildir. Bu nedenle, varsayılan olarak, sekme sırası "optimize edilmiştir." Sekme durakları tipik senaryolar için gerekli olan alanlara ayarlanmıştır.

Bununla birlikte, sık gerçekleştirdiğiniz görevleri yerine getirmek için bazı alanların varsayılan sekme sırasında olmadığını görebilirsiniz. Bu durumda, Windows Ekran Okuyucusu kullanıyorsanız, Windows Ekran okuyucusunun klavyesini kullanarak bu alanlara erişebilir ve içeriklerini denetleyebilirsiniz. Bunun yerine **Seçenekler** sayfasında **Gelişmiş sekme sırası** seçeneğini etkinleştirebilirsiniz. Bu seçenek, tüm düzenlenebilir ve salt okunur alanları sekme sırasının parçası yapar. Daha sonra özel bir sekme sırası oluşturmak için sayfa kişiselleştirmeyi kullanabilir ve sekme sırasının parçası olması gerekmeyen alanları dışarıda bırakabilirsiniz. Kişiselleştirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

!["Gelişmiş sekme sırası" seçeneği](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "\"Gelişmiş sekme sırası\" seçeneği")

## <a name="form-patterns"></a>Form modelleri

Üründeki sayların yaklaşık yüzde 90 küçük bir model kümesini temel alır. Bu modeller *form modelleri* olarak adlandırılır. Her bir form modeli, sayfada en sık gerçekleştirilen eylemleri sağlamak için kullanılır. Bir form modeli, alışkanlığı ve kolay anlaşılırlığı garanti eder, çünkü sık kullanılan eylemler ve veriler farklı sayfalarda daima aynı konumda gösterilir. Az sayıda form modeli olduğundan, sayfa sayısı ne olursa olsun, kullanıcılar sistemi kolaylıkla anlayabilir ve form modellerini tanıdıktan sonra sayfaları güvenli şekilde kullanabilir.

Form modelleri hakkında daha fazla bilgi için bkz. [Form stilleri ve modelleri](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Esnek düzen

Ürün, en küçük ekranlardan yüksek çözünürlüklü büyük ekranlara kadar çeşitli cihazlar ve form faktörlerinde çalışmak üzere tasarlanmıştır. Esnek düzen alt yapımız kullanıcıların yüzde 200 oranında yakınlaştırma yapmasına (bazı senaryolarda yüzde 200'den fazla) olanak tanır.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Geliştiricilere ve müşterilere yardımcı olmak için kılavuz özelleştirmelerinde erişilebilir düşünceyi içerir.

Microsoft'un erişilebilirlik sağlama konusundaki en iyi uygulamaları hakkında daha fazla bilgi edinmek için bkz. [Formlar, ürünler ve denetimlerde erişilebilirlik](../../dev-itpro/user-interface/enable-accessibility.md).
