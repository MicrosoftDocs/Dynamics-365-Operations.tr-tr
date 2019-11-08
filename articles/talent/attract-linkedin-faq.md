---
title: LinkedIn SSS ile Attract tümleştirme
description: Bu konu LinkedIn ile Microsoft Dynamics 365 Talent - Attract arasında tümleştirme konusunda karşılaşabileceğiniz sorulara yanıt verir.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: b77ad598ba209dbbd73765c49947e84a3995153d
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550379"
---
# <a name="attract-integration-with-linkedin-faq"></a>LinkedIn SSS ile Attract tümleştirme

[!include [banner](includes/banner.md)]

LinkedIn, dünyanın en büyük çevrimiçi uzman ağı. Microsoft Dynamics Talent: Attract, dünyadaki en üstün yeteneklere erişim sağlamak için LinkedIn ile tümleşir. Attract, işleri LinkedIn'e doğrudan nakletmenize ve aynı zamanda LinkedIn'den aday bilgiler çekmenize sağlar.

## <a name="for-recruiters-and-hiring-managers"></a>İşe alanlar ve işe alma yöneticileri için

Burada, Attract ve LinkedIn'in birlikte kullanımıyla ilgili sık sorulan soruların yanıtları bulunmaktadır.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Attract ile hangi LinkedIn özelliklerini edinebilirim?

LinkedIn ile yapılacak Attract tümleştirmesi aşağıdaki görevleri gerçekleştirmenize olanak tanır:

