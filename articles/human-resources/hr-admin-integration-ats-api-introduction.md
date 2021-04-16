---
title: Başvuran İzleme Sistemi tümleştirme API'si tanıtımı
description: Bu konuda Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'si açıklanmaktadır.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 599f9728019cd6bc59c59a4f08df06c6c9c9ac31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798447"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Başvuran İzleme Sistemi tümleştirme API'si tanıtımı

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'si açıklanmaktadır. API'nin amacı, Dynamics 365 Human Resources ile iş ortaklığı yapılan ATS'ler arasında kolaylaştırılmış tümleştirmeleri etkinleştirmektir.

![ATS tümleştirme akışı](media/hr-admin-integration-ats-api-introduction-flow.png)

Tümleştirilmiş deneyim, bir işe alma yöneticisi işe alım isteği oluşturduğunda Human Resources'da başlar. İstek etkinleştirildiğinde, ATS bir işe alım projesi oluşturma isteği için ayrıntıyı çeker. Ardından, pozisyonlar için bir aday seçmek ve işe almak için işe alım ardışık düzenini izler. Son olarak, ATS seçilen adayın kaydını Human Resources'a göndererek iki yönlü tümleştirmeyi tamamlar. Aday kaydı daha sonra çalışan kaydını oluşturmak için daha fazla ekleme doğrulaması ve iş akışından geçebilir.

Tümleştirmeyi etkinleştirmek için Human Resources aşağıdaki bileşenleri ekledi:

1.  İşe alma isteği oluşturma işlevi.
2.  Genişletilmiş aday profili ve ilgili iş akışları.
3.  Uygulamaları tümleştirmeye yeni işlevselliği açan bir tümleştirme API'si.

