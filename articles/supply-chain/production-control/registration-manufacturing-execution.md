---
title: "Üretim uygulama için kayıt"
description: "Bu konu üretim yürütmeyi yapılandırmak ve kullanmak için anlamanız gereken temel kavramları ve koşulları açıklar."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5d4ee2fb1cd58107043939c3721fd857909f16b
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="registration-for-manufacturing-execution"></a>Üretim uygulama için kayıt

[!include [banner](../includes/banner.md)]

Bu konu üretim yürütmeyi yapılandırmak ve kullanmak için anlamanız gereken temel kavramları ve koşulları açıklar. 

Üretim uygulama, temel olarak üretim şirketleri tarafından kullanılmak üzere tasarlanmıştır. Çalışanlar, **İş kaydı** sayfasını kullanarak üretim işlerindeki zaman ve madde tüketimini kaydedebilirler. Tüm kayıtlar onaylanır ve daha sonra ilgili modüllere transfer edilir. Kayıtların devamlı onaylanması ve transfer edilmesi müdürlerin, üretim emirlerindeki gerçek maliyetleri kolayca takip etmesine izin verir.

## <a name="manufacturing-execution-and-registration-terminology"></a>Üretim uygulama ve kayıt terminoloji
Aşağıdaki tabloda üretim uygulama ve ilgili kayıt görevler için geçerli terimler açıklanmıştır.

| Vade                          | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Üretim yürütme       | Üretim işlerinde, projelerde ve dolaylı faaliyetlerde zamanın, malzeme tüketiminin ve maliyetlerin kaydedilmesi için kullanılan bir işlevdir. Kayıt işlemi bir üretim uygulama kayıt istemcisinde yapılır.                                                                                                                                                                                                                                                                                                                                                                                                   |
| İş listesi                      | **İş kaydı** sayfasında çalışanlara belirli bir kaynak, örneğin bir makine üzerinde gerçekleştirmeleri gereken işlerin listesi gösterilir. Bir çalışan, iş listesindeki her bir iş veya görev için zaman ve madde tüketimi kaydı gerçekleştirebilir.                                                                                                                                                                                                                                                                                                                                                                           |
| İşleri gruplama                  | Bir çalışan **İş kaydı** sayfasında aynı anda birden faza işe başlıyorsa buna işleri gruplama adı verilir. Gruplanan işler için harcanan zaman, atama anahtarları kullanılarak tek tek işlere çeşitli şekillerde tahsis edilebilir.                                                                                                                                                                                                                                                                                                                                                         |
| Lider/asistan kayıtları | Bir çalışan, bir kaynağa bir asistan kaydedebilir ve birkaç çalışanın aynı üretim işlerinde çalıştığı, küçük bir ekip oluşturabilir. Çalışanların asistanlara bağlandığı kaynaklar liderler olarak adlandırılır. Sadece lider kaynak, kayıt yapabilir. Tüm asistanlar otomatik olarak aynı kayıtları alır. Örnek olarak, bir makine lider olarak hareket ediyorsa bu makine için asistan olarak kaydedilen çalışanlar **İş kaydı** sayfasında kayıtlar gerçekleştirebilir ve asistanlarla bağlantılı olan hem makine hem çalışanlar aynı kayıtları alır. |
| Dolaylı faaliyet             | Örneğin bir departman toplantısı, bir temizleme işi veya atölyedeki bir bakım işi gibi doğrudan bir üretim işiyle veya bir projeyle bağlantılı olmayan bir aktivite. Çalışanlar, üretim işlerinde ve projelerinde kaydettikleri gibi dolaylı faaliyetlerde de aynı şekilde kayıtlar oluşturabilirler.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Üretim uygulamada kayıtlar
Çalışanlar, üretim işlerinde gerçekleştirilen çalışma için üretim uygulamada farklı türlerde kayıtlar oluşturabilirler. Çalışanlar, sistem grubuna bağlı olarak proje faaliyetlerinde ve molalar, devamsızlıklar ve dolaylı faaliyetler vb. gibi üretime dayalı olmayan görevlerde de kayıtlar yapabilirler. Buradaki kayıt türleri şunlardır:

