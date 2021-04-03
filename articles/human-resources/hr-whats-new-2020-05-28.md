---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (28 Mayız 2020)
description: Bu konuda, 28 Mayıs 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e8d7f87f30286eefa1b3b53925702f4735132e6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465282"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (28 Mayız 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3287 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>İzin planı başına çoklu türleri etkinleştirdiğinizde LeaveRequest varlığı çalışmıyor (447498)

Bu değişiklikle, **LeaveEnrollmentV2Entity** artık çoklu izin türlerini etkinleştirdiğinizde ortaya çıkan hatayı düzeltebilir şekilde kullanılabilir.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Toplu çekişme azaltma özelliği (Önizleme) (446619)

Bu özelliği etkinleştirdiğinizde, görevleri ve işleri bitirmede toplu iş çerçevesi tablolarında bloke etmek için bir azaltma bekleyebilirsiniz.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>Çalışanı kaydederken UpdateConflict kişilerde bir kaydın düzenlenmesini engelliyor (427915)

Bu değişiklik, yeni bir çalışan eklerken, adres bilgilerini güncelleştirirken ve Dil tercihini değiştirirken oluşan bir hatayı düzeltir. Bu benzersiz senaryoda, kaydın güncelleştirilmediği bir hata görüntülenir. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Yeniden göndermek için onaylı bir izin isteğine bir ek eklenememesi (425407)

Bu değişiklik artık eklerin onaylanmış izin isteklerine izin veriyor.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Kullanıcı, başka bir yasal varlık formundaki bir çalışan için maaş girebilir (409529)

Bu değişiklik, yanlış yasal varlık için maaş kayıtlarının yanlışlıkla girilmesini önlemek üzere maaş seçeneklerini devre dışı bırakır.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Bir çalışan transfer ettiğinizde ve çalışan pozisyonu atama tarihi pozisyon süresinden önce olduğunda hata (429402)

Bu senaryodaki bir çalışanın aktarılması sırasında hata iletileri sorunu gidermek için gereken değişiklikleri daha iyi açıklayacak şekilde güncelleştirildi.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Çalışan Self Servis kazançları kaydında ek özellikleri
 
Artık çalışanın kayıt olduğu her plan için sosyal haklar kaydı işlemi sırasında ek ekleyebilirsiniz. Böylece, **çalışanların kayıtlı kazancı** formundaki ekleri görebilirsiniz .

## <a name="in-preview"></a>Ön izlemede

## <a name="human-resources-application-in-teams"></a>Teams'de Human Resources uygulaması

Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir . İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler. Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>İzni askıya alma

Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Tahakkukun askıya alınmış olduğunu belirtmek için kullanıcı deneyimini güncelleştirme (429550)

Kullanıcı deneyimi şimdi tahakkukun bir plan için askıya alınmış olduğunu gösteriyor.

## <a name="coming-soon"></a>Çok yakında

## <a name="database-logging-in-preview-in-june"></a>Veritabanı günlükleri (Haziran 'da önizlemede)

Veritabanı günlükleri özelliği hangi tablo ve alanların izleneceğini belirlemenize olanak sağlar. Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar. Bu değişiklikleri zaman içinde görmek için sorgulama özellikleri kullanılabilir.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>İzin satın alma ve satma (önizlemede 1 Haziran 'ta)

Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar. Bu işlem genellikle el ile yönetilir. Bu özellik, HR departmanı için ilkeleri ve istekleri yönetmenin daha otomatikleştirilmiş bir yolunu sağlar ve yönetim sürecini korurken hataları ortadan kaldırır. Daha fazla bilgi için bkz:

- [İzin satın alma ve satma ilkelerini yönetme](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [İzin satın alma ve satma](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları
 
Kazançlar yönetimi varlıkları serbest bırakılıyor. DMF varlıkları, sosyal haklar yönetimini kolayca konfigüre etmek için verilerin içe aktarılması ve verilmesi Veri taşımak için bir sosyal haklar yönetimi şablonu da kullanılabilecek. Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Tahakkuk askıya almalara neden kodu ekleme (1 Haziran)

Neden kodları tahakkuk askıya almaya eklenmiştir.

## <a name="carry-forward-rules-june-1"></a>Devretme kuralları (1 Haziran)

Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Belirtilen izin türleri için izin tahakkunu askıya alma (1 Haziran)

Bu sürümde İK, ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilir. Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez. Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>Tahakkuk askıya almaları için DMF varlığı kullanılabilir (1 Haziran)

DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]