- [İşleri LinkedIn'e naklet](./attract-post-jobs-to-linkedin.md) (serbest sınırlı listeler olarak).
- [LinkedIn'den Attract aday bilgilerini dışa aktarın](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [İş adaylarınızın LinkedIn ile olan işleriniz için geçerli olmasına izin verin.](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>LinkedIn'e iş nakledebilmem için ne gerekir?

Yöneticiniz [Attract'ta LinkedIn tümleştirmesini konfigüre etmelidir](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Bundan sonra başlamaya hazırsınız.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Attract'tan LinkedIn'e iş yayınlamayı nasıl yaparım?

Attract'ta bir iş oluşturduktan sonra, yalnızca LinkedIn'e karşılık gelen **şimdi naklet** düğmesini seçmeniz gerekir. Daha fazla bilgi için, bkz. [Attract'tan LinkedIn'e iş yayınla](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>LinkedIn'den Attract'a aday bilgilerini nasıl alırım?

Evet. LinkedIn'de iyi bir aday görüyorsanız, bu adayın bilgilerini Attract'a kolayca dışa aktarabilirsiniz. Daha fazla bilgi için bkz. [LinkedIn Recruiter ile kaynak bulma](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Attract'tan LinkedIn'e erişmeye nasıl yardım alabilirim?

Attract'tan işleri LinkedIn'de yayınlarken ya da oturum açarken sorunla karşılaşıyorsanız, bkz. [LinkedIn ile sorun giderme entegrasyonu](./attract-troubleshoot-linkedin.md).

Attract'la ilgili diğer sorunlar için, bkz. [Talent desteği al](./talent-support.md). LinkedIn ile ilgili yardım için [LinkedIn desteği sayfasına](https://www.linkedin.com/help) bakın.

## <a name="for-admins-and-developers"></a>Yöneticiler ve geliştiriciler için

Burada, Attract ve LinkedIn'in arasında entegrasyon yapılandırmasıyla ilgili sık sorulan soruların yanıtları bulunmaktadır.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>İş verenlerin ve işe alma yöneticilerinin işleri LinkedIn'e nakledebilmesi için nasıl Attract'i yapılandırabilirim?

Her iki seçeneği de Yönetim Merkezi'ndeki **LinkedIn Entegrasyonu** sekmesinde konfigüre edebilirsiniz. Daha fazla bilgi için bkz [LinkedIn ile entegrasyon kurma](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>LinkedIn'den aday bilgilerini dışa aktarabilir miyim?

Evet, ancak öncelikle LinkedIn Recruiter ile tümleştirmeyi konfigüre etmelisiniz. Daha fazla bilgi için bkz [LinkedIn ile entegrasyon kurma](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>İşleri LinkedIn'deki Premium İş yuvalarına nasıl nakledebilirim?

Attract, işleri LinkedIn'e nakletmek için güçlü bir çözüm sağlasa da, ek esneklik gerektiğini fark edebilirsiniz. Örneğin, uygun olan sınırlı listelere ek olarak Premium İş yuvalarını deftere nakledebilmek ya da LinkedIn'in toplu iş gönderilerinizi günde bir kereden fazla işlemesini isteyebilirsiniz.

#### <a name="types-of-linkedin-job-posts"></a>LinkedIn iş nakil türleri

LinkedIn, aşağıdaki proje nakil türleri sunar:

- **Sınırlı Liste** – Adaylar LinkedIn'de ve şirketin LinkedIn sayfasında iş aradığında arama sonuçlarında görünen ücretsiz iş nakilleri. Sınırlı Listeler, etkin iş arayanlara yöneliktir. Bu tür bir liste, Attract tarafından LinkedIn'e sağlanan türdür. LinkedIn'de sınırlı listeleme işlerini yükseltemiyorsunuz. Sınırlı Listeleri yükseltmek istiyorsanız, İş kaydırmayı etkinleştirmek için LinkedIn ile çalışmanız gerekir. İş kaydırma hakkında daha fazla bilgi için bkz. [İş Kaydırma İçin Sınırlı Listeler ve Premium İş Yuvaları](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) ve [İş kaydırma ile ilgili SSS](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Özel İş Yuvası**: , LinkedIn akışı, e-postalar ve alan **ilgilenebileceğiniz işler** gibi LinkedIn'de çeşitli yerlerde görünen satın alınan nakiller. Premium İş Yuvaları pasif adaylar için hedeflenir, ancak bunlar iş aramalarında da yer alıyor.

Attract işleri LinkedIn'e nakleder (serbest sınırlı listeler olarak). Premium İş Yuvalarını kullanmak istiyorsanız, İş kaydırmayı LinkedIn Recruiter ile kullanmalısınız. İş Kaydırma, LinkedIn ile bir iş kaydırma sözleşmesi gerektirir. Daha fazla bilgi için bkz. [LinkedIn Recruiter ile İş Kaydırma - Genel Bakış](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>LinkedIn'de toplu iş işlemenin sıklığı

LinkedIn, bir toplu işteki iş yayınlarını her gün bir kez Attract ile işler. Bu nedenle, işlerin, Attract ile nakledildikten sonra LinkedIn'de görünmesi 48 saate kadar sürebilir. İşlerin LinkedIn'de daha erken görüntülenmesi gerekiyorsa veya herhangi bir ek esneklik gerekiyorsa, Recruiter System Connect uygulama programlama arabirimini (API) LinkedIn'den kullanabilirsiniz. Daha fazla bilgi için bkz. [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect)

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>LinkedIn'e iş nakli için seçenekler tablosu

Aşağıdaki tabloda, projelerin LinkedIn'e nakledilmesi ile ilgili farklı seçenekler açıklanmıştır. Her seçeneğin ve ek bilgilerin avantajlarını içerir.

|  | Attract | LinkedIn Recruiter ile iş kaydırma | Recruiter System Connect API |
|---|---|---|---|
| **Açıklama** | Attract işleri LinkedIn'e nakleder (XML akışı olarak). | Şirket LinkedIn ile sözleşme yapar ve işleri nakletmek için bir XML akışı sağlar. | Müşteri, Attract ile LinkedIn Recruiter arasında bilgileri eşitlemek için API kullanır. |
| **Ne tür bir iş nakledebilirim?** | Sınırlı Listeleme | Premium İş Yuvası veya Sınırlı Listeleme | Sınırlı Listeleme |
| **LinkedIn'de işi yükseltebilir miyim?** | Hayır | Premium İş Yuvaları: Evet<br>Sınırlı Listeleme: Hayır | Hayır |
| **LinkedIn'in işleri deftere nakil sıklığı nedir?** | Günde bir | Günde bir | API tarafından tanımlanan, günlük birden çok kez |
| **LinkedIn tarafından önerilsin mi?** | Hayır | Evet | Hayır |
| **Bana ne gerekir?** | Attract Satın alma | LinkedIn ilw iş kaydırma sözleşmesi ve Premium İş yuvalarını satın alma | LinkedIn ile bir API sözleşmesi | 
| **Nerede daha fazla bilgi bulabilirim?** | [LinkedIn ile tümleştirmeyi ayarlama](./attract-admin-linkedin.md) | [LinkedIn Recruiter ile iş kaydırma - Genel Bakış](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Attract ile LinkedIn'e iş nakletmek için LinkedIn Recruiter System Connect lisansına gerek yoktur.

## <a name="see-also"></a>Ayrıca bkz.

[LinkedIn ile tümleştirmeyi ayarlama](./attract-admin-linkedin.md)

[Attract'tan LinkedIn'e iş yayınlama](./attract-post-jobs-to-linkedin.md)

[LinkedIn Recruiter ile aday kaynağı bulma](./attract-linkedin-recruiter.md)

[LinkedIn ile tümleştirme sorun giderme](./attract-troubleshoot-linkedin.md)
