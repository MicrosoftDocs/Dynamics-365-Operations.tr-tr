---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (08 Temmuz 2020)
description: Bu konuda, 8 Temmuz 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14dfd925009cb2a9d40044e27f28521ff4d331b7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130409"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (8 Temmuz 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3382 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="database-logging"></a>Veritabanı günlüklerine kaydetme

Veritabanı günlükleri hangi tablo ve alanların izleneceğini belirlemenize olanak tanır. Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar. Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız. Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Personel self servisi adını yapılandırma

**İnsan Kaynakları parametrelerinde** artık **Personel self servisi** çalışma alanının adını **Self servis** olarak değiştirebilirsiniz. Daha fazla bilgi için bkz. [Personel self servise çalışma alanı adını değiştirme](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Kazanç yönetimi açık kayıt erişimi dönem dışında

Bu sürüm, personelin kayıt dönemi dışındaki veya yaşam olayı olmaksızın açık kazanç kaydına erişebilmesini sağlayan bir hatayı düzeltir. Sonuç olarak, Personel self servisinde açık kaydı göstermeniz gerekiyorsa, erişilebilir olması için açık kayıt tarihlerini bugüne (veya daha öncesine) ayarlamanız gerekir. Bu ayarı, **Kazanç yönetimi > Kurallar ve seçenekler dönemleri** altından değiştirebilirsiniz.

## <a name="email-employee-enrollment-confirmation"></a>Personel kaydı e-posta onayı

Şimdi, kazanç seçimlerini tamamladıktan sonra personele e-posta gönderebilirsiniz. Varsayılan bir ileti gönderebilir veya bir kuruluş e-posta şablonu kullanabilirsiniz. Bu ayarlar, **İnsan kaynakları parametreleri > Kazanç yönetimi** altında bulunur.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>İptal edilen izin, Kişiler çalışma alanında yaklaşan izinde görünmeye devam ediyor (441358)

İptal edilen izin artık **Kişiler** çalışma alaındaki izin kartlarında yaklaşan izin olarak görünmüyor.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>PositionV2 varlığındaki departman varlığı özelliği kullanılamıyor (456486)

Artık, yinelenen ilişki oluşturmadan bir departman ekleyebilirsiniz.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity emeklilik planları için yalnızca hesaplanan alanları kullanmalıdır (459779)

**PayrollWorkerEnrolledBenefitDetailEntity** varlığı dışa aktarıldığında, dışa aktarma işlemi bir oran tablosuna göre bir hesaplanan alan mı veya destekleyici tablodaki **ContributionAmountCur** alanın mı kullanılması gerektiğini belirler. Veri varlığının kullandığı mantık, uygulamanın normalde kullanmadığı durumlarda oran tablosunu kullanır. Bu mantık varlık dışarı aktarma işlemlerinin bu sütun için bir sıfır değeri döndürmesine neden olur çünkü bir hesaplama oran tablosu yoktur ve ürün müşterinin bir tablo belirtmesine izin vermez.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Personel yönetimi ve Personel self servisinde Çekçe dilinde kafa karıştırıcı çeviri (400276)

Bu sürüm **Şirket dizini**, **Sonraki kayıtlı kurs**, **İş** ve **Pozisyon** için çevirileri düzeltir.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>WorkCalendarEmployment tablosunda oluşturulan veya değiştirilen sistem alanları sağlanmıyor (460171)

Oluşturulan ve değiştirilen sistem alanları artık Human Resources'taki **WorkCalendarEmployment** tablosunda sunulmaktadır.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Gelecekte personel işe alma ve ayrıntı ekleme için boş referans özel durumu (455475)

Bu sürüm, bir personel işe alındığında **İşe alma ve ayrıntı ekleme** seçeneği kullanıldığında personel girişinde oluşan bir hatayı (boş referans) düzeltir.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Dataverse Çalışan varlığında yapılan değişiklikler Human Resources'ta yansıtılmıyor (455652)

Dataverse'teki **Çalışan** varlığında aşağıdaki alanlarda yapılan değişiklikler artık Human Resources'ta görünecek:

- **Evden çalışıyor**
- **Kıdem tarihi**
- **Yıldönümü tarihi**
- **Orijinal işe alma tarihi**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Doğru ücret düzeyi pozisyona atanan işe göre varsayılana ayarlanmıyor (394136)

Bu değişiklikle, doğru ücret düzeyi **Pozisyon ayrıntıları** için **Geçerlilik tarihi** kayıtları ve **Ücret planı ataması**'nın **Başlangıç tarihi** temel alınarak varsayılana ayarlanmaktadır.

## <a name="in-preview"></a>Ön izlemede

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

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse'te bulunan denetim listesi varlıkları

Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)
