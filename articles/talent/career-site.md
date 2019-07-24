---
title: Attract'ta kariyer sitesi işlevi
description: Bu konu, Attract içinde adaya yönelik site işlevi hakkında genel bakış sağlar.
author: hasrivas
manager: AnnBe
ms.date: 03/20/2019
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
ms.author: hasrivas
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: e51fb00536884d2b3815c05a0968714d8b9326f2
ms.sourcegitcommit: a6b32be10b6eb6340f8f68261bf62d0202c03dd1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/05/2019
ms.locfileid: "1729715"
---
# <a name="career-site-functionality-in-attract"></a>Attract'ta kariyer sitesi işlevi

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Talent: Attract içinde adaya yönelik site işlevi hakkında genel bakış sağlar. Bu makale bu işlevselliği ayarlamayı açıklar.

Attract, kariyer sitesini bir kiracıdaki her bir ortamda sağlar. Örneğin, bir kuruluşta bir geliştirme ortamı ve test ortamı varsa, geliştirme ortamı için bir mesleki site ve test ortamı için başka bir site sağlanır. Mesleki her site tamamen ayrılmış ve kendi kimlik doğrulama mekanizması vardır. İşler ve aday profilleri mesleki siteler arasında paylaşılmaz.

Varsayılan olarak, mesleki site herkese açıktır. Bu nedenle, aday harici oturum açmadan işaretlenen tüm işleri görebilir. Bununla birlikte, tüm eylemler adayların oturum açmasını gerektirir.

## <a name="career-site-management"></a>Kariyer sitesi yönetimi

Aşağıdaki öğeler için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki (çark simgesi) **Yönetim Merkezi**'ni seçin ve **Şirket bilgileri** sekmesini seçin.

-   **Kuruluş adı** - Kuruluş adı, kariyer sitesinin üstündeki gezinti çubuğunda görünür. Aday kuruluş adını seçerek tüm açık iş listeleyen bir sayfaya gider.

-   **Kuruluş logosu** - Kuruluşun logo görüntüsü kariyer sitesinin sol üst köşesinde görünür. Aday logo görüntüsünü seçerek tüm açık iş listeleyen bir sayfaya gider.

    > [!NOTE] 
    > Kariyer sitesinde görüntülenen logo görüntüsünün, sabit 20 piksel (px) yüksekliği vardır. Yönetim merkezine eklediğiniz görüntü uyacak şekilde ölçeklendirilir. Bu nedenle, genişliği resme bağlı olarak değişebilir.
 
Aşağıdaki öğeler için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki **Yönetim Merkezi**'ni seçin ve **Kariyer sitesi yönetimi** sekmesini seçin.

-   **Arama Motoru Optimizasyonu** - Etkinleştirildiğinde, Attract kariyer sitesine gönderilen tüm ortak iş ilanları, Bing ve Google gibi arama motorları kullanılarak aranabilir olacaktır. 

    > [!NOTE] 
    > Bu ayarın etkinleştirilmesiyle, arama sonuçlarının görüntülenmesi arasında bir gecikme olabilir, kullandığınız arama motoruna bağlı olarak.
    
-   **Hüküm ve koşullar** - etkinleştirildiğinde, tüm adaylar, herhangi bir iş başvurusu yaparken kuruluşun hüküm ve koşullarını kabul etmek zorundadır. Attract yöneticisi, kendi Onay metnini ve ayrıca Hükün ve Koşullar sayfasına olan bağlantıyı yapılandırabilir. 

        
## <a name="career-site-urls"></a>Kariyer sitesi URL'leri

Aşağıdaki liste, sık kullanılan kariyer sitesi URL'leri ve bunlara nasıl erişileceğini içerir.

-   **Kariyer sitesi giriş sayfası URL'si** - Kariyeri sitesi giriş sayfası URL'sini görüntülemek için, Attract'e bir yönetici olarak oturum açın, **Ayarlar** menüsünde **Yönetici merkezi**'ni seçin ve sonra **Kariyer sitesi yönetimi** sekmesini seçin.

