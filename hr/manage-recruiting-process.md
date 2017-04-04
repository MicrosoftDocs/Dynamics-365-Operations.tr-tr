---
title: "Bir işe alma sürecini yönetmek"
description: "Bu makalede açık pozisyonların ilan edilmesi ve başvuru sahiplerinin işe alınması işlemleri, başvuru sahibinin ve başvuru bilgilerinin takip edilmesi, başvuru sahipleriyle iş görüşmeleri gerçekleştirilmesi ve organizasyonunuzdaki açık pozisyonların doldurulması amacıyla bir veya daha fazla sayıda aday seçilmesi de dahil olmak üzere işe alan kişilerin bir işe alma sürecindeki adımları takip etmek üzere kullanabileceği bir konsept açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Bir işe alma sürecini yönetmek

Bu konu, işe alanlar bir personel arama sürecindeki adımları izlemek için kullanabileceğiniz çabalarını açık pozisyonları ve başvuranları işe almak da dahil olmak üzere, izleme başvuran ve uygulama bilgilerini, başvuranlar görüme ve kuruluşunuzdaki açık pozisyonları doldurmak için bir veya daha fazla aday seçerek bir kavramı açıklar.

<a name="overview"></a>Özet
--------

İşe alma projeleri, bir tüzel kişilik için açık pozisyonları doldururken tamamlamanız gereken adımları organize etmenize yardımcı olabilir. Başvuranı İstihdam kuruluşunuz için geçerlidir bir kişidir.  Bir uygulama bir başvuranın ifadesidir bir şirket tarafından görevli ilgi ve belirli bir açılış express ilgisini bir işe alma projesine bağlı.  Tek başvuran, kuruluşunuzda birden çok uygulama aynı tüzel kişilik içinde ya da birden fazla şirket olabilir.

<a name="recruitment-projects"></a>İşe alma projeleri
--------------------

İşe alma projeleri, işe alanlar bir veya daha fazla açık pozisyonları doldurma karşı ilerleme durumunu izlemek izin verir.  İşe alma projesi, departman ve pozisyonları bir veya daha fazla açık iş tanımlar. İşe alma projeler ayrıca açık pozisyonlar için şu bilgileri takip eder:
-   Açık pozisyonların tam sayısı
-   İşe alma müdür ve pozisyon için iletişim kurulabilecek alternatif kişi
-   İşe almanın onaylandığı tarih
-   Uygulama son başvuru tarihi
-   Tahmini işe başlangıç tarihi

İşe alma projesi, açık pozisyon için duyuru yapılmak üzere **Personel self servis** altında kullanılan **İş ilanını** içerir. Açık pozisyonun çalışanlara gösterilmesi için işe alma projesinin mutlaka bir **İş ilanına** sahip olması, ** Personel self serviste göster** alanının Evet konumuna ayarlanmış olması, **Başvuru son tarihinin** daha ileri bir tarih olması ve işe alma projesinin durumunun **Başlatıldı** olması gerekir. Aşağıdaki tabloda, olası işe alma projesi durumları ve bunların açıklamaları listelenmektedir.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Planlandı | Personel arama çabalarını Hazırlanmakta olan.  İşe alma, bu proje için henüz başlamadı. |
| Başladı   | Bu projedeki açık pozisyonlar için başvurular kabul edilmektedir.                    |
| Tamamlanan  | Bu proje için tüm açık pozisyonlar doldurulmuştur.                                          |
| İptal edildi  | İşe alma işlemi bu proje için iptal edilmiştir.                                           |

İşe alım yapacak kişiler ayrıca açık pozisyonların harici mecralarda duyurulması için kullanılan **Ortamı** kaydedebilir ve ayrıca proje veya uygulamalar ile ilgili**Gelişmeleri** takip edebilir.

<a name="applicants"></a>Başvuranlar
----------

Bir başvuran kuruluşunuzdaki proje için geçerli bir kişidir.  Başvuranlar, gelen arama için beceri büyük havuzu vererek, kuruluşunuzdaki tüm tüzel kişilikler arasında paylaşılır. Başvuru sahipleri için yeterlilikleri, referansları, lojman taleplerini ve kişisel bilgileri saklayabilirsiniz. Bir başvuran kaydı oluşturduğunuzda, Genel Adres Defteri'nde o başvuran kişi için kayıt oluşturulur. Başvuru sahipleri için aşağıdaki genel adres defterini güncellemek için**Başvuru sahibi** sayfasını kullanabilirsiniz:
-   Adres bilgileri
-   İletişim bilgileri
-   Kimlik bilgileri
-   Ad ile ilgili ayrıntılar
-   Kişisel bilgiler