-   **Giriş saati/çıkış saati** (zaman ve katılım ile kullanılabilir) – Çalışanların işe geldiği saat giriş saati ve işten ayrıldığı saat çıkış saatidir.
-   **Üretim işlerinde kayıt** – Çalışanlar iş listelerinde görüntülenen üretim işleri için örneğin bir işin başlatılması ve bir iş için geribildirim raporlanması gibi kayıtlar gerçekleştirebilirler. Çalışanlar aynı anda birden fazla iş başlatabilirler. Buna iş gruplama adı verilir.
-   **Stok hakkında kayıt** – Çalışanlar atölyede kullanılan, ancak doğrudan üretim işleriyle bağlantılı olmayan malzemelerle ilgili kayıtlar oluşturabilirler. Bunlara örnek olarak gres, yağlayıcılar ve makinenin çalışmaya devam etmesi için gerekli olan diğer malzemeler gösterilebilir. Kayıt bir stok günlüğünde gerçekleştirilir.
-   **Projeler hakkında kayıt** (zaman ve katılımla birlikte kullanılabilir) – Çalışanlar, iş listelerinde görüntülenen projeler veya proje faaliyetleri hakkında örneğin çalışma başlatma ve çalışma sonlandırma vb. gibi kayıtlar oluşturabilirler.
-   **Proje giderleri ve proje maddeleri kaydetme** (zaman ve katılım ile birlikte kullanılabilir) – Çalışanlar bir proje gideri günlüğünde bulunan bir projeye ilgili olarak, örneğin kilometre ve köprü geçiş ücreti vb. gibi giderleri (harcamaları) kaydedebilirler. Çalışanlar ayrıca projelerdeki madde tüketimlerini de kaydedebilirler. Bu bir proje madde günlüğünde yapılır.
-   **Bir asistanı başka bir çalışana kaydetme** – İki veya daha fazla sayıda çalışan bir üretim işinde veya bir projede birlikte çalışıyorsa bir çalışan bir makineye asistan olarak kaydedilebilir ve diğer çalışan lider olarak görev yapar. Lider, gerekirse başka bir çalışanı lider olarak seçebilir.
-   **Devamsızlık kaydı** (zaman ve katılım ile birlikte kullanılabilir) – Çalışanlar, kurulmuş olan çeşitli devamsızlık kodlarına zaman kaydedebilirler. Bir çalışan işe geç geldiğinde, mesai gününde devamsızlık yapması gerekiyorsa veya standart çalışma süresi profiline göre beklenenden önce işten çıkarsa devamsızlık belirtilebilir.
-   **Mola kaydı** (zaman ve katılım ile birlikte kullanılabilir) – Mesai gününde çalışanlar mola vermek için iş istasyonlarından ayrılmalarını kaydedebilirler. Birkaç mola türü ayarlanabilir. Bir çalışan iş istasyonuna geri döndüğünde ve tekrar oturum açtığında sistem, çalışanın geri döndüğünü kaydeder ve mola kaydı sonlanır.
-   **Dolaylı faaliyetlerin kaydı** (zaman ve katılım ile birlikte kullanılabilir) – Dolaylı faaliyetlerdir örneğin departman toplantısı, bir ekip toplantısı veya atölyede gerçekleştirilen bir bakım işi vb. gibi çalışanlar bir mesai gününde içinde bulunabilecekleri, üretimle ilgili olmayan faaliyetlerdir. Çalışanlar, oluşturulmuş dolaylı faaliyetler için kayıtlar oluşturabilirler.
-   **Fazla mesai kaydı** (zaman ve katılım ile birlikte kullanılabilir) – Normal çalışma süresinden daha uzun çalışması istenen çalışanlar, çalışılan ekstra saatlerin esnek süre mi, yoksa fazla mesai mi olarak kaydedileceğini seçebilirler.





