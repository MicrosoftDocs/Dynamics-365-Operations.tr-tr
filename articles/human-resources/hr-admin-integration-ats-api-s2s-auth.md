---
title: ATS tümleştirme API'sı için sunucudan sunucuya kimlik doğrulaması
description: Bu konuda, Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'sına karşı tümleştirmeler için sunucudan sunucuya kimlik doğrulamasının nasıl ayarlanacağı açıklanmaktadır.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 350fb5a00b85f28fa8aef2ca50cf1f277b8f635e
ms.sourcegitcommit: e4cc43b06ef3f0f562849e2c960025cb244d6017
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743555"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>ATS tümleştirme API'sı için sunucudan sunucuya kimlik doğrulaması


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'sına karşı uygulama tümleştirmeleri için sunucudan sunucuya kimlik doğrulamasının nasıl ayarlanacağı açıklanmaktadır. Microsoft Dataverse sanal tablosuna ve ilişkili verilere erişebilmek için, hizmet sorumlusu için yönetilmesi gereken birkaç güvenlik katmanı vardır. Kullanıcıya Microsoft Power Platform'da Dataverse sanal tablosuna erişim izni ve Dynamics 365 Human Resources'daki verilere erişim hakkı verilmesi gerekir.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Power Platform'daki Dataverse sanal tablolarına erişim verme

