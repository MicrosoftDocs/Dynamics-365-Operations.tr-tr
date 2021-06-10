---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (23 Temmuz 2020)
description: Bu konuda, 23 Temmuz 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055401"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (23 Temmuz 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3416 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Bir Pozisyonda Mali Boyutları silmek beklenen şekilde çalışmıyor (445476)

Bir pozisyondan boyutları kaldırmak, artık aynı pozisyonları Dataverse'ten de kaldırır.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Hiyerarşide bulunmayan pozisyonlar etkin olmayan pozisyonları gösteriyor (397257)

Etkin olmayan (süresi dolmuş) pozisyonlar, artık **Hiyerarşide bulunmayan pozisyonlar** olarak pozisyon hiyerarşisinde görüntülenmiyor. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Data Management Framework (DMF) üzerinde LeaveEnrollmentEntity ve HcmWorkerEntity arasında gerçekleştirilen doğrulama, yavaş veri yükleri oluşmasına neden oluyor (442324)

Bu sürümdeki değişiklikler **LeaveEnrollmentEntity** performansını artırır.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Kuruluş yönetimi kişiselleştirilemiyor (447490)

Bu değişiklikle, artık **Kuruluş yönetimi** içindeki bağlantıları kişiselleştirebilirsiniz.

## <a name="in-preview"></a>Ön izlemede

## <a name="mandatory-fields"></a>Zorunlu alanlar 

Artık İnsan Kaynakları kişiselleştirme yetenekleri kullanarak alan zorunlu hale getirebilirsiniz. Bu özellik için **Kaydedilmiş görünümler** gereklidir .

## <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](./hr-admin-teams-leave-app.md). 

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

## <a name="platform-changes"></a>Platform değişiklikleri

Platform güncelleştirmesi 10.0.12 (36)

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]