---
title: Erişilebilirlik özellikleri
description: Bu konu, çeşitli engelleri bulunan kullanıcılara yardımcı olmak üzere tasarlanan işlevleri açıklar.
author: TLeforMicrosoft
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 4cf5a5fc2d40e66d189d281b343d1525edf7e8c5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744135"
---
# <a name="accessibility-features"></a>Erişilebilirlik özellikleri

[!include [banner](../includes/banner.md)]

Bu konu, çeşitli engelleri bulunan kullanıcıların bu uygulamayı kullanmalarına yardımcı olacak işlevleri açıklar. Örneğin, Microsoft Windows Ekran Okuyucusu gibi yardımcı görme teknolojileri kullanan kişilere yönelik özellikler vardır.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Ekran Okuyucusu ve yalnızca klavye erişimi

Her alan ve denetimde bir etiket ve ilgili kısayola ilişkin bir açıklama vardır. Ekran okuyucu etiket ve açıklamayı okuyabilir.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>En sık gerçekleştirilen eylemler için kısayollar

Çoğu kullanıcı için, günlük sistem kullanımı çok sayıda veri girişi ve klavye etkileşimi içerir. Kullanıcı deneyimini geliştirmek için ekranda "atlama" yapmanıza yardımcı olacak kısayollar ve özel eylemler için kısayollar oluşturduk. Daha fazla bilgi için bkz. [Klavye kısayolları](shortcut-keys.md).

## <a name="navigation-search"></a>Gezinti araması

En soldaki bölme olan Gezinti bölmesi menüsünü kullanarak erişilen her sayfa **Arama** kutusundan da bulunabilir. **Arama** kutusuna gitmek için Alt+G tuşlarına basın ve sonra sayfa açıklamasını veya adı yazın.

![Arama kutusuna "Banka hesapları" girildi](media/6d08b0be32808221023e2aa92d69fd70.png "Arama kutusuna &quot;Banka hesapları&quot; girildi")

Daha fazla bilgi için bkz. [Gezinti araması](navigation-search.md).

> [!NOTE]
> Doğrudan yalnızca üst düzey sayfalara gidebilirsiniz. İkincil sayfalar kendi ana sayfalarındaki bilgileri veya bağlamı kullanır.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Yalnızca klavye kullanıcıları ve baş aşağıda veri girişi için eylem arama

Bir sayfada yer alan her eyleme seklem sırası aracılığıyla klavyeden erişilebilir. Bu konunun ilerleyen bölümlerinde sekme sırası hakkında bilgi verilmektedir. Eylemleri daha doğrudan çalıştırmak için eylem arama işlevini kullanabilirsiniz.

### <a name="example"></a>Örnek

Eylem Bölmesindeki **Satış siparişi** sekmesinde yer alan **E-posta bildirimi** grubunda görüntülenen **E-posta bildirimi günlüğü** eylemini çalıştırmak istiyorsunuz.

![Eylem Bölmesindeki e-posta bildirim günlüğü eylemi](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg "Eylem Bölmesindeki &quot;e-posta bildirim günlüğü&quot; eylemi")

Seçeneklerden biri klavyenizi kullanmaktır. Odağı Eylem Bölmesine taşımak için CTRL+F6 tuşuna basın ve **E-posta bildirimi günlüğü** üzerine gelene kadar Sekme tuşuna art arda basarak tük sekmelerin ve eylemlerin üzerinden geçin.