İşe alma isteğini ve aday işlevselliğini ayarlama ve kullanma hakkında daha fazla bilgi için bkz. [İş adaylarını işe alma](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Bu API, Microsoft Dataverse (eski adıyla Common Data Service) üzerine kuruludur. Bu API ile tüm RESTful etkileşimi, OData kullanan Microsoft Dataverse Web API'si üzerinden yapılır. Bu API, Dataverse Web API'sinin bir alt kümesidir. Dataverse Web API'si; kimlik doğrulama, SLA'lar, toplu iş, eşzamanlılık denetimi ve hata işleme gibi özellikleri tanımlar.

Microsoft Dataverse Web API'si hakkında daha fazla genel bilgi için bkz:

- [Microsoft Dataverse nedir?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse Web API'sini kullanma](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse geliştirici kılavuzu](https://docs.microsoft.com/powerapps/developer/data-platform)

Yukarıdaki belgeler, [kimlik doğrulamayı yönetme](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [işlemleri gerçekleştirme](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api) , [API ile Postman'i kullanma](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) ve API ile [değişiklik izleme veya delta belirteçlerini kullanma](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) gibi Dataverse Web API'sini kullanma hakkında ayrıntılar ve geliştirici kılavuzu içerir.

### <a name="option-sets"></a>Seçenek kümeleri

Bu belgede açıklanan ATS tümleştirme API'sinin veri modeli, varlık özellikleriyle ilişkili numaralandırılmış değerler sağlayan seçenek kümelerini içerir. Dataverse Web API'sinde seçenek kümeleriyle çalışma hakkında ayrıntılı bilgi için bkz. [Web API'sini kullanarak seçenek kümeleri oluşturma ve güncelleştirme](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets). Seçenek kümeleri her Dataverse ortamı için tanımlanır.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Dataverse'te Human Resources için sanal tablolar

ATS tümleştirme API'sinin uç noktaları , Microsoft Dataverse'ün sanal tablo platformu yeteneklerini kullanır. Varsayılan olarak, sanal tablolar ve ilişkili API uç noktaları Human Resources ortamları için dağıtılmamıştır ve kuruluşların ortam için hangi OData uç noktalarının kullanıma sunulacağını belirlemesine olanak tanır. API'yi kullanmak istiyorsanız ortam için Human Resources varlıklarına yönelik sanal tablolar oluşturulmalıdır. 

API'ye yönelik sanal tablolar oluşturma hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="data-model"></a>Veri modeli

Veri modeli iki ana varlığa odaklanır:

- **RecruitingRequest,** bir ATS'ye bir veya daha fazla açık pozisyon için gönderilen işe alma isteğini temsil eder. Örnek bir sorgu için bkz. [İşe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire**, bir pozisyon için teklifi kabul eden bir adayın ayrıntılarını temsil eder. **Kişi**, aday olan kişiyi temsil eder. Bir kişinin şirkette aday, işçi, çalışan veya yüklenici gibi birden fazla rolü alabilir. Örnek bir sorgu için, bkz. [İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Aşağıdaki diyagramda API içindeki ilişkiler gösterilmektedir. Çeşitli türlerin, Human Resources'da önceden var olan ve burada belirtilmeyen diğer varlıkların yabancı anahtarları vardır. Bu belge, işe alma tümleştirme senaryolarına özgü varlıklar hakkında bilgi sağlar. Ancak Dynamics 365 Human Resources için Dataverse Web API'sinde tümleştirmenizle de ilgili olabilecek birçok başka varlık vardır. Örneğin, burada tanımlanmayan çalışanlar, işler, pozisyonlar veya diğer varlıklar için de ayrıntıya ihtiyacınız olabilir. Bu varlıkların çoğuna yabancı anahtar ilişkilerinde veya gezinti özelliklerinde referans verilir.

![ATS Tümleştirme API'si veri modeli](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>İşe alma isteği ve ilgili varlıklar ve seçenek kümeleri

Örnek sorgu: 

- [Işe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Varlıklar:

- [İşe alma isteği](hr-admin-integration-ats-api-recruiting-request.md)
- [İşe alma isteği pozisyonu](hr-admin-integration-ats-api-recruiting-request-position.md)
- [İşe alma isteği becerisi](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [İşe alma isteği eğitimi](hr-admin-integration-ats-api-recruiting-request-education.md)
- [İşe alma isteği konumu](hr-admin-integration-ats-api-recruiting-request-location.md)

Seçenek kümeleri:

- [İş muafiyet durumu](hr-admin-integration-ats-api-job-exempt-status.md)
- [İşe alma isteği pozisyon durumu](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [İşe alma isteği durumu](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Mevzuat iş kategorisi](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>İşe alınacak aday ve ilgili varlıklar ve seçenek kümeleri

Örnek sorgu:

- [İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Varlıklar:

- [İşe alınacak aday](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Kişi](hr-admin-integration-ats-api-person.md)
- [Kişi eğitimi](hr-admin-integration-ats-api-person-education.md)
- [Kişi profesyonel deneyimi](hr-admin-integration-ats-api-person-professional-experience.md)
- [Kişi adresi](hr-admin-integration-ats-api-person-address.md)
- [Taraf ilgili kişisi](hr-admin-integration-ats-api-party-contact.md)
- [Kişi yeteneği](hr-admin-integration-ats-api-person-skill.md)
- [Değerlendirme düzeyi](hr-admin-integration-ats-api-rating-level.md)
- [Kişi sertifikası](hr-admin-integration-ats-api-person-certificate.md)
- [Sertifika türü](hr-admin-integration-ats-api-certificate-type.md)
- [Kişi filtreleme](hr-admin-integration-ats-api-person-screening.md)
- [Filtreleme türleri](hr-admin-integration-ats-api-screening-types.md)
- [Kişi kimlik numarası](hr-admin-integration-ats-api-person-identification-number.md)

Seçenek kümeleri:

- [Başvuran tümleştirmesi sonucu](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Boş Evet Hayır](hr-admin-integration-ats-api-blank-yes-no.md)
- [Tamamlanma durumu](hr-admin-integration-ats-api-completion-status.md)
- [İlgili kişi türü](hr-admin-integration-ats-api-contact-type.md)
- [Eğitim kredisi esası](hr-admin-integration-ats-api-education-credit-basis.md)
- [Cinsiyet](hr-admin-integration-ats-api-gender.md)
- [Medeni durum](hr-admin-integration-ats-api-marital-status.md)
- [Yılın ayları](hr-admin-integration-ats-api-months-of-year.md)
- [Hayır Evet](hr-admin-integration-ats-api-no-yes.md)
- [Dönem birimi](hr-admin-integration-ats-api-period-unit.md)
- [Filtreleme sıklığı](hr-admin-integration-ats-api-screening-frequency.md)
- [Filtreleme sıklığı oluşturma kaynağı](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Yetenek düzeyi türü](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Ayrıca bkz.

[İş adaylarını işe alma](hr-personnel-recruit.md)<br>
[Microsoft Dataverse nedir?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API'sini kullanma](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[Web API'sini kullanarak seçenek kümeleri oluşturma ve güncelleştirme](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]