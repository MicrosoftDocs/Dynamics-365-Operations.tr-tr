---
title: "LinkedIn İşveren ile kaynak bulma"
description: "Bu konu, iş ve iş adayı önerileri almak için makine öğrenimini kullanma hakkında bilgi sağlar."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: tr-tr
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>LinkedIn İşveren ile kaynak bulma
[!include[banner](../includes/banner.md)]

LinkedIn, dünyanın en büyük beceri veritabanı ve çoğu zaman işe alanların doldurmak istediği işler için kaynak adaylar bulmak, adaylarla iletişim kurmak için kullandığı birincil sistemdir. LinkedIn İşveren'in Dynamics 365 for Talent: Attract ile entegrasyonu, kullanıcıların işe alımını ve verileri iki sistem arasında eşit tutmayı kolaylaştırır.

> [!NOTE]
> Kapsamlı işe alma eklentisi ve LinkedIn İşveren lisans sayısı, Attract ile LinkedIn İşveren kullanabilmek için gereklidir.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Attract ile LinkedIn İşveren ayarlayın 

LinkedIn İşveren özellikleri kullanabilmek için önce Attract örneğinizle sözleşme düzeyi veya şirket düzeyinde erişim yapılandırmanız gerekir. Yapılandırma işlemini tamamlamak için LinkedIn İşveren sözleşmenizden yönetici olan kullanıcıyla çalışmanız gerekir. Attract ile LinkedIn İşveren konfigüre etmek için aşağıdaki adımları izleyin.

1.  Bir yönetici olarak Attract oturumu açın ve  **Yönetici Ayarları**na gidin.

2.  Sol bölmedeki **LinkedIn Entegrasyonu** sekmesine tıklatın.

