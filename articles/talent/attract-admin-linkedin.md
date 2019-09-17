---
title: Microsoft Dynamics 365 for Talent - Attract için LinkedIn ile tümleştirmeyi ayarlama
description: Bu konu, Microsoft Dynamics 365 for Talent - Attract'a yönelik LinkedIn tümleştirmesinin nasıl yapılandırılacağını açıklar ve böylece Attract'ten işleri LinkedIn'e kolayca nakledebilir ve iş verenlerin, işe alma bilgilerini bir adayın LinkedIn profiliyle eşitleyebilmesini sağlayabilirsiniz.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8e42ec7d0bb74089b4e915b5a30277401e694cf9
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756234"
---
# <a name="set-up-linkedin-integration"></a>LinkedIn tümleştirmesini ayarlama

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract ile LinkedIn tümleşmesini yapılandırarak iş verenlerinizin ve işe alma yöneticilerinizin dikkatini çekmenize yardımcı olun. Attract, işleri en büyük profesyonel çevrimiçi ağ olan LinkedIn'e doğrudan nakletmenize olanak tanır.

Attract aracılığıyla LinkedIn'e naklettiğiniz işler Sınırlı Listelerdir ve şirketinize yönelik ek bir maliyet olmadan sağlanır. Bu listelemeler yalnızca, Attract gibi LinkedIn yazılım ortakları aracılığıyla kullanılabilir. Şirketin LinkedIn sayfasındaki **kariyer** panelinde görünmezler, yalnızca ücretli listelerin orada göründüğü için bunlar burada görünmez. Ancak, olası adaylar tüm kullanılabilir işleri görüntülerken görüntülenir. Sınırlı Listelemeler LinkedIn iş aramalarında da gösterilir.

Attract, bu popüler kariyer sitesinden adaylarla birleşmenize yardımcı olacak LinkedIn ile bütünleşmenin iki yolunu sağlar:

- Attract'tan LinkedIn'e iş yayınlayın.
- LinkedIn'den Attract'e aday arayın.

Her iki seçeneği de Yönetim Merkezi'ndeki **LinkedIn Entegrasyonu** sekmesinde konfigüre edebilirsiniz. Yönetici merkezini açmak için <https://attract.talent.dynamics.com/adminsettings> adresine gidin.

> [!NOTE]
> [Kapsamlı işe alma eklentisi](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) ve  [LinkedIn Recruiter lisans sayısı](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18), Attract ile LinkedIn Recruiter kullanabilmek için gereklidir. Daha fazla bilgi için bkz. [hangi Attract sürümü?](./attract-comprehensive-hiring.md).

İşleri LinkedIn'de yayınlarken sorunla karşılaşıyorsanız, bkz. [LinkedIn ile sorun giderme entegrasyonu](./attract-troubleshoot-linkedin.md).

İşleri LinkedIn'e nakletmenin diğer yolları hakkında bilgi için, [LinkedIn'de SSS](./attract-linkedin-faq.md) bölümüne bakın.

## <a name="configure-job-posting-to-linkedin"></a>LinkedIn'de iş yayınlamayı konfigüre et