Ancak, eylemi daha doğrudan da çalıştırabilirsiniz. Sayfadaki herhangi bir konumdan Ctrl + Kesme işareti (') tuşuna basarak eylemleri arama kutusunu görüntüleyin.

![Eylem arama kutusu](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg "Eylem arama kutusu")

Arama kutusuna eylemi açıklayan sözcükleri yazın. Eylem kullanılabilir duruma gelir ve doğrudan çalıştırabilirsiniz. Örneğin **e-posta**, **bildir** (sözcüğün bir kısmı) veya **günlük** yazarak "E-posta bildirimi günlüğü" işlevine "atlayabilirsiniz".

![Arama kutusuna "E-posta" girildi](media/image4.png "Arama kutusuna &quot;E-posta&quot; girildi")

![Arama kutusuna "Bildir" girildi](media/image5.png "Arama kutusuna &quot;Bildir&quot; girildi")

![Arama kutusuna "Günlük" girildi](media/image6.png "Arama kutusuna &quot;Günlük&quot; girildi")

İşlemi tamamladığınız zaman Ctrl+Kesme işareti tuşuna yeniden basarak eylem aramasını çalıştırmadan önce çalıştığınız alana geri dönebilirsiniz.

Daha fazla bilgi için bkz. [Eylem araması](action-search.md).

## <a name="tab-sequence"></a>Sekme sırası

Sistem günlük kullanımında, genel görevleri gerçekleştirmek için her alan gerekli değildir. Bu nedenle, varsayılan olarak, sekme sırası "optimize edilmiştir." Sekme durakları tipik senaryolar için gerekli olan alanlara ayarlanmıştır.

Bununla birlikte, sık gerçekleştirdiğiniz görevleri yerine getirmek için bazı alanların varsayılan sekme sırasında olmadığını görebilirsiniz. Bu durumda, Windows Ekran Okuyucusu kullanıyorsanız, Windows Ekran okuyucusunun klavyesini kullanarak bu alanlara erişebilir ve içeriklerini denetleyebilirsiniz. Bunun yerine **Seçenekler** sayfasında **Gelişmiş sekme sırası** seçeneğini etkinleştirebilirsiniz. Bu seçenek, tüm düzenlenebilir ve salt okunur alanları sekme sırasının parçası yapar. Daha sonra özel bir sekme sırası oluşturmak için sayfa kişiselleştirmeyi kullanabilir ve sekme sırasının parçası olması gerekmeyen alanları dışarıda bırakabilirsiniz. Kişiselleştirme hakkında daha fazla bilgi için bkz. [Kullanıcı deneyimini kişiselleştirme](personalize-user-experience.md).

!["Gelişmiş sekme sırası" seçeneği](media/8c0f12bbb3f26032997ef0ba95d89b6a.png "&quot;Gelişmiş sekme sırası&quot; seçeneği")

## <a name="form-patterns"></a>Form modelleri

Uygulamadaki sayfaların yaklaşık yüzde 90'ı küçük bir model kümesini temel alır. Bu modeller *form modelleri* olarak adlandırılır. Her bir form modeli, sayfada en sık gerçekleştirilen eylemleri sağlamak için kullanılır. Bir form modeli, alışkanlığı ve kolay anlaşılırlığı garanti eder, çünkü sık kullanılan eylemler ve veriler farklı sayfalarda daima aynı konumda gösterilir. Az sayıda form modeli olduğundan, sayfa sayısı ne olursa olsun, kullanıcılar sistemi kolaylıkla anlayabilir ve form modellerini tanıdıktan sonra sayfaları güvenli şekilde kullanabilir.

Form modelleri hakkında daha fazla bilgi için bkz. [Form stilleri ve modelleri](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Esnek düzen

Ürün, en küçük ekranlardan yüksek çözünürlüklü büyük ekranlara kadar çeşitli cihazlar ve form faktörlerinde çalışmak üzere tasarlanmıştır. Esnek düzen alt yapımız kullanıcıların yüzde 200 oranında yakınlaştırma yapmasına (bazı senaryolarda yüzde 200'den fazla) olanak tanır.

Akıllı telefonlar ve diğer küçük ekranlarda, denetimlerin ve form düzeninin, ana verilerin sık kullanılan olmasını sağlamak için duyarlı şekilde uyum sağlar. Bu duyarlı davranışlar, gruplardaki sütunların ve sekmelerin tek bir sütuna düşürülmesi, kabuk öğelerinin gizlenmesi ve eylem bölmesinin ortadan kaldırılması da içerir.

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Geliştiricilere ve müşterilere yardımcı olmak için kılavuz özelleştirmelerinde erişilebilir düşünceyi içerir.

Microsoft'un erişilebilirlik sağlama konusundaki en iyi uygulamaları hakkında daha fazla bilgi edinmek için bkz. [Formlar, ürünler ve denetimlerde erişilebilirlik](../../dev-itpro/user-interface/enable-accessibility.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]