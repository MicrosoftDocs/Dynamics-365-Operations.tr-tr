---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (20 Ağustos 2020)
description: Bu konuda, 20 Ağustos 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a97997212a090f141c7280f7e48fd116a1f31481
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062173"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (20 Ağustos 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3478 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Kişi çalışma alanındaki kartlarda yaklaşan ve bekleyen izin bilgilerini gösterme

Artık **Kişi** çalışma alanındaki İzin ve devamsızlık kartlarında bekleyen ve yaklaşan izin isteği seçenekleri bulunur.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Personel self servisi'deki Personel rolü için özel alan varsayılan olarak Evet değil (477106)

Artık **Özel** alan, personeller Personel self servisi'ndeki **Kişisel bilgiler** sayfası üzerinden yeni adres kayıtları eklediğinde varsayılan olarak **Evet** olur. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Personel yönetimindeki İşe alınacak adaylar hızlı sekmesinde hatalı aday sayısı gösteriliyor (470110)

Artık, **Personel yönetimi** sayfası işe alınacak aday sayısını doğru şekilde görüntüler. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Tahakkuk sıfır olarak ayarlandığında işten çıkarılan personel için hastalık izni girilemiyor (446195)

Gelecekte işten çıkarılacak ve tahakkuku sıfıra ayarlanmış personeller için artık izin işlemleri kullanılabilir. İzin işlemleri, personelin işten çıkarılma tarihine kadar girilebilir. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Yeni Çalışan formuna özel alanlar eklemek İzin yönetme eylem bölmesindeki alanları devre dışı bırakıyor (473314)

Yeni **Çalışan** formuna özel alanlar eklendiğinde **İzni yönet**'teki yeni **Çalışan** formunda yer alan eylem bölmesi seçenekleri devre dışı bırakılmayacak.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Yorum yaz alanını zorunlu hale getirme özelliği, izin isteğinin yorum girilmeden gönderilmesine izin veriyor (473543)

Yorum alanları artık zorunlu olabilir ve izin istekleri de bu ayara uyar. Zorunlu alanlar önizleme özelliğidir.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="in-preview"></a>Ön izlemede

### <a name="mandatory-fields"></a>Zorunlu alanlar

İnsan Kaynakları kişiselleştirme yeteneklerini kullanarak alanları zorunlu hale getirebilirsiniz. Bu özellik için **Kaydedilmiş görünümler** gereklidir . Kayıtlı görünümler hakkında daha fazla bilgi için bkz.

- Dynamics 365 2020 sürümü 2. dalga planında [Kayıtlı görünümler - genel kullanılabilirlik](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)
- [Kayıtlı görünümleri tamamen kullanan formlar oluşturma](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Çok yakında

### <a name="human-resources-app-in-teams-preview-features"></a>Teams'de Human Resources uygulaması önizleme özellikleri
 
-  **Bildirimler**: Teams'deki Human Resources uygulamasında izin isteklerini gönderen ve onaylayan kişiler bildirim alacak. Onaylayan kişiler, izin isteklerini onaylayabilecek veya reddedebilecek; gönderen kişiler ise istek onaylandığında veya reddedildiğinde bildirim alacak.
 
- **Yönetici izin takvimi**: Yöneticiler, doğrudan onlara bağlı çalışanlar için onaylanan ve bekleyen izinleri takvim görünümünde görebilecek. Bu görünüm, takım üyelerinin izinde olduğu tarihlerin daha kolay anlaşılmasını sağlar.

### <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

## <a name="known-issues"></a>Bilinen sorunlar

**Özellik yönetimi** çalışma alanı, genel kullanıma sunulduklarında önizleme özellikleri olarak devre dışı bırakılan özellikleri görüntülüyor olabilir. Aşağıda, yanlış durum gösteren genel kullanıma sunulmuş özelliklerin listesi verilmiştir. 

- Kazanç yönetimi
- Servis talebi yönetimi
- Veritabanı Günlük Kaydı (Denetleme)
- Tek bir şirket veya tek bir plan için izin tahakkuku
- İzin ve devamsızlık tahakkuku askıya alma
- Bakiye ayarlama neden kodu ve açıklaması
- İzin satın alma ve satma
- İzin ve devamsızlık takvimi
- İzin ileri taşıma kuralları
- İzin tahakkuku denetleme
- İzin tahakkuku silme işlemi
- İzin tahakkuku yuvarlama
- Tek bir izin planında birden fazla izin türü yapılandır
- İzin iyileştirmelerini güncelleştir
- Tahakkuklar için personelin tam zamanlı eşdeğerini kullan
- Şirketler arası ücret görünümü
- Performans incelemelerini yazdırma
- İzin tahakkuku tatil düzeltmeleri

### <a name="benefit-plan-employee-entity"></a>Kazanç planı personel varlığı 

Yakın zamanda, **BenefitsPlanEmployee** varlığıyla ilgili iki sorun tespit ettik. Çalışan kayıt anlaşmaları içeri aktarılırken **Kapsam kodu** ve **Plan türü kodu** hatalı ayarlanıyor. Bu sorun, personel kazanç planlarının Personel self servisi'ndeki **Çalışan kazanç planları** formunda ve **Açık kayıt anlaşması** formunda yanlış gösterilmesine neden oluyor. Bu sorun, personelin Personel self servisi'nde plan seçme özelliğini de etkileyebilir. Şu anda geçici çözüm yok. Bunu yüksek öncelikli bir düzeltme olarak ele alıyoruz ve bir sonraki sürümde düzeltmeyi sunacağız.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]