-   **Bireysel iş ilanı başvuru URL'si** - Siz ilk defa [bir harici iş ilanı verdiğinizde](Creating-jobs-Attract.md#postings), Attract uygulamasından **Uygula** bağlantısını kopyalayabilirsiniz. Bu bağlantı için URL aşağıdaki biçimde olacaktır: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)

-   **Bireysel iş ilanı URL'si** - İş ilanının URL'si, Başvur URL'sinin bir alt dizesidir. İş numarasına kadar her şeyden oluşur. Bu nedenle, öncedeki Başvur URL'si için iş ilanı URL'si [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e) olur

## <a name="authentication-options"></a>Kimlik doğrulama seçenekleri

Adayların Attract mesleki sitesi için seçenekleri şunlardır:

-   Kişisel hesap:

    -   LinkedIn

    -   Microsoft

    -   Google

    -   Facebook

-   İş veya okul hesabı:

    -   Microsoft Azure Active Directory (Azure AD)

Azure AD oturum açma, yalnızca dahili aday içindir. Bu nedenle, yalnızca Azure AD kimlik bilgilerini kullanan iç adaylar için çalışır. Örneğin, Contoso Ltd bir çalışanı olan bir aday, alakalı olmayan bir şirket olan Alpine Ski House'da bir işe başvurmak istiyor. Bu durumda, çalışan Contoso Ltd.'den kendi şirket Azure AD kimlik bilgilerini kullanmaya çalışırsa, başarısız olur. 

Adayların Azure AD kullanarak oturum açmaları gerekir, görüntüledikleri iş yalnızca dahili olarak listelenmişse.

## <a name="create-and-maintain-a-profile"></a>Profil oluştur ve sürdür

Mesleki siteye adaylar oturum açtıktan sonra profil oluşturmak ve kendi profilini güncelleştirmek için sayfanın üstündeki gezinme çubuğunda **Profilim**'i seçebilirsiniz.
Profil kişisel bilgileri, iş deneyimiyle ilgili bilgiler, eğitim ayrıntıları, belgeleri, bağlantıları ve beceri kümeleri hakkında bilgi içerir. Profil oluşturulduktan sonra adayın ilgilendiği işlere başvurmak için kullanılabilir. Profiller, Attract'a adaylar için doğru işlere önermesine yardımcı olur.

> [!NOTE]
> Aday kullanıyorsa, yukarıda listelenen e-posta kimliği için yetkilendirme sağlayıcılarını birini kullanarak oturum açın, profiliyle ilişkili ilgili kişi e-posta kodu, e-posta kodu varsayılan olur. Ancak, sonraki istenilen zaman değiştirilebilir ve ilkinden tümüyle bağımsızdır. Attract her zaman iletişim e-posta kimliğini, tüm e-posta iletişimleri için profilinizle ilişkilendirecektir.

## <a name="find-the-right-job"></a>Uygun işi bulun

İş listesi sayfasında, aday arama koşulları girerek belirli bir iş için arama yapabilir. Arama işlevselliği, iş başlığı ve açıklamada iş arama terimlerine bakar arar ve sonuçları ilgili işleri gösterir. Adaylar iş yeri veya işlevleri temel alarak herhangi bir anda sonuçları filtreleyebilir.

Adaylar kariyer sitesinde önerilen iş kümesini de görebilir. Aday için önerilen güncelleştirmelerin işleri adayın eski başvuruları, profili ve özgeçmiş üzerinde temel alır.

> [!NOTE] 
> İş önerileri mesleki sitede en az 10 iş varsa ve aday profilini tamamlarsa gösterilir.

Dahili adaylar bir işin işe alma yöneticisi/veya işvereninin kim olduğunu da görüntüleyebilirler, ekibin bu üyeleriyle iletişim kurmak istedikleri taktirde. Ancak, harici adayların, herhangi bir işin işe alım ekibinin üyelerini görme şansı yoktur.

## <a name="contact-the-hiring-team"></a>İşe alım takımıyla bağlantı kurun
Yalnızca dahili adaylar işe alım ekibiyle iletişime geçebilir. Bu sınırlama tüm işler için geçerlidir, yalnızca dahili veya halka açık olarak yayınlamış olduklarından bağımsız olarak.

