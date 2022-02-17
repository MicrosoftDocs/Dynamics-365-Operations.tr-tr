---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (06 Ağustos 2020)
description: Bu konuda, 6 Ağustos 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 08/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dbcf854330b7c5ba6ca812a5aed384584c05ce8d
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062198"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (06 Ağustos 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3444 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="platform-update-1001236-is-now-available"></a>Platform güncelleştirmesi 10.0.12(36) artık kullanılabilir durumdadır.

Daha fazla bilgi için bkz. [Finance ve Operations uygulamalarının 10.0.12 sürümü için platform güncelleştirmeleri (Ağustos 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları
 
Kazançlar yönetimi varlıkları serbest bırakılıyor. DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır. Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır. Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürüm dalgası 1. planında [DMF varlığı desteği](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support)
- [Veri yönetimine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire, izin istekleri satın alma ve satma için iş akışı oluşturuyor (446557)

Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 2. dalga planında [Çalışanların izin satın almasına ve satmasına olanak tanıyın](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)
- [İzin satın alma ve satma ilkelerini yönetme](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [İzin satın alma ve satma](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Çalışan posta adresleri V2 varlığı sınırlı erişimi olan tüzel kişilikler üzerinde erişime sahip (459126)

Bu değişiklikle, **Çalışan posta adresi V2** varlığı kullanıcıya verilen erişim iznini tüzel kişiliğe göre kısıtlayacaktır.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>İş akışı e-posta köprüsü ilgili incelemeleri açamıyor (437398)

İnceleme iş akışında performans incelemesi açmak için yer tutucuyu kullandığınızda, e-postada oluşturulan köprü şimdi seçili kaydı açıyor.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>İzin satın alma ve satma için yeni varlıklar (473180)

Veri yönetimi çerçevesi varlıkları şimdi izin satın alma ve satma için kullanılabilir. Daha fazla bilgi için bkz. [Veri yönetimine genel bakış](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Kayıt bilgilerini görüntülerken ve gelişmiş filtreleri kullanırken, kullanıcı diğer çalışanların kayıtlarına erişebiliyordu (472490)

Bu değişiklikle, Personel self servisi kullanıcıları personel self servisi kullanırken yalnızca kendi kayıtlarına erişebilir. Filtre uygulama seçeneğini değiştirirken kayıt bilgileri görüntülendiğinde artık ek veri gösterilmiyor.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Personel yönetimi analizi, çıkan çalışan kayıtlarını içeriyor (382893)

Bu sürümle, personel yönetimi analizi yalnızca etkin çalışanları içeriyor. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Bir çalışan için bir başarı artışı işlenemiyor (473125)

Bu değişiklik, yeni başarı artışı için yürürlük tarihini değiştirdiğinizde, başarı artışları girmenizi sağlıyor.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>İnceleme iş akışı birden fazla kez başlatılabiliyor (467541)

Bu değişiklikle, performans incelemesi iş akışını yalnızca bir kez başlatabilirsiniz. Yönetici durumu artık incelemeye başlama seçeneğini görüntülemiyor.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Onaylanan bir izin isteği iptal edilirken izin isteği iş akışı hatayla sonlanıyor (472063)

Bu sürümde, onaylı bir izin isteğini iptal ettiğinizde, isteğin durumu artık onaylanmış durumda kalmıyor ve iş akışı devam ediyor.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Şablondan yeni bir inceleme oluştururken sistem işten çıkmış olan çalışanları öneriyor (460624)

Bu değişiklikle, bir şablondan yeni incelemeler oluştururken, işten çıkan çalışanlar kullanılmayacak. İstihdam tarihleri dışında olan çalışanlar için incelemeler oluşturamazsınız.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Pozisyon hiyerarşisi döngüsel başvuru algılaması (415879)

Bu değişiklikle, konum hiyerarşisi dairesel referans algılaması zaman içindeki tek bir noktaya sınırlanır. Farklı tarihler için döngüsel referans algılamasını, raporlama yapısının herhangi bir döngüsel referansı olmadığını doğrulamak için çalıştırabilirsiniz.

## <a name="buy-and-sell-leave"></a>İzin satın alma ve satma 

Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar. Bu işlem genellikle el ile yönetilir. Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir. İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 2. dalga planında [Çalışanların izin satın almasına ve satmasına olanak tanıyın](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave)
- [İzin satın alma ve satma ilkelerini yönetme](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [İzin satın alma ve satma](./hr-employee-self-service-buy-sell-leave.md)

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

## <a name="in-preview"></a>Ön izlemede

### <a name="mandatory-fields"></a>Zorunlu alanlar

İnsan Kaynakları kişiselleştirme yeteneklerini kullanarak alanları zorunlu hale getirebilirsiniz. Bu özellik için **Kaydedilmiş görünümler** gereklidir . Kayıtlı görünümler hakkında daha fazla bilgi için bkz.

- Dynamics 365 2020 sürümü 2. dalga planında [Kayıtlı görünümler - genel kullanılabilirlik](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)
- [Kayıtlı görünümleri tamamen kullanan formlar oluşturma](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz:

- Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams'de Human Resources uygulaması](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="coming-soon"></a>Çok yakında

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

## <a name="known-issues"></a>Bilinen sorunlar

**Özellik yönetimi** çalışma alanı, genel kullanıma sunulduklarında önizleme özellikleri olarak devre dışı bırakılan özellikleri görüntülüyor olabilir. Aşağıda, yanlış durum gösteren genel kullanıma sunulmuş özelliklerin listesi verilmiştir. 

1.  Kazanç yönetimi
2.  Servis talebi yönetimi
3.  Veritabanı Günlük Kaydı (Denetleme)
4.  Tek bir şirket veya tek bir plan için izin tahakkuku
5.  İzin ve devamsızlık tahakkuku askıya alma
6.  Bakiye ayarlama neden kodu ve açıklaması
7.  İzin satın alma ve satma
8.  İzin ve devamsızlık takvimi
9.  İzin ileri taşıma kuralları
10. İzin tahakkuku denetleme
11. İzin tahakkuku silme işlemi
12. İzin tahakkuku yuvarlama
13. Tek bir izin planında birden fazla izin türü yapılandır
14. İzin iyileştirmelerini güncelleştir
15. Tahakkuklar için personelin tam zamanlı eşdeğerini kullan
16. Şirketler arası ücret görünümü
17. Performans incelemelerini yazdırma
18. İzin tahakkuku tatil düzeltmeleri

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]