Attract'ten LinkedIn'e iş nakledebilmek için [LinkedIn Şirket Kimliğine](https://aka.ms/findID) ihtiyacınız vardır. LinkedIn Şirket Kimlik Kodu, şirketinizi LinkedIn içinde benzersiz şekilde tanımlayan bir dizi sayıdır. Daha fazla bilgi için bkz. [LinkedIn Şirket Kimliğinizle LinkedIn İş Panosunu İlişkilendirme - sık sorulan sorular](https://aka.ms/findID).

Attract iş nakillerinizin bir akışını LinkedIn'e gönderir ve LinkedIn'e günde yaklaşık olarak bir kez bakar. İşlerinizin siteye nakledilmesi 48 saate kadar sürebilir.

LinkedIn'e verilen iş ilanları LinkedIn sitesinde yayınlanır. LinkedIn'e iş ilanı vermek için test ortamı yoktur. Bu nedenle, yanlışlıkla hiçbir test işini deftere nakletmemenize dikkat edin. 

1. Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici merkezi**'ni seçin. Alternatif olarak, <https://attract.talent.dynamics.com/adminsettings>'e gidin.
2. **LinkedIn Tümleştirme** sekmesini seçin.
3. **Şirket adı** altında, şirketinizin adını ve **şirket kodu** altından LinkedIn Şirket kodunu girin. Şirket adının şirketinizin LinkedIn sayfasında görünen adla eşleştiğinden emin olun. LinkedIn Şirket kimlikleri için daha fazla bilgi için bkz. [LinkedIn Şirket Kimliğinizle LinkedIn İş Panosunu İlişkilendirme - sık sorulan sorular](https://www.linkedin.com/help/linkedin/answer/98972).

    Kuruluşunuzla ilgili bilgileri değiştirmeniz gerekiyorsa, bkz. [Kuruluşunuzun adresini, teknik ilgili kişiyi ve daha fazlasını değiştirin](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Sorunlarınız devam ediyorsa [LinkedIn desteğine](https://www.linkedin.com/help/linkedin) başvurun.

4. **Kaydet**'i seçin.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Attract ile LinkedIn Recruiter ayarlamak 

İş verenlerin LinkedIn Recruiter üzerinden işe almasına izin vermek için, Attract'te tümleştirme LinkedIn Recruiter konfigüre etmelisiniz. Yapılandırma işlemini tamamlamak için kurumunuzun LinkedIn Recruiter sözleşmenizden yönetici olan kullanıcıyla çalışmanız gerekir.

1. Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici merkezi**'ni seçin. Alternatif olarak, <https://attract.talent.dynamics.com/adminsettings>'e gidin.
2. **LinkedIn Tümleştirme** sekmesini seçin.

    [![LinkedIn Recruiter tümleştirme başlatmak için Attract yönetici görünümü](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Kurulumu başlatmak için **Bağlan**'ı seçin. LinkedIn oturum açma işlemi boyunca size kılavuzluk edilecek.
4. Birde çok LinkedIn sözleşmelerinde lisansınız varsa, Attract sistemine bağlanmak istediğiniz sözleşmeyi seçin. LinkedIn sözleşmesinde tek bir lisans varsa, bu adım gerekli değildir.
5. **Recruiter System Connect (RSC)** altında **Talep**e tıklayın.

    [![LinkedIn Recruiter tümleştirme talebi başlatmak için Attract yönetici görünümü](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. **Recruiter System Connect (RSC)** ayarı şimdi **Ortağa hazır** olarak görünmelidir. Bu sayfada **Ortağa bildir** görürseniz birkaç saniye bekleyin, **Ortağa bildir**i seçin ve sayfayı yenileyin. Ayar  **Ortağa hazır**olarak görünmelidir.

    [![İsteklerin Attract tarafının tamamlandığını belirten Attract Yönetici görünümü](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Sonraki adımı tamamlamak için LinkedIn Recruiter Sözleşmenizde bir yönetici ayrıcalığı olması gerekir.

    1. Yönetim hesabınızı kullanarak LinkedIn'de oturum açın ve sağ üst tarafta **LinkedIn Recruiter** seçin. 
    2. Sayfanın üstündeki **Daha fazla** menüsünde **Yönetici ayarları**ve ardından **ATS** sekmesini seçin.
    3. Tek tıklamayla tek bir sözleşme için dışa aktarmayı etkinleştirmek üzere **sözleşme düzeyi erişimi**ni etkinleştirin (Bu sözleşmedeki her bilgisayar için). Tüm şirket için bunu etkinleştirmek amacıyla **şirket düzeyinde erişimi etkinleştirin (şirketinizdekiher sözleşme için)**.

    [![LinkedIn Recruiter Yönetici görünümünden Attract tümleştirmeyi aç](./media/EnableRSC.png)](./media/EnableRSC.png)

8. Attract Yönetici Merkezinde, **LinkedIn entegrasyonu** sekmesini seçin. **Recruiter System Connect (RSC)** ayarı şimdi **etkin** olarak görünmelidir.

    [![LinkedIn Recruiter tümleştirme tamamlandı](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Attract'te LinkedIn ile Uygulamayı ayarlayın

Adayların LinkedIn profillerini kullanarak işleriniz için geçerli olmasına izin verebilirsiniz. LinkedIn ile uygulama hakkında daha fazla bilgi için, [LinkedIn'in gücünü her yerde görün: LinkedIn ile uygulayın](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Bu özellik şu anda önizlemededir. Bu adımları izlemeden önce, LinkedIn ile uygulamanın etkinleştirildiğinden emin olun. Önizleme özelliklerini etkinleştirmek hakkında daha fazla bilgi için bkz. [Talent içinde önizleme özelliklerine erişim](./access-preview-feature.md).

1. Sağ üst köşedeki **Kurulum** menüsünden (çark simgesi) **Yönetici merkezi**'ni seçin. Alternatif olarak, <https://attract.talent.dynamics.com/adminsettings>'e gidin.
2. **LinkedIn Tümleştirme** sekmesini seçin.

    [![LinkedIn Recruiter tümleştirme başlatmak için Attract yönetici görünümü](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. **LinkedIn ile uygulamak** için, **Bağlan**'ı seçerek kurulumu başlatın. LinkedIn ile işlem boyunca size kılavuzluk edilecek.

## <a name="see-also"></a>Ayrıca bkz.

[LinkedIn SSS](./attract-linkedin-faq.md)

[Attract'tan harici sitelere iş yayımlama](./posting-jobs-external.md)

[LinkedIn Recruiter ile aday kaynağı bulma](./attract-linkedin-recruiter.md)

[İşler oluşturma](./creating-jobs-attract.md)

[LinkedIn ile tümleştirme sorun giderme](./attract-troubleshoot-linkedin.md)
