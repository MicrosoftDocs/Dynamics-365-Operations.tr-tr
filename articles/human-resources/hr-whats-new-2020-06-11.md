---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 11 2020)
description: Bu konuda, 11 Haziran 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420982"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 11 2020)

Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır. Değişiklikler derleme numarası 8.1.3316 uygulanır. Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Kolaylaştırılmış çalışan formu bazen alt formu kapatma (X) düğmelerinin çalışmayı durdurmasına neden oluyor (442369)

Yeni **Çalışan** formu etkinleştirildiğinde, alt formlardaki kapat (**X**) düğmesi bazen çalışmıyordu. Bu aralıklı görülen bir sorundu. Ayrılıp geri döndüğünüzde formu kapatabiliyordunuz. Örneğin, sol taraftaki bir menü öğesini seçip **Çalışan** formuna geri döndüğünüzde formu kapatabiliyordunuz. Bu haftanın sürümüyle bu sorunu düzeltildi. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Çalışan kişisel ilgili kişi varlığı, kişisel ilgili kişileri üst ilişki türüyle birlikte dışarı aktarmıyor

Bu sürümde, **Çalışan kişisel ilgili kişi** varlığı tüm ilişki türlerini dışa aktarıyor.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity, varsayılan olarak Ceridian bordro tümleştirme paketinin parçası olmalıdır (448506)

Bu değişiklikle, **HcmPositionWorkerAssignmentV2Entity** Ceridian Bordro tümleştirme paketine dahil edildi.

## <a name="in-preview"></a>Ön izlemede

## <a name="database-logging"></a>Veritabanı günlüklerine kaydetme

Veritabanı günlükleri özelliği hangi tablo ve alanların izleneceğini belirlemenize olanak tanır. Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar. Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız. Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).

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

## <a name="new-platform-capabilities"></a>Yeni platform yetenekleri 

Kişiselleştirmeyi kullanarak alanları zorunlu hale getirebileceksiniz. Bu özellik, **Kaydedilmiş görünümleri** etkinleştirmenizi gerektirir.

## <a name="configure-the-name-of-employee-self-service"></a>Personel self servisini yapılandırma

Personel self servis çalışma alanının adını Self servis olarak güncelleştirmek için Human Resources parametrelerinde yeni bir seçenek kullanılabilir olacaktır. 

## <a name="see-also"></a>Ayrıca bkz.

[Human Resources'taki yenilikler veya değişiklikler](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Güncelleştirme işlemi](hr-admin-setup-update-process.md)</br>
[Özellikleri yönetme](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]