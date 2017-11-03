---
title: "Şirkete özgü İK parametreleri ayarlama"
description: "İnsan Kaynakları (HR) parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c280b5ae3b8fc208759ec486db0a1015a9c24633
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-company-specific-hr-parameters"></a>Şirkete özgü İK parametreleri ayarlama

[!include[banner](includes/banner.md)]


İnsan Kaynakları (HR) parametrelerinin ayarları şirketler arasında paylaşılır ancak diğer parametrelerin ayarları şirkete özeldir. Bu makalede, şirkete özgü İK parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

İki sayfa İnsan Kaynakları (HR) parametrelerini ayarlamak için kullanılır. Şirketler arasında paylaşılan parametreler için **İnsan Kaynakları paylaşılan parametreleri** sayfasını kullanırsınız. Şirkete özgü parametreler için (diğer bir deyişle, tek bir şirket için uygulanan ayarlar) **İnsan Kaynakları parametreleri** sayfasını kullanırsınız. **İnsan Kaynakları parametreleri** sayfasında ayarlar altı sekmeye ayrılır:

-   Genel
-   İşe alma - bu, Dynamics 365 for Talent'a dahil edilmemiştir
-   Ücret
-   Numara serileri
-   Aile ve sağlık Yasası (FMLA) bırakın.
-   Çalışan self servisi

Her sekme, tek bir şirketle ilgili bilgileri içerir. **genel** sekmesindeki ayarlar, Devamsızlık, yaralanma ve hastalık ve yeni işe alma hakkında bilgi görünümünü belirler. Bu sekmedeki ayarlar, çalışırken görünen bazı varsayılan girdileri de tanımlar. Özellikle bu sekme açık devamsızlık hareketlerine, raporlar için kullanılacak stil sayfasına uygulamak için bir renk seçmenizi, eğitim kursları ve devamsızlık kaydı arasında tümleştirmeyi etkinleştirmenizi ve bu tümleştirmeyi denetlemek için kullanılacak devamsızlık kodunu seçmenizi sağlar. Ayrıca yaralanma ve hastalık servis talebi olaylarının ne kadar tutulacağını gösterebilir ve yeni bir çalışan işe alındığında gösterilen varsayılan kimlik numarasını belirtebilirsiniz. 

**İşe alma** sekmesi, başvuranlar için otomatik olarak gönderilen yazışma için kullanılan belge tiplerini ve talep edilmemiş başvurular için kullanılan işe alma projesini tanımlar (belirli bir işe alma projesi için olmayan uygulamalar). İşe alma projesi eskimesi için tanımlanan dönem,**işe alma Yönetimi** çalışma alanındaki **projeleri eskime** içinde döşemeye dahil edilen işe alma projesini belirleyen işe alma projeleri belirler. Uygulama son başvuru tarihi uyarısı için tanımlanan dönem **işe alma** çalışma alanındaki **son başvuru tarihi yaklaşan** döşemesindeki son başvuru tarihi yaklaşan işe alma projeleri görüntülemek için kullanılan uygulama son uyarısı için kullanılır. 

**Ücret** sekmesindeki ayarlar, kullanıcının bir sabit veya değişken ücret planı bilgilerini kaydetmek istediklerini onaylamaları gerekip gerekmediğini tanımlar. **Kaydetme doğrulamasını etkinleştir** onay kutusunu işaretlerseniz, kullanıcılar ücretle ilgili bir sayfayı her kapatmak istediklerinde kaydı kaydetmek isteyip istemediklerini soran bir ileti alır. Ücret yönetimindeki bazı sayfalar kullanıcıların bilgileri silmesine izin vermez. Bu nedenle, kullanıcılardan bilgilerinin kaydedilmesini istediklerini doğrulamalarını isteyerek, kaydedilen daha sonra silinemez bilgi miktarını sınırlama olanağınız olabilir. **Kaydetme doğrulamayı etkinleştir** onay kutusu temizlendiğinde, kayıtları her zaman hemen kaydedilir, büyük olasılıkla kullanıcı hazır olmadan önce. Performans yönetimi kullanıyorsanız, **Ücret** sekmesi performansı değerlendirirken tazminat planlarına atanan model yerine bir değerlendirme modeli kullanmayı seçmenizi sağlar. 

### <a name="previously-released-functionality"></a>Daha önce yayımlanan işlev
**numara serisini** sekmesindeki ayarlar uygulamalar, devamsızlık kayıtları, Maaş işlem sonuçları, olay sayıları, kurslar ve kurs gündemi gibi İnsan Kaynakları'ndaki öğeleri otomatik olarak atamak için kullanılan sıralarını belirler. Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** listesi sayfasını kullanın (**Organizasyon yönetimi** &gt; **Numara serileri** &gt; **Numara serileri**'ne tıklayın).

### <a name="if-youre-using-dynamics-365-for-talent"></a>Dynamics 365 for Talent kullanıyorsanız
**numara serisini** sekmesindeki ayarlar uygulamalar, devamsızlık kayıtları, Maaş işlem sonuçları, olay sayıları, kurslar ve kurs gündemi gibi İnsan Kaynakları'ndaki öğeleri otomatik olarak atamak için kullanılan sıralarını belirler. Numara serisi referanslarını ve kodlarını korumak için **Numara serileri** liste sayfasını kullanın (**Sistem yönetimi** &gt; **Bağlantı sekmeleri** &gt; **Numara serileri** &gt; **Numara serileri**'ne tıklayın). 

**FMLA** sekmesi tanımlayan bir çalışanın FMLA için uygun olmak için kaç saat çalışması gerektiğini, uygunluğu için gerekli olan çalışma uzunluğu ve İstihdam İstihdam uzunluğunu belirlemek için kullanılan tarih başlangıcını tanımlar. Ayarlar da çalışanların hakkı FMLA saat sayısını ve FMLA kaç FMLA saat çalışanlar kullanmış hesaplamak için kullanılan bırakma takvimini tanımlar. **FMLA** sekmesi, yalnızca Amerika Birleşik Devletleri'nde şirketler için kullanılabilir. 

**Not:** Çalışılan saat sayısı 1250'yi aşamaz ve 12 ay İstihdam uzunluğunu aşamaz. Bu en büyük değerler Amerika Birleşik Devletleri'nde federal yasalara uygundur. Son olarak, **Çalışan Self-Servisi** sekmesinde ayarlar yöneticinin kendi çalışanlarının adına girebileceği bilgiyi belirler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Tüzel kişilikler arasında İK parametreleri ayarlama](set-up-hr-parameters-across-legal-entities.md)