Adaylar, gönderilen bir iş hakkında ilgi göstermek için işe alım ekibiyle iletişime geçebilir veya daha fazla bilgi isteyebilirler. Listelenen işe alım ekibi üyelerinden herhangi biriyle iletişime geçebilirler (işe alım yöneticisi veya işveren). İsteğe bağlı olarak iletiye bir özgeçmiş iliştirebilirler veya profillerinin bir parçası olarak önceden karşıya yüklemiş oldukları bir özgeçmişi seçebilirler.

Dahili bir aday, işe alım ekibi üyesini iletişim için seçtikten sonra, Attract bu kişilere adayın adına bir e-posta gönderir. Aynı zamanda, adayın profili **Aday** aşamasına eklenir, bu aşama iş için kullanılabiliyorsa. **Aday** aşaması altında, işverenler veya işe alım yöneticileri, onlarla iletişime geçen adayları görüntüleyebilirler. Ayrıca, aday profillerini görüntüleyebilir ve potansiyel adayları işe almak üzere davet edebilirler.

Adaylar, işe alım ekibi üyelerine halihazırda iletişime geçtikleri işlere başvurabilirler. Başvurduktan sonra, adaylar kariyer sitesi üzerinden ekip üyeleriyle iletişime geçemezler.

## <a name="apply-for-jobs"></a>İşlere başvur

Adaylar doğru işi bulduktan sonra, **İş ayrıntıları** sayfasında **Başvur** düğmesini kullanarak başvurabilirler. Bu aşamada adaylar yeni bir profil oluşturabilir veya varolan profillerindeki ilgili bilgileri gözden geçirin.
Adaylar gerekirse bir özgeçmiş ve sonra iş başvurusu gönderebilir.

### <a name="enable-applying-for-jobs-with-linkedin-profiles"></a>LinkedIn profilleriyle işe başvurmayı etkinleştir

Pozisyonlar için adayların başvurmasını Attract'in onlara LinkedIn aracılığıyla başvurmasına izin vererek kolaylaştırabilirsiniz.

> [!NOTE] 
> Adayların LinkedIn ile başvurmalarına olanak sağlamadan önce bir veya daha fazla LinkedIn işe alımcı lisansına sahip olmanız gerekir.

1. Attract'e bir yönetici olarak oturum açın.
2. **Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Yönetici merkezini** seçin.
3. **LinkedIn Tümleştirmesi** sekmesini seçin ve bir LinkedIn Recruiter hesabı ile bağlayın.
4. **LinkedIn Recruiter System Connect  Tümleştirmesi** bölümünde, **LinkedIn ile başvur** ayarı için **Etkin**'i seçin.

Ayarı etkinleştirdikten sonra, adaylar mevcut LinkedIn profil verilerini kullanarak başvurabilirler. Adaylar **LinkedIn ile başvur** düğmesini seçtiklerinde, halihazırda oturum açmamışlarsa, LinkedIn ile kimlik doğrulamaları istenir. Kimlik doğruladıktan sonra, LinkedIn profilleri, uygulama sayfasında gösterilen mevcut tüm profil verisini değiştirir. Adaylar, bilgiyi ihtiyaç duydukları şekilde düzenleyebilir ve başvuruyu gönderebilirler. Bir aday, işe başvurmadan sayfadan giderse, profil verileri Attract içinde güncelleştirilmez.

## <a name="check-application-status"></a>Başvuru durumunu kontrol edin

Adaylar bir veya daha fazla işe başvurduğunda, açık ve kapalı uygulamalarını görüntülemek için sayfanın üstündeki gezinme çubuğundaki **Başvurular**'ı seçebilir. Aday başvurularından birini açarken geçerli aşamayı ve tamamlaması gereken eylem öğelerini görür. Örneğin, bir adayın yüz yüze görüşme tarihlerini belirtmesi gerekiyorsa sayfada kullanılabilir seçenekleri gösterilir.

## <a name="internal-jobs"></a>Dahili işler

Şu anda, dahili olarak işaretlenen ve Attract kariyer sitesine gönderilmeyen işler kariyer sitesinde görünmez. Yalnızca Attract uygulamasından kopyalanabilecek doğrudan **Başvur** URL'sini kullanarak erişilebilirler.
