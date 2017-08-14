---
title: "Mobil çalışma alanında gider yönetimi"
description: "Bu konu, Gider yönetimi mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı kullanıcıların bir girişi yakalamasını ve yüklemesini, böylece daha sonra bir gider raporuna ekleyebilmelerini sağlar. Kullanıcılar ayrıca ekli bir alış irsaliyesi kullanarak bir gider satırını hızla oluşturabilir ve gider raporlarını oluşturup yönetebilirler."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: 2dd3db95eb741c37dd8a50c397cb4c9494599250
ms.openlocfilehash: 993586b1fb46c21d2b68a6060ab897c8ccc76a6c
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanı

[!include[banner](../includes/banner.md)]

Bu konu, **Gider yönetimi** mobil çalışma alanı hakkında bilgi sağlar. Bu çalışma alanı kullanıcıların bir girişi yakalamasını ve yüklemesini, böylece daha sonra bir gider raporuna ekleyebilmelerini sağlar. Kullanıcılar ayrıca ekli bir alış irsaliyesi kullanarak bir gider satırını hızla oluşturabilir ve gider raporlarını oluşturup yönetebilirler. Ek olarak, onaylayıcılar **Gider yönetimi** mobil çalışma alanını, onlara atanmış gider raporlarını görüntülemek ve bu gider raporlarını onaylamak veya reddetmek için kullanabilirler.


Bu mobil çalışma alanı, Microsoft Dynamics 365 for Unified Operations mobil uygulaması ile kullanılmak üzere geliştirilmiştir.


## <a name="overview"></a>Özet

Çoğu kuruluş, personelin iade için gönderdiği bir seyahatle ya da işle ilgili gider raporuna, bir fişin kopyasının eklenmesini gerektirir. **Gider yönetimi** mobil çalışma alanı, kullanıcıların yeni gider satırlarını, fişin fotoğrafını ekleyerek istedikleri mobil cihazda hızla oluşturmalarını sağlar. Alternatif olarak, kullanıcılar fişin fotoğrafını çekebilir ve gider raporuna daha sonra ekleyebilirler. Personeller de gider raporlarını oluşturabilir ve yönetebilirler, ayrıca bunları daha sonra onaylanmak ve para iadesi almak üzere mobil cihazlarını kullanarak gönderebilirler.


Özellikle, **Gider yönetimi** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:

- Fişin bir fotoğrafını çekmek ve Microsoft Dynamics 365 for Finance and Operations Enterprise edition'a yüklemek. Daha sonra fotoğrafı bir gider raporuna ekleyebilirsiniz.
- Dosyayı kaydedilen bir giriş olarak yüklemek. Daha sonra dosyayı bir gider raporuna daha sonra ekleyebilirsiniz.
- Ekli bir fişi kullanarak yeni bir gider satırı oluşturmak. Satır maddesini bir gider raporuna daha sonra ekleyebilir ve onay ve iade için gönderebilirsiniz.

Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü Temmuz 2017 güncelleştirmesini kullanıyorsanız, aşağıdaki özelliklerden de faydalanabilirsiniz:

- Yeni gider raporu oluştur.
- Kredi kartı hareketlerini ve önceden oluşturulmuş diğer giderleri bir gider raporuna ekleyin.
- Bir gider raporu için yeni bir giderler oluşturun.
- Bir girişi herhangi bir gider raporu için bir gidere ekleyebilirsiniz; ister fişin fotoğrafını çekerek, isterseniz de bir dosyayı yakalanan bir fiş olarak karşıya yükleyerek.
- Şirketin gider ilkelerine dayalı olarak, bir gidere konukların listesini ekleyin.
- Şirketin gider ilkesine bağlı olarak, giderleri maddeleştirin.
- Bir gider raporunu onay veya geri ödeme için gönderin.
- Atanmış onaylayıcısı olduğunuz gider raporlarını onaylayın veya reddedin.