[![LinkedIn İşveren tümleştirme başlatmak için Attract yönetici görünümü](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  **Bağlan**a tıklayın, kurulumu başlatın, LinkedIn oturum açma işleminde kılavuzluk alın.

4.  Birde çok LinkedIn sözleşmelerinde lisansınız varsa, Attract sistemine bağlanmak istediğiniz sözleşmeyi seçin. LinkedIn sözleşmesinde tek bir lisans varsa, bu adım gerekli değildir.

5.  LinkedIn pencere öğesi gösterilen tümleştirmelerin listesiyle, Yönetici ayarlarını şimdi yükler. **Recruiter System connect** altında **Talep**e tıklayın.

[![LinkedIn İşveren tümleştirme istemek için Attract yönetici görünümü](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Attract'tan tümleştirme istedikten sonra **Ortak hazır** olarak gösterilir ve **İşveren Yönetici ayarları**ndan açmaya hazır olur. Bu sayfada **Ortağa bildir** görürseniz birkaç saniye bekleyin, **Ortağa bildir**e tıklayın ve sayfayı yenileyin. Şimdi **Ortak hazır** olarak görünür.

[![İsteklerin Attract tarafının tamamlandığını belirten Attract Yönetici görünümü](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Sonraki adımı tamamlamak için LinkedIn İşveren Sözleşmenizde bir Yönetici ayrıcalığı olması gerekir.

7.  LinkedIn için yönetici hesabı kullanarak oturum açın ve sağ üstteki İşveren LinkedIn gidin. 

8. Ekranın üstündeki **Daha fazla** menüsünde **Yönetici ayarları**ve ardından **ATS** sekmesine tıklayın.

Attract sistem açılabilir birkaç seçenekle listede görüntülenir.

9. Dışa aktarmak için yalnızca 1 tıklamayı etkinleştirmek isterseniz, **ATS göstergesinde** ve **ATS profil pencere öğesi**nde, **Şirket düzeyinde erişim**i seçin. Tüm şirket düzeyinde erişim özelliklerini artı InMail geçmişi, Not geçmişi ve InMail saplama profil erişimi etkinleştirmek isterseniz, **sözleşme düzeyi erişim**i seçin.

10. LinkedIn İşveren**Yönetici-ATS** ayarlarından istediğiniz erişim düzeyini açın.

[![LinkedIn İşveren Yönetici görünümünden Attract tümleştirmeyi aç](./media/EnableRSC.png)](./media/EnableRSC.png)

12. AttractAdmin olarak Attract Yönetici ayarlarına dönün ve**LinkedIn tümleştirme** sekmesini seçin. LinkedIn pencere öğesi yüklemesini, seçilen erişim düzeyi açık olarak **Etkin** şeklinde görmeniz gerkeir.

[![LinkedIn İşveren tümleştirme tamamlandı](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>LinkedIn İşvren özelliklerini kullanma

LinkedIn İşveren özellikleri Attract Yönetici tarafından etkinleştirildiğinde iş alın yöneticileri ve işverenlerin erişimine açık olur. LinkedIn hesabınızı bu özellikleri kullanmak için **kullanıcı ayarları** altından bağlayın. Hem yönetici hem de kullanıcı ayarları bağlandıktan sonra birkaç özellik kullanılabilir olacaktır.

### <a name="in-ats-profile-widget"></a>ATS profil pencere öğesi

Adayın LinkedIn profilini Attract içinde görebilirsiniz. LinkedIn pencere öğesi, LinkedIn kullanıcı bilgileri ATS bilgileriyle eşleştiğinde aday profili görüntüler.

Profil görüntülemek için aday profiline işten veya beceri havuzundan gidin. Aday profilinde **LinkedIn** sekmesini seçin ve profil pencere öğesi yüklenir. Profil pencere öğesini kullanarak doğru eşleşme olup olmadığını gösterin. Değilse doğru kişiyi bulun. Bu sayfadan LinkedIn İşveren projelerinize aday da kaydedebilirsiniz.

### <a name="1-click-export"></a>1 tıkla dışa aktarma 

LinkedIn'de aday kaynağı bulurken a.ık olan işlere 1 tıklamayla aday dışa aktarımı yapabilirsiniz. 1 tıkla dışa aktarma için aşağıdaki adımları tamamlayın. Aşağıdaki adımları tamamlamadan önce iş için işe alma yöneticisi veya İşveren atanmış ve işin **Aday müşteri** aşaması olduğundan emin olun

1.  İş oluşturun, uygun roller atayın ve işi etkinleştirin.

2.  İş etkinleştirildiğinde LinkedIn İşveren'e ilerleyin.

3.  Aradığınız adayı bulun ve profiline gidin.

4.  Kişi kartında iş arama kutusunu kullanıp iş başlığı veya Attract'ta etkinleştirilmiş İş Kodu kullanarak işi bulun. İş bulamazsanız, **ATS değişikliği**ne tıklayarak doğru Attract örneği bulun.

5. İş seçtikten sonra **dışa aktar**a tıklayın. Aday Attract tarafından getirilir.

6.  Attract'a gidin ve ilgili işi açın. İşin **Aday müşteri** aşamasında dışa aktardığınız adayı bulursunuz.

### <a name="in-ats-indicator"></a>ATS göstergesinde 

LinkedIn İşveren kullanarak, adayın kuruluşunuzdaki diğer işlere başvurup başvurmadığını izler, iş başvurularının hangi aşamalarında olduklarına bakabilir ve LinkedIn İşveren'de Attract'tan gelen geri bildirimlerle yorumları görüntüleyebilirsiniz.

1.  LinkedIn İşvere'i açın ve aradığınız aday profilini bulun.

2.  Adayın profilinde **ATS'de** bölümünü açmak için aşağı kaydırın.

3.  Bu pencere öğesini, LinkedIn İşveren görünümündeki Attract'ta mevcut olan aday hakkındaki bilgileri görüntülemek için kullanabilirsiniz.

4.  **İşler ve durumlarını** seçerek parçası oldukları işleri, son durumu ve her işte nasıl ilerlediklerini görün.

5.  **görüşme geribildirimi** sekmesini seçerek görüşmecilerin Attract'a gönderdiği geri bildirimleri görün.

6.  **Notlar** sekmesini seçerek Attract'ta bu başvuran için yakalanan notları görün.

### <a name="inmail-history"></a>InMail geçmişi

LinkedIn InMail geçmişi, LinkedIn İşveren'le sözleşme düzeyinde erişimle kullanılabilir. Etkin olduğunda, adayla olan tüm InMail geçmişi görebilirsiniz. Adayla InMail değişimi yapan kuruluşunuzdan diğer kullanıcıları görebilir ancak aralarındaki mesajları göremezsiniz.

InMail geçmişini görüntülemek için adayın profiline gidin. **LinkedIn** sekmesine gidin ve geçmişini görüntülemek için aşağı aydırma yapın. Yalnızca aday isteğinize yanıt verdiyse ve profilini LinkedIn'de paylaşmayı seçtiyse InMail geçmişini görüntüleyebilirsiniz. Her birkaç saatte bir InMail gelen iletileri Attract ile eşitlenir.

### <a name="notes-history"></a>Notlar geçmişi 

LinkedIn notlar geçmişi, LinkedIn İşveren'le sözleşme düzeyinde erişimle kullanılabilir. Etkinleştirildiğinde, aday hakkında kurumunuzda farklı işverenler tarafından yakalanan notları görebilirsiniz.

Notlar geçmişini görüntülemek için adayın profiline gidin. **LinkedIn** sekmesine gidin ve geçmişini görüntülemek için aşağı aydırma yapın. LinkedIn İşveren'den aday hakkındaki tüm notları görüntüleyebilirsiniz.

### <a name="inmail-stub-profile"></a>InMail saplama profili

InMail saplama profili, LinkedIn İşveren'le sözleşme düzeyinde erişimle kullanılabilir. Adaylar kuruluşunuzdaki herhangi bir kullanıcıyla LinkedIn profillerini paylaşmayı kabul ederse, adayları Attract'ta takip edebilir ve her aday için yeni bir aday kaydı oluşturulur.

Aday listesini görüntülemek için **Beceri havuzları**na gidin, sistem tarafından oluşturulan LinkedIn beceri havuzunu görün. Bu beceri havuzu, LinkedIn'den alınan aday ve alt profilleri listesini içerir. Adayın adını ve soyadını gösterir. Adayın e-posta kodu, aday e-posta adresini paylaşmayı seçtiyse görüntülenir.

