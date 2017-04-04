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
translationtype: Human Translation
ms.sourcegitcommit: aaf5c93a1ac71de27338c13218407616808ee001
ms.openlocfilehash: 39f2904a6b722ad0048ba1d94651098ee642079b
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-company-specific-hr-parameters"></a>Şirkete özgü İK parametreleri ayarlama

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

Ayarlar **maaş** sekmesi, bir sabit veya değişken maaş planı bilgisini kaydetmek istediğiniz kullanıcıların onaylaması gerekip gerekmediğini belirleyin. Seçerseniz **Kaydet doğrulamayı etkinleştir** onay kutusu, kullanıcıların bir maaş ile ilgili sayfa kapatmak istediğiniz zaman aldıkları kaydı kaydetmek isteyip istemediğinizi soran bir ileti. Bazı maaş Yönetimi sayfalarında kullanıcıların bilgileri silmek izin vermeyin. Bu nedenle, kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir. **Kaydetme doğrulamayı etkinleştir** onay kutusu temizlendiğinde, kayıtları her zaman hemen kaydedilir, büyük olasılıkla kullanıcı hazır olmadan önce. Performans yönetimi kullanıyorsanız, **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar. 

**numara serisini** sekmesindeki ayarlar uygulamalar, devamsızlık kayıtları, Maaş işlem sonuçları, olay sayıları, kurslar ve kurs gündemi gibi İnsan Kaynakları'ndaki öğeleri otomatik olarak atamak için kullanılan sıralarını belirler. Numara serisi referansları ve kodlarını korumak için kullanın **Number sequences** Listesi Sayfası (tıklayın **kuruluş yönetim**&gt;**Number sequences**&gt;**Number sequences**). 

**FMLA** sekmesi tanımlayan bir çalışanın FMLA için uygun olmak için kaç saat çalışması gerektiğini, uygunluğu için gerekli olan çalışma uzunluğu ve İstihdam İstihdam uzunluğunu belirlemek için kullanılan tarih başlangıcını tanımlar. Ayarlar da çalışanların hakkı FMLA saat sayısını ve FMLA kaç FMLA saat çalışanlar kullanmış hesaplamak için kullanılan bırakma takvimini tanımlar. **FMLA** sekmesi, yalnızca Amerika Birleşik Devletleri'nde şirketler için kullanılabilir. 

**Not:** Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz. Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur. Son olarak, **Çalışan Self-Servisi** sekmesinde ayarlar yöneticinin kendi çalışanlarının adına girebileceği bilgiyi belirler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Tüzel kişilikler arasında İK parametreleri ayarlama](set-up-hr-parameters-across-legal-entities.md)