## <a name="prerequisites"></a>Ön koşullar
Önkoşullar, kuruluşunuza dağıtılan Microsoft Dynamics 365 sürümüne dayalı olarak farklılık gösterir.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition Temmuz 2017 güncelleştirmesini kullanıyorsanız önkoşullar 
Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü Temmuz 2017 güncelleştirmesi kuruluşunuza dağıtıldıysa, sistem yöneticisinin **Gider yönetimi** mobil çalışma alanını yayımlaması gerekir. Yönergeler için bkz: [Bir mobil çalışma alanı yayımlama](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations sürüm 1611 platform güncelleştirmesi 3 veya daha sonraki sürüm kullanıyorsanız ön koşullar
Kuruluşunuza platform güncelleştirmesi 3 veya üzeri ile Microsoft Dynamics 365 for Operations 1611 sürümü dağıtılmışsa, sistem yöneticisinin aşağıdaki ön koşulları yerine getirmesi gerekir. 

<table>
<thead>
<tr class="header">
<th>Önkoşul</th>
<th>Rol</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 4019015 uygulayın.</td>
<td>Sistem yöneticisi</td>
<td>KB 4019015, <strong>Gider yönetimi</strong> mobil çalışma alanını içeren bir X++ güncelleştirmesi veya meta veri düzeltmesidir. KB 4019015 uygulamak için sistem yöneticiniz bu adımları atması gerekir.
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Meta veri düzeltmesini Microsoft Dynamics Lifecycle Services (LCS) üzerinden indirin</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Meta veri düzeltmesini kurun</a>.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Dağıtılabilir bir paket oluşturun</a> <strong>ApplicationSuite</strong> ve <strong>ExpenseMobile</strong> modellerini içeren ve daha sonra dağıtılabilir paketi LCS'ye yükleyin.</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Dağıtılabilir paketi uygulayın</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>Gider yönetimi</strong> mobil çalışma alanını yayımlayın.</td>
<td>Sistem yöneticisi</td>
<td>Bkz. <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobil çalışma alanı yayınlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobil uygulamasını yükleyin ve kurun
Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:

- [Android telefonlar için](https://go.microsoft.com/fwlink/?linkid=850662)
- [İPhone'lar için](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Mobil uygulamaya oturum açın
1. Mobil cihazınızda uygulamayı başlatın.
2. Dynamics 365 URL'nizi girin.
4. İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir. Kimlik bilgilerinizi girin.
5. Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir. Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.


[![Yenilemek için çekin](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak bir girişi yakalayın

1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Giriş yakalama**'yı seçin.
3. **Fotoğraf çek** veya **Resim seç**'i seçin.
4. Şu adımlardan birini izleyin:

    - **Fotoğraf çek**'i seçtiyseniz, şu adımları izleyin:

        1. Mobil cihazınızın kamerasına götürülürsünüz ve böylece fişin bir faturasını çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde, fotoğrafı kabul etmek için **Tamam**'ı seçin.
        2. İsteğe bağlı: Fotoğraf için bir isim ve varsa not girin.

    - **Resim seç**'i seçtiyseniz, şu adımları izleyin:

        1. Listeden bir resim seçin.
        2. İsteğe bağlı: Resim için bir isim ve varsa not girin.

5. **Tamam**'ı seçin.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Gider yönetimi mobil çalışma alanını kullanarak giderleri hızlıca girin
1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Hızlı gider girişi**'ni seçin.
3. Gider için kategori seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş gider kategorilerinin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Kategoriniz listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Gider kategorisine göre arama yapın veya gider türüne göre aramaya geçin.
4. Giderin hareket tarihini girin.
5. İsteğe bağlı: Gider için tüccarı girin.
6. Giderin tutarını girin.
7. Giderin para birimini seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş para birimlerinin bir listesini görürsünüz. Varsayılan olarak, 400 para birimi yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Para biriminiz listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Para birimine göre arama yapın veya adına göre aramaya geçin.
8. **Fotoğraf çek** veya **Resim seç**'i seçin.
9. Şu adımlardan birini izleyin:

    - **Fotoğraf çek**'i seçtiyseniz, mobil cihazınızın kamerasına götürülürsünüz ve böylece fişin bir faturasını çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde, fotoğrafı kabul etmek için **Tamam**'ı seçin.
    - **Resim seç**'i seçtiyseniz, listeden bir resim seçin.

10. **Tamam**'ı seçin.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Gider yönetimi mobil çalışma alanını kullanarak bir gider raporunu onaylayın (Temmuz 2017 güncelleştirmesin kullanıyorsanız)
1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Gider onayları**, onayınız için size atanmış olan gider raporlarının sayısını gösterir. Bu sayı yaklaşık her 30 dakikada bir güncelleştirilir. **Gider onayları**'nı seçin.

    Onayınız için size atanmış olan gider raporlarının listesi gösterir.
    
3. Gider ayrıntılarını görmek için bir gider raporu seçin.
4. Ayrıntılarını görmek için bir gider seçin. Bir gider için gösterilen bilgi tüm fişleri, konukları ve maddeleme ayrıntılarını içerir.
5. **Gider raporu sayfasında**, gider raporunu onaylamayı veya reddetmeyi seçin.
6. Onay eylemi için herhangi bir yorum girin
7. **Tamam**'ı seçin.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Gider yönetimi mobil çalışma alanını kullanarak yeni bir gider raporu oluşturun ve onaylamaya gönderin (Temmuz 2017 güncelleştirmesin kullanıyorsanız)
1. Mobil cihazınızda **Gider yönetimi** çalışma alanını açın.
2. **Gider girişi**'ni seçin.
3. **Yeni rapor**'u seçin veya varolan bir gider raporunu listeden seçin.
4. Yeni gider raporları için amacı ve mevcut diğer bilgileri girin. Bu bilgi, gider yönetiminin şirketinizde nasıl yapılandırıldığına göre çeşitlilik gösterir.
5. **Tamam**'ı seçin.
6. Kredi kartı hareketleri gibi mevcut giderleri gider raporuna eklemek için **Ekle**'yi seçin.
7. Listeden bir veya daha fazla gider seçin.
8. **Tamam**'ı seçin.
9. Gider raporuna yeni bir gider eklemek için **Yeni gider**'i seçin.
10. Gider için kategori seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş gider kategorilerinin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Kategoriniz listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Gider kategorisine göre arama yapın veya gider türüne göre aramaya geçin.
11. İsteğe bağlı: Gider için tüccarı girin.
12. Giderin hareket tarihini girin.
13. Giderin tutarını girin.
14. Giderin para birimini seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş para birimlerinin bir listesini görürsünüz. Varsayılan olarak, 400 para birimi yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Para biriminiz listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Para birimine göre arama yapın veya adına göre aramaya geçin.
15. **Tamam**'ı seçin.
16. Gidere daha fazla ayrıntı eklemek için **Daha fazla ayrıntı ekle**'yi seçin. Kullanılabilir olan alanlar, gider yönetiminin şirketinizdeki yapılandırmasına bağlıdır.
17. Bir şirket ilkesi, bir gider için fiş gerektiriyorsa, **Fişler**'i seçin ve daha sonra aşağıdaki adımları izleyin:

    1. **Fişi yakala** veya **Fişi ekle**'yi seçin.
    2. Şu adımlardan birini izleyin:

        - **Fişi yakala**'yı seçtiyseniz, aşağıdaki adımları izleyin:

            1. **Fotoğraf çek** veya **Resim seç**'i seçin.
            2. Şu adımlardan birini izleyin:

                - **Fotoğraf çek**'i seçtiyseniz, şu adımları izleyin:

                    1. Mobil cihazınızın kamerasına götürülürsünüz ve böylece fişin bir faturasını çekebilirsiniz. Fotoğraf çekmeyi bitirdiğinizde, fotoğrafı kabul etmek için **Tamam**'ı seçin.
                    2. İsteğe bağlı: Fotoğraf için bir isim ve varsa not girin.

                - **Resim seç**'i seçtiyseniz, şu adımları izleyin:

                    1. Listeden bir resim seçin.
                    2. İsteğe bağlı: Resim için bir isim ve varsa not girin.

            3.  **Tamam**'ı seçin.

        - **Fişi ekle**'yi seçtiyseniz, aşağıdaki adımları izleyin:

            1.  Listeden bir veya daha fazla resim seçin.
            2.  **Tamam**'ı seçin.

    3. Gider ayrıntılarına dönmek için **Geri** düğmesini seçin.

18. Bir şirket ilkesi, bir gider için konuklar gerektiriyorsa, **Konuklar**'ı seçin ve daha sonra aşağıdaki adımları izleyin:

    1. **Konuk**, **Önceki konuklar** veya **İş arkadaşları**'nı seçin.
    2. Şu adımlardan birini izleyin:

        - **Konuk**'u seçtiyseniz, şu adımları izleyin:

            1. Konuğun adını girin.
            2. İsteğe bağlı: Konuğun kuruluşunu ve/veya ülkesini girin.
            3. İsteğe bağlı: Konuğun unvanını girin.
            4. **Tamam**'ı seçin.

        - **Önceki konuklar**'ı seçerseniz aşağıdaki adımları izleyin:

            1. Listeden bir veya daha fazla önceki konuğu seçin. Önceki gider raporlarına eklemiş olduğunuz önceki konukların çevrimdışı kullanım için uygulamanıza yüklenmiş bir listesini göreceksiniz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Önce konuk listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Adına göre arama yapın veya kuruluş, ülke veya unvana göre aramaya geçin.
            2. **Tamam**'ı seçin.

        - **İş arkadaşları**'nı seçtiyseniz, şu adımları izleyin:

            1. Listeden bir veya daha fazla iş arkadaşı seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş iş arkadaşlarının bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). İş arkadaşınız listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Adına göre arama yapın veya şirket, veya unvana göre aramaya geçin.
            2. **Tamam**'ı seçin.

    3. Gider ayrıntılarına dönmek için **Geri** düğmesini seçin.

19. Şirket ilkesi, bir giderin listelenmiş olmasını gerektiriyorsa, **Listelenmiş**'i seçin ve daha sonra aşağıdaki adımları izleyin:

    1. Listelenecek ilk tarihi seçin.
    2. **Listeleme ekle**'yi seçin.
    3. Gider listeleme için alt kategoriyi seçin. Çevrimdışı kullanım için uygulamanıza yüklenmiş gider alt kategorilerinin bir listesini görürsünüz. Varsayılan olarak, 50 madde yüklenir, ancak bir geliştirici bu sayıyı değiştirebilir. Geliştiriciler, daha fazla bilgi için şuraya göz atabilirler: [Mobil platform](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform). Alt kategoriniz listede yoksa, bir çevrimiçi arama gerçekleştirmek için **Ara**'yı seçin. Gider alt kategorisi adına göre arayın.
    4. Listeleme için hareket tutarını girin.
    5. İhtiyaç duyulursa hareket tarihini düzenleyin.
    6. **Tamam**'ı seçin.
    7. Seçilen tarih için tüm listelemeleri eklemeyi tamamlayana kadar önceki adımları yineleyin.
    8. Ek günler için, **Sonraki güne kopyala**'yı seçerek listelemeyi sonraki güne kopyalayabilirsiniz. Alternatif olarak, listelenecek tarihleri seçebilir ve daha sonra ilk tarihte yaptığınız gibi listelemeler ekleyebilirsiniz.
    9. Gideri listelemeyi bitirdikten sonra, **Geri** düğmesini seçerek gider ayrıntılarına dönün.

20. **Gider raporu** sayfasına dönmek için **Geri** düğmesini seçin.
21. Tüm giderleri eklemeyi bitirene kadar önceki adımları yineleyin.
22. **Gönder**'i seçin.
23. Onaylayıcı için herhangi bir yorum girin.
24. **Tamam**'ı seçin.

