---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 25 2020)
description: Bu konuda, 23 Haziran 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127509"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 23 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3347 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>İşten çıkarılan bir çalışan için bir kayıt sona erdiğinde, kayıt türü, bakiye ve tutarın tümü kaydı bırak formunda temizlenir (444867)

Bu seçim yapıldığında, **izin türü**, **Bakiye** ve **tutar** değerlerinin artık temizlenmesi yerine bu değerler korunur.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Yeni Özellik (tek bir şirket veya tek bir plan için tahakkuku bırak) etkinleştirildiğinde tahmin edilen bakiye yanlış (456553)

Doğru tahmin edilen bakiye artık tek bir kurum veya tek bir plan için izin tahakkuku etkinleştirildiğinde gösterilir.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Yinelenen gezinme özelliklerine neden olan ilişkileri olan varlıklar (456486)

Bu sürüm, birden çok varlığın gezinme özellikleriyle ilgili bir sorunu düzeltir. Tekrarlanan ilişkiler algılandı. Bu senaryoların hepsi düzeltildi.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Performans incelemesi ile ilgili şirketler arası açıklamalar (455536)

Şirketler arası Yorumlar, bu düzeltmeyle ilgili performans incelemelerde artık görünür. Bu değişiklik, aynı performans incelemesi için farklı şirketlerde girilen gözden geçirici açıklamalarının görünümünü düzeltir.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Maaş yönetimi verilerini gösteren tutarsızlık (432562)

Dağıtım verilerinin tutarlı bir görünümü artık yönetici self servis 'de tutulur. Çalışanın **maaş ayrıntılarına** nasıl gittiğinize bağlı olarak maaş verileri artık sürekli olarak yöneticilere göre görüntülenir.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Sabit maaş planının geçerlilik tarihi varsayılan olarak bugünün tarihine (411994)

Maaş başlangıç tarihi şimdi çalışana atanan pozisyonun başlangıç tarihine göre yapılır.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Bırak ve devamsızlık formu bu form açıldığında yarım gün tanımını etkinleştir devre dışı bırakıldı (452607)

Bu değişiklikle, Yeni bırakma hareketleri olana kadar **yarım gün açıklamasını etkinleştir** özelliği etkinleştirilir. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Excel üzerinden HcmDiscussionEntity yayımlanamıyor; TotalRatingScore alanı hatası (453899)

Şimdi, Excel çalışma kitabı tasarımcısında **HCMDiscussionEntity** kullanarak **TotalRatingScore** alanını güncelleyebilirsiniz.

## <a name="in-preview"></a>Ön izlemede

## <a name="database-logging"></a>Veritabanı günlüklerine kaydetme

Veritabanı günlükleri hangi tablo ve alanların izleneceğini belirlemenize olanak tanır. Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar. Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız. Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Zorunlu alanlar 

Artık İnsan Kaynakları kişiselleştirme yetenekleri kullanarak alan zorunlu hale getirebilirsiniz. Bu özellik için **Kaydedilmiş görünümler** gereklidir .

## <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları
 
Kazançlar yönetimi varlıkları serbest bırakılıyor. DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır. Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır. Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.

## <a name="buy-and-sell-leave"></a>İzin satın alma ve satma 

Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar. Bu işlem genellikle el ile yönetilir. Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir. İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur. Daha fazla bilgi için bkz:

- [İzin satın alma ve satma ilkelerini yönetme](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [İzin satın alma ve satma](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Tek bir şirket veya tek bir plan için izin tahakkuku

Müşteriler tek bir şirket veya tek bir izin ve devamsızlık planı için tahakkukları işleyebilir. Bu özellik, farklı izin yılı veya izin tahakkuk ilkeleri olan müşteriler için tahakkuk işlemine açıklık sağlar. Daha fazla bilgi için bkz. [Şirket veya izin planı başına izin tahakkuku](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>İzin isteklerine ekler ekleme

Onaylanmış izin isteklerine ek ekleme yeteneği, geçerli COVID-19 ortamında kritik öneme sahip. Çalışanlar şimdi bu ekleri ekleyebilirler. Ayrıca, izin isteklerinde güncelleştirmelerin nasıl yapıldığıyla ilgili daha fazla öngörüye shaip olabilirler. Daha fazla bilgi için, bkz. [Mevcut bir isteğe ek ekleme](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Tahakkuk askıya almalara neden kodu ekleme 

Neden kodları tahakkuk askıya almaya eklenmiştir.

## <a name="carry-forward-rules"></a>Devretme kuralları 

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Belirtilen izin türleri için izin tahakkunu askıya alma

Ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilirsiniz. Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez. Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir 

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="coming-soon"></a>Çok yakında

## <a name="configure-the-name-of-employee-self-service"></a>Personel self servisini yapılandırma

Personel self servis çalışma alanının adını Self servis olarak güncelleştirmek için **Human Resources parametrelerinde** yeni bir seçenek kullanılabilir olacaktır.

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]