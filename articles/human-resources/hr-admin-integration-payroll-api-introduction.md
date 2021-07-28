---
title: Bordro tümleştirme API'sına giriş
description: Bu konuda, Dynamics 365 Human Resources Bordro tümleştirme API'sı açıklanmaktadır.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b6b01053a043477521d7eb1a41bb9f6f51fc0e4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360580"
---
# <a name="payroll-integration-api-introduction"></a>Bordro tümleştirme API'sına giriş

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu belgede, Dynamics 365 Human Resources Bordro tümleştirme API'sı açıklanmaktadır. API, Human Resources ve iş ortağı bordro sistemleri arasında uçtan uca sorunsuz tümleştirmeler sağlar. Tümleşik deneyim Human Resources'ta personel profili, maaş ve kesinti ve katkı bilgileri ile başlar. Bir çalışanı işe alıp gerekli profili ve ödeme bilgilerini Human Resources'a girdiğinizde bordro sistemi, bordroyu işlerken kullanmak için bu bilgileri çeker. Çalışan veya ödeme bilgilerinde yapılan tüm güncelleştirmeler de sonraki ödeme çalıştırmasında kullanılmak üzere çekilir.

[![Bordro tümleştirme akışı.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Tümleştirmeyi etkinleştirmek için Human Resources'ta aşağıdaki bileşenler bulunur:

- Bir çalışanı ödeme için hazır olarak işaretleme işlevi
- Uygulamaları tümleştirmeye yeni işlevsellik açan bir tümleştirme API'sı

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Bu API, Microsoft Dataverse (eski adıyla Common Data Service) üzerine kuruludur. Bu API ile tüm RESTful etkileşimi, OData kullanan Microsoft Dataverse Web API'si üzerinden yapılır. Bu API, Dataverse Web API'sinin bir alt kümesidir. Dataverse Web API'si; kimlik doğrulama, SLA'lar, toplu iş, eşzamanlılık denetimi ve hata işleme gibi özellikleri tanımlar.

Microsoft Dataverse Web API'si hakkında daha fazla genel bilgi için bkz:

- [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse Web API'sini kullanma](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse geliştirici kılavuzu](/powerapps/developer/data-platform)

Bu belge, aşağıdaki konular dahil olmak üzere Dataverse Web API'sını kullanmayla ilgili ayrıntıları ve geliştirici kılavuzunu içerir:

- [Web API'sı ile Microsoft Dataverse'te kimlik doğrulaması yapma](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Web API'sını kullanarak işlem gerçekleştirme](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Web API'sı ile Postman kullanma](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Verileri harici sistemlerle eşitlemek için değişiklik izlemeyi kullanma](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse'te Human Resources için sanal tablolar

Bordro tümleştirme API'sının uç noktaları, Microsoft Dataverse'ün sanal tablo platformu yeteneklerini kullanır. Varsayılan olarak, sanal tablolar ve ilişkili API uç noktaları Human Resources ortamları için dağıtılmamıştır ve kuruluşların ortam için hangi OData uç noktalarının kullanıma sunulacağını belirlemesine olanak tanır. API'yi kullanmak istiyorsanız ortam için Human Resources varlıklarına yönelik sanal tablolar oluşturulmalıdır.

API'ye yönelik sanal tablolar oluşturma hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Veri modeli

Aşağıdaki diyagramda API içindeki ilişkiler gösterilmektedir. Çeşitli türlerin, Human Resources'da önceden var olan ve burada belirtilmeyen diğer varlıkların yabancı anahtarları vardır. Bu belge, bordro tümleştirme senaryolarına özgü varlıklar hakkında bilgi sağlar. Ancak Human Resources için Dataverse Web API'sında tümleştirmenizle de ilgili olabilecek birçok başka varlık vardır. Bu varlıkların bazılarına yabancı anahtar ilişkilerinde veya gezinti özelliklerinde referans verilir.

[![Bordro Tümleştirme API'sı veri modeli.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Bordrolu personel ve ilgili varlıklar

Varlıklar:

- [Bordrolu personel](hr-admin-integration-payroll-api-payroll-employee.md)
- [Bordrolu çalışanın adresi](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Bordro sabit ücret planı](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Bordro değişken ücret planı](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Bordrolu pozisyon işi](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Bordrolu pozisyon](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Ayrıca bkz.

[Bordro varlıkları oluşturma ve gözden geçirme](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Human Resources parametrelerini yapılandırma](hr-setup-parameters.md)<br>
[Human Resources paylaşılan parametrelerini yapılandırma](hr-setup-shared-parameters.md)<br>
[Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API'sini kullanma](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
