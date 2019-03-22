---
title: Attract'ta kariyer sitesi işlevi
description: Bu konu, Attract içinde adaya yönelik site işlevi hakkında genel bakış sağlar.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/13/2019
ms.locfileid: "389990"
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

    >   [!NOTE] 
    >   Kariyer sitesinde görüntülenen logo görüntüsünün, sabit 20 piksel (px) yüksekliği vardır. Yönetim merkezine eklediğiniz görüntü uyacak şekilde ölçeklendirilir. Bu nedenle, genişliği resme bağlı olarak değişebilir.
 
Aşağıdaki öğeler için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki **Yönetim Merkezi**'ni seçin ve **Kariyer sitesi yönetimi** sekmesini seçin.

-   **Arama Motoru Optimizasyonu** - Etkinleştirildiğinde, Attract kariyer sitesine gönderilen tüm ortak iş ilanları, Bing ve Google gibi arama motorları kullanılarak aranabilir olacaktır.

    >   [!NOTE] 
    >   Bu ayarın etkinleştirilmesiyle, arama sonuçlarının görüntülenmesi arasında bir gecikme olabilir, kullandığınız arama motoruna bağlı olarak.
         
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

## <a name="create-and-maintain-a-profile"></a>Profil oluştur ve sürdür

Mesleki siteye adaylar oturum açtıktan sonra profil oluşturmak ve kendi profilini güncelleştirmek için sayfanın üstündeki gezinme çubuğunda **Profilim**'i seçebilirsiniz.
Profil kişisel bilgileri, iş deneyimiyle ilgili bilgiler, eğitim ayrıntıları, belgeleri, bağlantıları ve beceri kümeleri hakkında bilgi içerir. Profil oluşturulduktan sonra adayın ilgilendiği işlere başvurmak için kullanılabilir. Profiller, Attract'a adaylar için doğru işlere önermesine yardımcı olur.

>   [!NOTE]
>   Aday kullanıyorsa, yukarıda listelenen e-posta kimliği için yetkilendirme sağlayıcılarını birini kullanarak oturum açın, profiliyle ilişkili ilgili kişi e-posta kodu, e-posta kodu varsayılan olur. Ancak, sonraki istenilen zaman değiştirilebilir ve ilkinden tümüyle bağımsızdır. Attract her zaman iletişim e-posta kimliğini, tüm e-posta iletişimleri için profilinizle ilişkilendirecektir.

## <a name="find-the-right-job"></a>Uygun işi bulun

İş listesi sayfasında, aday arama koşulları girerek belirli bir iş için arama yapabilir. Arama işlevselliği, iş başlığı ve açıklamada iş arama terimlerine bakar arar ve sonuçları ilgili işleri gösterir. Adaylar iş yeri veya işlevleri temel alarak herhangi bir anda sonuçları filtreleyebilir.

Adaylar kariyer sitesinde önerilen iş kümesini de görebilir. Aday için önerilen güncelleştirmelerin işleri adayın eski başvuruları, profili ve özgeçmiş üzerinde temel alır.

>   [!NOTE] 
>   İş önerileri mesleki sitede en az 10 iş varsa ve aday profilini tamamlarsa gösterilir.

## <a name="apply-for-jobs"></a>İşlere başvur

Adaylar doğru işi bulduktan sonra, **İş ayrıntıları** sayfasında **Uygula** düğmesini kullanarak başvurabilirler. Bu aşamada adaylar yeni bir profil oluşturabilir veya varolan profillerindeki ilgili bilgileri gözden geçirin.
Adaylar gerekirse bir özgeçmiş ve sonra iş başvurusu gönderebilir.

## <a name="check-application-status"></a>Başvuru durumunu kontrol edin

Adaylar bir veya daha fazla işe başvurduğunda, açık ve kapalı uygulamalarını görüntülemek için sayfanın üstündeki gezinme çubuğundaki **Başvurular**'ı seçebilir. Aday başvurularından birini açarken geçerli aşamayı ve tamamlaması gereken eylem öğelerini görür. Örneğin, bir adayın yüz yüze görüşme tarihlerini belirtmesi gerekiyorsa sayfada kullanılabilir seçenekleri gösterilir.

## <a name="internal-jobs"></a>Dahili işler

Şu anda, dahili olarak işaretlenen ve Attract kariyer sitesine gönderilmeyen işler kariyer sitesinde görünmez. Yalnızca Attract uygulamasından kopyalanabilecek doğrudan **Başvur** URL'sini kullanarak erişilebilirler.