Power Platform'daki Dataverse sanal tablolarına erişim vermenin ilk adımı, Power Platform'da uygulamanızı Dataverse sanal tablosu uç noktalarına karşı kimlik doğrulaması için ayarlamaktır. Bunu yapma adımları [Microsoft Dataverse geliştirici kılavuzunda](/powerapps/developer/data-platform) özetlenmiştir.

  - Tek kiracılı uygulama kayıtları: [Tek Kiracılı sunucudan sunucuya kimlik doğrulaması kullanma](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Birden çok kiracılı uygulama kayıtları: [Birden çok kiracılı sunucudan sunucuya kimlik doğrulaması kullanma](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>ATS tümleştirmeleri için güvenlik rolü oluşturma

Uygulama kullanıcısını oluşturduktan sonraki adımlardan biri, kullanıcıyı uygulamanın uç noktalara sahip olacağı erişimi tanımlayan bir güvenlik rolüne atamaktır. Bu, tek kiracılı uygulama kayıtları için [Uygulama kullanıcısı oluşturma](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) ve birden çok kiracılı kayıtlar için [Uygulama kullanıcısı için güvenlik rolü oluşturma](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) işleminin 7. adımıdır. 

Uygulama kullanıcısını atadığınız rolün ATS tümleştirmesinde kullanılan veri varlıklarına erişimi olmalıdır. Bu, hazır olarak kullanıma sunulmadığından yeni bir güvenlik rolünün oluşturulması gerekecektir. Yeni rol, [Güvenlik rolü oluşturma](/power-platform/admin/create-edit-security-role#create-a-security-role) alanında özetlenen adımlar izlenerek oluşturulabilir.

Yeni rol için, en azından yeni rolün **Özel Varlıklar** sekmesindeki aşağıdaki varlıklara uygun erişimin atanması gerekir. Tümleştirme daha kapsamlı uygulama verileri kullanıyorsa, eklemeniz gerekebilecek ek varlıklar olabileceğini unutmayın. Yeni rol oluşturulduktan sonra, uygulama kullanıcısına atanabilir.

  - Temel çalışan (mshr)
  - İşe alınacak aday (mshr)
  - Sertifika yeterliliği (mshr)
  - Sertifika türü (mshr)
  - Şirket
  - Ücret iş görevi (mshr)
  - Ücret iş türü (mshr)
  - Ülke/bölgeler (mshr)
  - Departman (mshr)
  - Eğitim yeterliliği (mshr)
  - Eğitim derecesi (mshr)
  - Eğitim disiplinleri (mshr)
  - Eğitim gereksinimleri (mshr)
  - Kimlik (mshr)
  - Kimlik türü (mshr)
  - Kurum (mshr)
  - Veren kurum (mshr)
  - İş ücreti (mshr)
  - İşler (mshr)
  - Eğitim düzeyi (mshr)
  - Taraf ilgili kişileri (mshr)
  - Kişiler (mshr)
  - Kişi adresleri (mshr)
  - Kişi eleme (mshr)
  - Pozisyon türü (mshr)
  - Pozisyonlar V2 (mshr)
  - Profesyonel deneyim yetkinliği (mshr)
  - Değerlendirme düzeyi (mshr)
  - Değerlendirme modelleri (mshr)
  - Neden kodları (mshr)
  - İşe alma isteği (mshr)
  - İşe alma isteği konumu (mshr)
  - İşe alma isteği pozisyonu (mshr)
  - İşe alma isteği becerileri (mshr)
  - Eleme türü (mshr)
  - Beceri yetkinliği (mshr)
  - Beceriler (mshr)
  - Unvanlar (mshr)
  - Gazilik durumu (mshr)
  - Çalışan (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Human Resources verileri için uygulama izinleri verme

İkinci adım, uygulamayı Human Resources uygulamasındaki bir kullanıcıya bağlayarak uygulamaya Human Resources verilerine uygun izinlerin verilmesini sağlamaktır. Bir uygulama kullanıcısı için, Dataverse sanal tabloları aracılığıyla sunucudan sunucuya aramalar, Dataverse'deki eylemi çağıran kullanıcı (uygulama) kimliğinin bağlamında yapılır. Sanal tablo bağdaştırıcısı hizmeti, Human Resources'taki ilişkili kullanıcıyı arar ve sorguyu o kullanıcının bağlamında çalıştırır. Bu, tümleştirilen uygulamanın gereksinim duyduğu verilere erişim sağlamak için kullanıcının doğru roller atanarak Human Resources içinde oluşturulması gerektiği anlamına gelir.

Human Resources kullanıcısının, Human Resources verileri için doğru izinlere atanması da gerekecektir. **İşe Alma Uygulaması** (HcmRecruitingIntegrator) rolü, işe alma verileriyle tümleştirme için gerekli olan birincil varlıkların ayrıcalıklarıyla kullanılabilir. Verilere uygun erişim hakkı vermek için, **Kullanıcılar** sayfasında uygulama kullanıcısına bu rol atanabilir. Human Resources güvenlik rolleriyle ilgili daha fazla bilgi için bkz. [Role dayalı güvenlik](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>Yeni kullanıcıyı uygun izinlerle ayarlama

Yeni kullanıcıyı uygun izinlerle ayarlamak için bu adımları izleyin:

  1. Human Resources'daki **Kullanıcılar** sayfasını açın ve **Yeni**'yi seçin.
  2. Yeni uygulama kullanıcısı için bir **Kullanıcı kimliği** ve **Kullanıcı adı** girin. Örneğin, "RecruitingIntegration" girebilirsiniz.

      > [!NOTE]
      > Uygulamada Microsoft Azure Active Directory (Azure AD) kullanıcı hesabı veya e-posta adresi yoksa, kullanıcı için e-posta adresi ve sağlayıcı alanlarına "RecruitingApp" benzeri bir şey girebilirsiniz.

  3. **Kullanıcı rolleri** hızlı sekmesinde, **Rol ata** eylemini seçin.
  4. **Kullanıcıya rol ata** bölmesinde, **İşe alma uygulaması** öğesini ve **Tamam**'ı seçin.
  5. Yeni kullanıcı kaydını kaydedin.

### <a name="link-the-new-human-resources-user-to-the-application"></a>Yeni Human Resources kullanıcısını uygulamaya bağlama

Kullanıcı oluşturulduktan sonra, uygulamayı Human Resources kullanıcısına bağlamak üzere uygulama için **Azure Active Directory Uygulamaları** formunda bir kayıt oluşturulmalıdır.

  1. **Azure Active Directory Uygulamaları** formunu açın **Yeni**'yi seçin.
  2. **İstemci kimliği** alanına, uygulama için oluşturulan uygulama kullanıcısının istemci kimliğini girin.
  3. **Ad** alanına tümleştirilen uygulamanın adını girin.
  4. **Kullanıcı kimliği** alanında, işe alma tümleştirmesi için oluşturulan yeni Human Resources kullanıcısını seçin.
  5. Yeni kaydı kaydedin.

Uygulama, yalnızca işe alım tümleştirmeleri için gerekli olan verilerle sınırlı olacak şekilde Human Resources verilerine erişime sahip olacaktır.

## <a name="see-also"></a>Ayrıca bkz.

[İş adaylarını işe alma](hr-personnel-recruit.md)<br>
[Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse Web API'sini kullanma](/powerapps/developer/data-platform/webapi/overview)<br>
[Web API'sini kullanarak seçenek kümeleri oluşturma ve güncelleştirme](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