## <a name="applications"></a>Başvurular
**Başvuru** sayfasında aldığınız iş başvurularındaki bilgileri kaydedebilirsiniz. Uygulama, kuruluşunuzda açarak işe ilgi Başvuranın ifadesidir.  Bir uygulama oluşturmak için başvuran bir başvuran veya kişi sisteminizde bulunması gerekir.
Başvuru sahipleri tarafından internetten gönderilen iş başvuruları, bir iş ilanı için girilen, talep edilen başvurular veya talep edilmeyen başvurulardır. Talep edilen başvurular otomatik olarak iş ilanının oluşturulduğu işe alma projesiyle ilişkilendirilir. Talep edilmeyen başvurular, **İnsan kaynakları parametreleri** sayfasındaki **İşe alma** alanında belirtilen işe alma projesiyle ilişkilendirilir.
### <a name="application-status"></a>Başvuru durumu

Başvuru durumu bir uygulamanın işe alma işleminin neresinde olduğunu gösterir. Aşağıdaki tabloda olası başvuru durumları ve bunlara ilişkin açıklamalar listelenmiştir.

| Durum    | Şunları gösterir…                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Alınan  | Başvuru alınmıştır.                                                             |
| Onaylandı | Başvurusunun alındığını doğrulamak üzere başvuru sahibine bir bildirim gönderilebilir.            |
| İş görüşmesi | Başvuru sahibine bir iş görüşmesi daveti gönderilebilir.                                     |
| Ret | Başvuru sahibine bir ret mektubu gönderilebilir.                                          |
| İptal edildi  | Başvuru sahibine bir iş geri çekme onayı gönderilebilir. Bu durum manuel olarak atanır. |
| İşe alındı  | Başvuru sahibine bir iş teklifi gönderilebilir.                                         |

### <a name="correspondence-actions"></a>Yazışma eylemleri

Bir **Başvuru sahibinin** iletişim eylemi, başvuruyu gönderen başvuru sahibiyle iletişim kurmak için kullandığınız belgeyi veya e-posta şablonunu belirler. İlişkilendirmek **başvuru yer işaretleri** uygulamadan değerlerini kullanmasına izin verecek şekilde Yazışma eylemi ile başvuran, görüşme ve işe alma projesi, Başvuranlarla iletişim sayfaları.  **Uygulama e-posta şablonları** hızlı bir uygulama belirli durum ve yazışma eylemi bileşimine sahip Başvuranlar için e-postalar göndermek için yazışma eylemleri için oluşturulabilir. Örneğin, kullanan tüm uygulamalar için bir onay e-posta gönderebilir bir **durum**, alınan ve bir **Yazışma eylemi** alınan.  E-postayı gönderdikten sonra uygulamaların durumunu otomatik olarak güncelleştirmek için seçeneğiniz vardır.

## <a name="application-routing"></a>Başvuru rotası

Bir başvurunun birden fazla çalışan tarafından incelenmesi gerekiyorsa, süreci yönetmek üzere bir çalışan dolaşım listesi oluşturmak için **Uygulama yönlendirme** sayfasını kullanabilirsiniz.

## <a name="interviews"></a>Görüşmeler

**Başvuran görüşmeleri** gelen zamanlanmış **uygulamalar** sayfa.  Kullanım **toplantı bilgilerini Gönder** başvuran ve görüşmeci görüşme zamanlama bilgilerini içeren bir takvim dosyası göndermek için düğme.

## <a name="skill-mapping"></a>Yetenek eşleme

Açık bir pozisyon için iyi bir aday olabilecek kişilerin belirlenmesi için **Yetenek eşleme** ve **Yetenek eşleme profilleri** kullanılabilir.

## <a name="hiring-applicants"></a>Başvuru sahiplerinin işe alınması

Bir başvuru sahibini işe almak için **Uygulamalar** sayfasını kullanın. Bir başvuru sahibini işe aldığınızda başvuru kaydının durumu **İşe alındı** olarak değişir ve başvuru sahibinin genel adres defteri kişi kaydı, yeni çalışan kaydıyla ilişkilendirilir. Yeni çalışan kaydı için genel adres defteri bilgileri üzerindeki değişiklikler yanı zamanda başvuru kaydında da görüntülenir. Bu yeni alt şimdiye kadar kuruluşunuzda farklı bir proje için geçerli olması durumunda, veri girişini azaltmak yardımcı olabilir.  Yeni bir konuma varolan bir çalışan işe almak için tıklatın **konumu değiştirmek** içinde **uygulama durumu** initiate aktarma işlemi için aşağı açılır.




