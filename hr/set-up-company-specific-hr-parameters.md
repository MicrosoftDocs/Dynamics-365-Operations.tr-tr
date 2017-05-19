---
title: "Şirkete özgü İK parametreleri ayarlama"
description: "İnsan Kaynakları (HR) parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b4c362ecb6134158cb9f00d3670232043c7d619d
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Şirkete özgü İK parametreleri ayarlama

[!include[banner](includes/banner.md)]


İnsan Kaynakları (HR) parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

İki sayfa İnsan Kaynakları (HR) parametrelerini ayarlamak için kullanılır. Şirketler arasında paylaşılan parametreler için **İnsan Kaynakları paylaşılan parametreleri** sayfasını kullanırsınız. Şirkete özgü parametreler için (diğer bir deyişle, tek bir şirket için uygulanan ayarlar) **İnsan Kaynakları parametreleri** sayfasını kullanırsınız. **İnsan Kaynakları parametreleri** sayfasında ayarlar altı sekmeye ayrılır:

-   Genel
-   İşe alma
-   Ücret
-   Numara serileri
-   Aile ve sağlık Yasası (FMLA) bırakın.
-   Çalışan self servisi

Her sekme, tek bir şirketle ilgili bilgileri içerir. **genel** sekmesindeki ayarlar, Devamsızlık, yaralanma ve hastalık ve yeni işe alma hakkında bilgi görünümünü belirler. Bu sekmedeki ayarlar, çalışırken görünen bazı varsayılan girdileri de tanımlar. Özellikle bu sekme açık devamsızlık hareketlerine, raporlar için kullanılacak stil sayfasına uygulamak için bir renk seçmenizi, eğitim kursları ve devamsızlık kaydı arasında tümleştirmeyi etkinleştirmenizi ve bu tümleştirmeyi denetlemek için kullanılacak devamsızlık kodunu seçmenizi sağlar. Ayrıca yaralanma ve hastalık servis talebi olaylarının ne kadar tutulacağını gösterebilir ve yeni bir çalışan işe alındığında gösterilen varsayılan kimlik numarasını belirtebilirsiniz. 

**İşe alma** sekmesi, başvuranlar için otomatik olarak gönderilen yazışma için kullanılan belge tiplerini ve talep edilmemiş başvurular için kullanılan işe alma projesini tanımlar (belirli bir işe alma projesi için olmayan uygulamalar). İşe alma projesi eskimesi için tanımlanan dönem,**işe alma Yönetimi** çalışma alanındaki **projeleri eskime** içinde döşemeye dahil edilen işe alma projesini belirleyen işe alma projeleri belirler. Uygulama son başvuru tarihi uyarısı için tanımlanan dönem **işe alma** çalışma alanındaki **son başvuru tarihi yaklaşan** döşemesindeki son başvuru tarihi yaklaşan işe alma projeleri görüntülemek için kullanılan uygulama son uyarısı için kullanılır. 

**Ücret** sekmesindeki ayarlar, kullanıcının bir sabit veya değişken ücret planı bilgilerini kaydetmek istediklerini onaylamaları gerekip gerekmediğini tanımlar. **Kaydetme doğrulamasını etkinleştir** onay kutusunu işaretlerseniz, kullanıcılar ücretle ilgili bir sayfayı her kapatmak istediklerinde kaydı kaydetmek isteyip istemediklerini soran bir ileti alır. Ücret yönetimindeki bazı sayfalar kullanıcıların bilgileri silmesine izin vermez. Bu nedenle, kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir. **Kaydetme doğrulamayı etkinleştir** onay kutusu temizlendiğinde, kayıtları her zaman hemen kaydedilir, büyük olasılıkla kullanıcı hazır olmadan önce. Performans yönetimi kullanıyorsanız, **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar. 

**numara serisini** sekmesindeki ayarlar uygulamalar, devamsızlık kayıtları, Maaş işlem sonuçları, olay sayıları, kurslar ve kurs gündemi gibi İnsan Kaynakları'ndaki öğeleri otomatik olarak atamak için kullanılan sıralarını belirler. Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** listesi sayfasını kullanın (**Organizasyon yönetimi** &gt; **Numara serileri** &gt; **Numara serileri**'ne tıklayın). 

**FMLA** sekmesi tanımlayan bir çalışanın FMLA için uygun olmak için kaç saat çalışması gerektiğini, uygunluğu için gerekli olan çalışma uzunluğu ve İstihdam İstihdam uzunluğunu belirlemek için kullanılan tarih başlangıcını tanımlar. Ayarlar da çalışanların hakkı FMLA saat sayısını ve FMLA kaç FMLA saat çalışanlar kullanmış hesaplamak için kullanılan bırakma takvimini tanımlar. **FMLA** sekmesi, yalnızca Amerika Birleşik Devletleri'nde şirketler için kullanılabilir. 

**Not:** Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz. Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur. Son olarak, **Çalışan Self-Servisi** sekmesinde ayarlar yöneticinin kendi çalışanlarının adına girebileceği bilgiyi belirler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Tüzel kişilikler arasında İK parametreleri ayarlama](set-up-hr-parameters-across-legal-entities.md)




