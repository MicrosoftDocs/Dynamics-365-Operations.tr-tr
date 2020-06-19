---
title: İnsan Kaynakları parametrelerini yapılandır
description: İnsan Kaynakları parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428745"
---
# <a name="configure-human-resources-parameters"></a>İnsan Kaynakları parametrelerini yapılandır

İnsan Kaynakları (HR) parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

İki sayfa İnsan Kaynakları (HR) parametrelerini ayarlamak için kullanılır. Şirketler arasında paylaşılan parametreler için **İnsan Kaynakları paylaşılan parametreleri** sayfasını kullanırsınız. Şirkete özgü parametreler için (diğer bir deyişle, tek bir şirket için uygulanan ayarlar) **İnsan Kaynakları parametreleri** sayfasını kullanırsınız. **İnsan Kaynakları parametreleri** sayfasında ayarlar altı sekmeye ayrılır:

-   Genel
-   İşe alma - Dynamics 365 Human Resources içine dahil değildir
-   Maaş
-   Numara serileri
-   Aile ve sağlık Yasası (FMLA) bırakın.
-   Çalışan self servisi

Her sekme, tek bir şirketle ilgili bilgileri içerir. **genel** sekmesindeki ayarlar, Devamsızlık, yaralanma ve hastalık ve yeni işe alma hakkında bilgi görünümünü belirler. Bu sekmedeki ayarlar, çalışırken görünen bazı varsayılan girdileri de tanımlar. Özellikle bu sekme açık devamsızlık hareketlerine, raporlar için kullanılacak stil sayfasına uygulamak için bir renk seçmenizi, eğitim kursları ve devamsızlık kaydı arasında tümleştirmeyi etkinleştirmenizi ve bu tümleştirmeyi denetlemek için kullanılacak devamsızlık kodunu seçmenizi sağlar. Ayrıca yaralanma ve hastalık servis talebi olaylarının ne kadar tutulacağını gösterebilir ve yeni bir çalışan işe alındığında gösterilen varsayılan kimlik numarasını belirtebilirsiniz. 

**İşe alma** sekmesi, başvuranlar için otomatik olarak gönderilen yazışma için kullanılan belge tiplerini ve talep edilmemiş başvurular için kullanılan işe alma projesini tanımlar (belirli bir işe alma projesi için olmayan uygulamalar). İşe alma projesi eskimesi için tanımlanan dönem,**işe alma Yönetimi** çalışma alanındaki **projeleri eskime** içinde döşemeye dahil edilen işe alma projesini belirleyen işe alma projeleri belirler. Uygulama son başvuru tarihi uyarısı için tanımlanan dönem **işe alma** çalışma alanındaki **son başvuru tarihi yaklaşan** döşemesindeki son başvuru tarihi yaklaşan işe alma projeleri görüntülemek için kullanılan uygulama son uyarısı için kullanılır. 

**Ücret** sekmesindeki ayarlar, kullanıcının bir sabit veya değişken ücret planı bilgilerini kaydetmek istediklerini onaylamaları gerekip gerekmediğini tanımlar. **Kaydetme doğrulamasını etkinleştir** onay kutusunu işaretlerseniz, kullanıcılar ücretle ilgili bir sayfayı her kapatmak istediklerinde kaydı kaydetmek isteyip istemediklerini soran bir ileti alır. Ücret yönetimindeki bazı sayfalar kullanıcıların bilgileri silmesine izin vermez. Bu nedenle, kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir. **Kaydetme doğrulamayı etkinleştir** onay kutusu temizlendiğinde, kayıtları her zaman hemen kaydedilir, büyük olasılıkla kullanıcı hazır olmadan önce. Performans yönetimi kullanıyorsanız, **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar. 

### <a name="previously-released-functionality"></a>Daha önce yayımlanan işlev

**numara serisini** sekmesindeki ayarlar uygulamalar, devamsızlık kayıtları, Maaş işlem sonuçları, olay sayıları, kurslar ve kurs gündemi gibi İnsan Kaynakları'ndaki öğeleri otomatik olarak atamak için kullanılan sıralarını belirler. Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** listesi sayfasını kullanın (**Organizasyon yönetimi** &gt; **Numara serileri** &gt; **Numara serileri**'ne tıklayın).

> [!NOTE]
> Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz. Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur. Son olarak, **Çalışan Self-Servisi** sekmesinde ayarlar yöneticinin kendi çalışanlarının adına girebileceği bilgiyi belirler.
