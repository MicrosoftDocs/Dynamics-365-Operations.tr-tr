---
title: Dynamics 365 Talent'taki yenilikler veya değişiklikler (Haziran 4 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4a42a3b817024447e2ff26cfcb3cdd0df1351158
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528062"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Dynamics 365 Talent'taki yenilikler veya değişiklikler (Haziran 4 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.

## <a name="changes-in-attract"></a>Attract'te değişiklikler

Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.

## <a name="coming-soon-in-attract"></a>Yakın zamanda Attract'e geliyor

### <a name="job-approvals-on-the-home-page"></a>Giriş sayfasındaki iş onayları

Onaylar, panonun bir **Onaylar** bölümünde görüntülenir. Onaylayanlar onayları **Size atandı**'nın altında gözden geçirebilir. Bu bölümde iş kimliği, unvan, diğer onaylayanlar ve işin atandığı tarih gösterilir. Bir işi onaya gönderen kullanıcılar **Sizin tarafından talep edilen**'in altında işlerini inceleyebilir. Bu bölüm, gönderilen işi hala onaylaması gereken onaylayanları gösterir.

## <a name="changes-in-onboard"></a>Onboard'daki değişiklikler

Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.

## <a name="changes-in-core-hr"></a>Core HR içindeki değişiklikler

Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2330 için geçerlidir.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Konum hiyerarşisi verilerini doğrulamak için yeni sayfa

İnsan kaynakları (İK), personel ve yöneticiler yanlışlıkla içe aktarılmış olabilecek herhangi bir döngüsel referans için yönetim hiyerarşisini doğrulayabilir. Bu yeni sayfaya Kuruluş yönetimi **Kuruluş yönetimi \> Bağlantılar \> Pozisyonlar \> Pozisyon hiyerarşisi doğrulaması üzerinden erişebilirsiniz**.

### <a name="specify-reason-codes-on-leave-types"></a>İzin türlerinde neden kodları belirtme

Kuruluşlar izin istekleri hakkında ek bilgiler gerektirebilir. Belirli bir izin türü ile ilişkili sebep kodlarını artık belirtebilir ve çalışanların izin taleplerinde bir sebep kodu seçmelerine olanak sağlayabilirsiniz.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>İzin talepleri üzerindeki belirli izin türleri için sebep kodları gerektir

Kuruluşlar, bir çalışan izin talepleri gönderdiğinde belirli izin türleri için sebep kodlarının ayarlanmasını gerektirebilir. Şirket ilkesi veya mevzuat gereksinimleri nedeniyle bu gereksinim bulunabilir. Hangi izin türlerini bir sebep koduna ihtiyaç duyduğunu belirtebilir ve personelin, izin taleplerinde bu izin türleri için sebep kodu sağlamalarını gerektirebilirsiniz.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>İK için izin ve devamsızlık hareket listesi sağlama

Çalışan iznini takip etme ve iznin nasıl hesaplandığını anlama özelliği, yalnızca İK'nın çalışan sorularına yanıt vermesine yardımcı olmaz, aynı zamanda çalışanlar için doğru izin ödülleri verilmesini sağlar. İK artık hareketlere (izinler, tahakkuklar, ayarlamalar ve talepler) erişimine sahiptir ve böylece İK personeli, izin bakiyeleri arkasındaki nedenleri görebilir.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Bir Talent kaydının silinmesi kaydın Common Data Service'ten kaldırılması anlamına gelmez

Talent: Core HR'dan kaldırılan kayıtlar artık Common Data Service'ten de kaldırılıyor.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Değişken ücret planı geçerli başlangıç/bitiş tarihleri kabul edilmemektedir

Başlangıç tarihi planın başlangıç tarihinden önce veya bitiş tarihi planın bitiş tarihinden sonra ise bu sürümde bir çalışanı değişken ücret planına kaydedemezsiniz. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Kullanıcılar İptal'i seçtikerinde performans gözden geçirme açıklamaları kaldırılır

Bu sürüm, bir yorumu değiştirmeye başlar ve sonra **iptal**'i seçerse inceleme yorumlarının kaldırıldığı sorunu düzeltir. 

## <a name="in-preview"></a>Ön izlemede

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Önizleme özellikleri yalnızca korumalı alan örneklerinde etkinleştirilir

Talent'ın yeni bir örneğini oluşturduğunuzda, örnek türünün **Üretim** veya **Korumalı alan** olduğunu belirtebilirsiniz. **Korumalı alan** türünün örnekleri yeni özelliklerin erken test edilmesine izin verir. Varolan tüm Talent örnekleri **Üretim** örneği türüne güncelleştirilecek. Varolan örneklerden birinin **Korumalı alan** örneği türüne güncelleştirilmesini istiyorsanız değişiklik isteğini başlatmak için  [Destek](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) başvurun.

Değişikliklerin nasıl yayımlanacağı hakkında daha fazla bilgi için, bkz [Talent sağlama](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>İzin taleplerindeki izin türlerini kısıtlama

Kuruluşlar, çalışanlara birçok farklı türde izin sunabilir. Ancak, çalışanların bazı izin türlerine zaman aşımı istekleri gönderebilmesi için uygun olmayabilir. Bu izin türleri İK tarafından yönetiliyor olabilir. Bu sürümde çalışanların serbest bırakma taleplerini hangi izin türlerine gönderebilecekleri ile ilgili olarak ayarlayabilirsiniz. 

## <a name="coming-soon-in-core-hr"></a>Core HR'da yakında çıkacak

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Yönetim self servisinde performans için genişletilmiş bilgileri görüntüle

Yeni bir seçenek, yöneticilerin hem doğrudan raporların hem de genişletilmiş raporlarının performansını görüntülemesine olanak sağlar. Şu anda, satır yöneticileri performans hedeflerini atayabilir ve güncelleştirebilir ve çalışanları birlikte yönetebilecek yeni incelemeler yapabilir. Ek olarak, doğrudan yöneticiler ve bunların çalışanları performans gözden geçirme işleminin sorunsuz şekilde devam etmesine yardımcı olmak için performans günlüklerini koruyabilir ve güncelleştirebilir. Bu değişiklik uygulandığında, yöneticiler, kendi talimatlarına ek olarak, genişletilmiş raporlarının performansla ilgili bilgilerini görüntüleyebilir ve koruyabilirler. 

### <a name="print-performance-reviews"></a>Performans incelemelerini yazdırma

Çalışanlar, Yöneticiler ve İK, bir çalışanın performans incelemesini yazdırabileceklerdir.
