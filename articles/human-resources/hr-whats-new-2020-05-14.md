---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (14 Mayız 2020)
description: Bu konuda, 14 Mayıs 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127861"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (14 Mayız 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3244 uygulanır. Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.

## <a name="platform-changes"></a>Platform değişiklikleri

Platform değişiklikleri, bu haftaki sürüme dahil edildi. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.10 sürümü için platform güncelleştirmeleri (Mayıs 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Bu sürümde, hata düzeltmeleri ve kaydedilmiş görünümlerde değişiklikler bulunmaktadır.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Dataverse seçim listelerinin İzin sabit listeleriyle tutarlı olduğundan emin olma (436343)

Dataverse seçim listeleri artık İzin sabit listeleriyle tutarlı.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>İzin isteği iş akışını, istek miktarına göre kullanıcıların yapılandırmasına izin verme (300044)

Kullanıcılar, izin istekleri iş akışlarını istek miktarına göre yapılandırabilir.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Yeni çalışan formunun, gelişmiş güvenlik etkinleştirildiğinde Görünüm menüsü aracılığıyla verileri göstermesi (403185)

Bu sürüm, gelişmiş erişim etkinleştirildiğinde ve diğer şirketlerdeki çalışanlar erişilebilir olduğunda çalışanların görüntülenme sorunlarını tüzel varlıklar işlevleriyle düzeltir.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Tek bir plan veya tek bir şirket için izin tahakkuklarının çalışmasına izin verme (318844)

Bu değişiklikle, bir şirket veya plan için tahakkukları çalıştırabilirsiniz.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Pozisyonun tam zamanlı eşdeğerini (FTE) Kayıtlı işçi formunda gösterme (414658)

FTE değeri, izin türünde FTE seçeneği etkinleştirilmişse işçinin tahakkuk oranını işçinin bulunduğu konumdan belirler. Bu alan artık **Kayıtlı işçiler** formuna ve **Toplu kayıt** iletişim kutusuna dahil edilmiştir.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>İzin bakiyesi geçerlilik bitiş tarihleri, toplu işi ekleme (431266)

Artık her gün çalışan yeni bir toplu iş kullanılabilir. Geçerlilik bitiş tarihleri geldiğinde kalan izin bakiyesini azaltır.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Çalışanın kişisel ilgili kişi varlığını kullanarak bir çalışan için kişisel ilgili kişileri dışa aktarma işlevinin Ana ilişki türündeki kişisel ilgili kişileri dışa aktarmaması (345893)

**Çalışanın kişisel ilgili kişi** veri varlığı (DMF'de **HcmPersonalContactPersonEntity** ve OData'da **PersonalContactPerson**), **Ana** ilişki türüne sahip kişisel ilgili kişileri dışarı aktaramaz. Bu sorun, bu değişiklikten sonra oluşturulan kişisel ilgili kişiler için düzeltildi. **Ana** türündeki var olan kişisel ilgili kişiler, daha sonraki bir sürümde düzeltilecektir.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Neden kodlarının, İzin ve devamsızlık olarak işaretlendiklerinde ve akıcı çalışan formu etkinleştirildiğinde farklı senaryolarda görüntülenmesi (434163)

Bu değişiklik, akıcı çalışan girişini etkinleştirdiğinizde neden kodlarının yalnızca İzin ve devamsızlık kodlarıyla sınırlandırılmasını sağlar.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Gelecek dönem için çalışanlara izin planı atama önizleme özelliğinin hata göstermesi (433555)

Bu değişiklik, izin planına iki izin türünün atandığı ancak bir çalışan atamaya çalıştığınız durumlarda oluşan hatayı düzeltir.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Başlarken başlığının tüm kullanıcılar için görüntülenmesi (441731)

Bu değişiklikle birlikte Başlarken başlığı, Sistem yöneticisi veya Veri yönetimi yöneticisi olmayan kullanıcılar için gizlenir. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Dataverse Çalışan Adresi varlığının Human Resources'taki tarih saat bilgilerinin geçerli olduğu tarihler açısından farklı çalışması (425071)

Bu değişiklik, adres bilgilerini adres tarihlerine göre belirli senaryolarda hizalanmış halde tutar.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Onaylı bir izin isteğine bir ek eklenememesi (425407)

Bu hafta yayımlanan sürümle, izin isteklerini değiştirmeden onaylı izin isteklerine ek ekleyebilirsiniz.

## <a name="in-preview"></a>Ön izlemede

## <a name="leave-suspension"></a>İzni askıya alma

Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Tahakkukun askıya alınmış olduğunu belirtmek için kullanıcı deneyimini güncelleştirme (429550)

Kullanıcı deneyimi şimdi tahakkukun bir plan için askıya alınmış olduğunu gösteriyor.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Belirtilen izin türleri için izin tahakkunu askıya alma (272447)

Bu sürümde İK, ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilir. Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez. Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir (429549)

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Tahakkuk askıya almalara neden kodu ekleme (429547)

Neden kodları tahakkuk askıya almaya eklenmiştir.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>İnsan Kaynakları parametrelerinden izin ve devamsızlık parametrelerine geçişi başlat

Bu sürüm İnsan Kaynakları parametrelerini İzin ve devamsızlık parametreleriyle birleştirmeye başlar.

## <a name="carry-forward-rules"></a>Devretme kuralları

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]