---
title: "Attract'ta kariyer sitesi işlevi"
description: "Bu makale Microsoft Dynamics 365 for Talent - Attract içerisindeki adaya yönelik kariyer sitesi özelliği hakkında genel bakış sağlar. Bu makale bu işlevselliği ayarlamayı açıklar."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: tr-tr
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Attract'ta kariyer sitesi işlevi

[!include [banner](includes/banner.md)]

Bu makale Microsoft Dynamics 365 for Talent: Attract içerisindeki adaya yönelik kariyer sitesi özelliği hakkında genel bakış sağlar. Bu makale bu işlevselliği ayarlamayı açıklar.

## <a name="overview"></a>Genel bakış

Attract, kariyer sitesini bir kiracıdaki her bir ortamda sağlar. Örneğin, bir kuruluşta bir geliştirme ortamı ve test ortamı varsa, geliştirme ortamı için bir mesleki site ve test ortamı için başka bir site sağlanır. Mesleki her site **tamamen ayrılmış** ve kendi kimlik doğrulama mekanizması vardır. İşler ve aday profilleri mesleki siteler arasında paylaşılmaz.

Varsayılan olarak, mesleki site herkese açıktır. Bu nedenle, aday harici oturum açmadan işaretlenen tüm işleri görebilir. Bununla birlikte, tüm eylemler adayların oturum açmasını gerektirir.

## <a name="career-site-management"></a>Kariyer sitesi yönetimi

Aşağıdaki öğeler mesleki sitede ayarlarla denetlenir:

- **Kuruluş adı:** Kuruluş adı, kariyer sitesinin üstündeki gezinti çubuğunda görünür. Aday kuruluş adını seçerek tüm açık iş listeleyen bir sayfaya gider.
- **Kuruluş logosu:** Kuruluşun logo görüntüsü kariyer sitesinin sol üst köşesinde görünür. Aday logo görüntüsünü seçerek tüm açık iş listeleyen bir sayfaya gider.

Kuruluş adı ve logosu için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki (çark simgesi) **Yönetim Merkezi**'ni seçin ve **şirket bilgileri** sekmesini seçin.

> [!NOTE]
> Kariyer sitesinde görüntülenen logo görüntüsünün, sabit 20 piksel (px) yüksekliği vardır. Yönetim merkezine eklediğiniz görüntü uyacak şekilde ölçeklendirilir. Bu nedenle, genişliği resme bağlı olarak değişebilir.

## <a name="career-site-url"></a>Kariyer sitesi URL'si

İlk defa [harici bir iş paylaştığınızda](./Creating-jobs-Attract.md#postings), Attract uygulamasından **Uygula** bağlantısını kopyalayabilirsiniz. Bu bağlantı URL'si şu biçimde olur:`https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Kariyer sitesinin URL'si bir **Uygula** URL'sinin alt dizesidir. Şirket adına kadar her şeyen oluşur. Bu nedenle, önceki **Uygula** URL'si için, kariyer site URL'si: `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Kimlik doğrulama seçenekleri

Adayların Attract mesleki sitesi için seçenekleri şunlardır:

- Kişisel hesap:

    - LinkedIn
    - Microsoft
    - Google
    - Facebook

- İş veya okul hesabı:

    - Microsoft Azure Active Directory (Azure AD)

Azure AD oturum açma, yalnızca dahili aday içindir. Bu nedenle, yalnızca Azure AD kimlik bilgilerini kullanan iç adaylar için çalışır. Örneğin, Contoso Ltd bir çalışanı olan bir aday, alakalı olmayan bir şirket olan Alpine Ski House'da bir işe başvurmak istiyor. Bu durumda, çalışan Contoso Ltd.'den kendi şirket Azure AD kimlik bilgilerini kullanmaya çalışırsa, başarısız olur.

## <a name="create-and-maintain-a-profile"></a>Profil oluştur ve sürdür

Mesleki siteye adaylar oturum açtıktan sonra profil oluşturmak ve kendi profilini güncelleştirmek için sayfanın üstündeki gezinme çubuğunda **Profilim**'i seçebilirsiniz. Profil kişisel bilgileri, iş deneyimiyle ilgili bilgiler, eğitim ayrıntıları, belgeleri, bağlantıları ve beceri kümeleri hakkında bilgi içerir. Profil oluşturulduktan sonra adayın ilgilendiği işlere başvurmak için kullanılabilir. Profiller, Attract'a adaylar için doğru işlere önermesine yardımcı olur.

## <a name="find-the-right-job"></a>Uygun işi bulun

İş listesi sayfasında, aday arama koşulları girerek belirli bir iş için arama yapabilir. Arama işlevselliği, iş başlığı ve açıklamada iş arama terimlerine bakar arar ve sonuçları ilgili işleri gösterir. Adaylar iş yeri veya işlevleri temel alarak herhangi bir anda sonuçları filtreleyebilir.

Adaylar kariyer sitesinde önerilen iş kümesini de görebilir. Aday için önerilen güncelleştirmelerin işleri adayın eski başvuruları, profili ve özgeçmiş üzerinde temel alır.

> [!NOTE]
> İş önerileri mesleki sitede en az 10 iş varsa ve aday profilini tamamlarsa gösterilir.

## <a name="apply-for-jobs"></a>İşlere başvur

Adaylar doğru işi bulduktan sonra, iş ayrıntıları sayfasında **Uygula** düğmesini kullanarak başvurabilirler. Bu aşamada adaylar yeni bir profil oluşturabilir veya varolan profillerindeki ilgili bilgileri gözden geçirin. Adaylar gerekirse bir özgeçmiş ve sonra iş başvurusu gönderebilir.

## <a name="check-application-status"></a>Başvuru durumunu kontrol edin

Adaylar bir veya daha fazla işe başvurduğunda, açık ve kapalı uygulamalarını görüntülemek için sayfanın üstündeki gezinme çubuğundaki **Başvurular**'ı seçebilir. Aday başvurularından birini açarken geçerli aşamayı ve tamamlaması gereken eylem öğelerini görür. Örneğin, bir adayın yüz yüze görüşme tarihlerini belirtmesi gerekiyorsa sayfada seçenekleri gösterilir.

## <a name="internal-jobs"></a>Dahili işler

Şu anda, dahili olarak işaretlenen ve Attract kariyer sitesine gönderilmeyen işler kariyer sitesinde görünmez. Yalnızca Attract başvurusundan koplayanabilen **Başvur** URL'siyle erişilebilir.

