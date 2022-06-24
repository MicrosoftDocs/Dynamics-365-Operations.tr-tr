---
title: LinkedIn Talent Hub ile tümleştirme
description: Bu makalede, Microsoft Dynamics 365 Human Resources ile LinkedIn Talent Hub arasındaki tümleştirmenin nasıl ayarlanacağı açıklanmaktadır.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df4a0a4dec078392ba835318450f5983a6e95c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887762"
---
# <a name="integrate-with-linkedin-talent-hub"></a>LinkedIn Talent Hub ile tümleştirme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> Bu makalede açıklanan Dynamics 365 Human Resources ile LinkedIn Talent Hub arasındaki tümleştirme, 31 Aralık 2021 tarihinde kullanımdan kaldırıldı. Tümleştirme hizmeti, bu tarihten sonra artık kullanılamayacaktır. Tümleştirme hizmetini zaten kullanmayan kuruluşlar, kullanımdan kaldırılmadan önce hizmeti uygulayamaz.

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) bir başvuran izleme sistemi (ATS) platformudur. Tek bir yerden çalışanları bulmanıza, yönetmenize ve işe almanıza olanak tanır. Microsoft Dynamics 365 Human Resources ile LinkedIn Talent Hub'ı tümleştirerek bir pozisyon için işe alınan kişiler için Human Resources'da kolayca çalışan kayıtları oluşturabilirsiniz.

## <a name="setup"></a>Ayar

Bir sistem yöneticisinin LinkedIn Talent Hub ile tümleştirmeyi etkinleştirmek için kurulum görevlerini tamamlaması gerekir. Öncelikle, LinkedIn Talent Hub'a Human Resources'a veri yazmak için uygun izinleri vermek üzere Power Apps ortamında bir kullanıcı ve güvenlik rolü ayarlamanız gerekir.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Ortamınızı LinkedIn Talent Hub'a bağlayın

1. [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub)'ı açın.

2. Kullanıcı açılan menüsünde **Ürün Ayarları**'nı seçin.

3. Sol gezinti bölmesinde, **Gelişmiş** bölümünde, **Tümleştirmeler**'i seçin.

4. Microsoft Dynamics 365 Human Resources tümleştirmesi için **Yetkilendir**'i seçin.

5. **Dynamics 365 Human Resources** sayfasında LinkedIn Talent Hub'ı bağlayacağınız ortamı seçin ve sonra **Bağla**'yı seçin.

    ![LinkedIn Talent Hub işe alma.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Yalnızca Kullanıcı hesabınızın, hem Human Resources ortamında hem de ilişkili Power Apps ortamında yönetici erişimi olan ortamlara bağlanabilirsiniz. Human Resources bağlantı sayfasında herhangi bir ortam listelenmiyorsa, Human Resources ortamlarını kiracıda lisansladığınızdan ve bağlantı sayfasında oturum açmış olan kullanıcının hem Human Resources ortamı hem de Power Apps ortamı için yönetici izinlerine sahip olduğundan emin olun.

### <a name="create-a-power-apps-security-role"></a>Power Apps Güvenlik rolü oluşturma

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, LinkedIn Talent Hub örneğinizi bağlamak istediğiniz Human Resources ortamıyla ilişkilendirilmiş ortamı seçin.

3. **Ayarlar**'ı seçin.

4. **Kullanıcılar + izinler** düğümünü genişletin ve **Güvenlik rolleri**'ni seçin.

5. **Güvenlik rolleri** sayfasında, araç çubuğunda **Yeni rol**'ü seçin.

6. **Ayrıntılar** sekmesinde, **LinkedIn Talent Hub HRIS tümleştirmesi** gibi rol için bir ad girin.

7. **Özelleştirme** sekmesinde, aşağıdaki varlıklar için kuruluş düzeyinde **okuma** izni seçin:

    - Varlık
    - Alan
    - Yakınlık derecesi

8. Güvenlik rolünü kaydedin ve kapatın.

### <a name="create-a-power-apps-application-user"></a>Power Apps uygulaması kullanıcısı oluşturun

Aday kayıtlarını Power Apps ortamına yazmak için bağdaştırıcıya gereken izinleri vermek amacıyla LinkedIn Talent Hub bağdaştırıcısı için bir uygulama kullanıcısı oluşturulmalıdır.

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, LinkedIn Talent Hub örneğinizi bağlamak istediğiniz Human Resources ortamıyla ilişkilendirilmiş ortamı seçin.

3. **Ayarlar**'ı seçin.

4. **Kullanıcılar + izinler** düğümünü genişletin ve **Kullanıcılar**'ı seçin.

5. **Dynamics 365'te kullanıcıları Yönet**'i seçin.

6. Görünümü varsayılan **etkin kullanıcılar** görünümünden **uygulama kullanıcıları** görünümüne değiştirmek için listenin üzerindeki açılan menüyü kullanın.

    ![Uygulama Kullanıcıları görünümü.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Araç çubuğunda **Yeni**'yi seçin.

8. **Yeni kullanıcı** sayfası üzerinde, aşağıdaki adımları izleyin:

    1. **Kullanıcı türü** alanının değerini **Uygulama Kullanıcısı** olarak değiştirin.
    2. **Kullanıcı adı** alanını **Dynamics365 HR LinkedIn HRIS tümleştirmesine** ayarlayın.
    3. **Uygulama Kimliği** alanını **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** olarak ayarlayın.
    4. **Adı**, **Soyadı** ve **birincil e-posta** alanlarına herhangi bir değer girin.
    5. Araç çubuğunda **Kaydet\& Kapat**'ı seçin.

### <a name="assign-a-security-role-to-the-new-user"></a>Yeni kullanıcıya güvenlik rolü atama

Önceki bölümde yeni uygulama kullanıcısını kaydettikten ve kapattıktan sonra, **kullanıcılar listesi** sayfasına geri dönülür.

1. **Kullanıcılar listesi** sayfasında, görünümü **uygulama kullanıcıları** olarak değiştirin.

2. Önceki bölümde oluşturduğunuz uygulama kullanıcısını seçin.

3. Araç çubuğunda **Rolleri Yönet**'i seçin.

4. Tümleştirme için daha önce oluşturduğunuz güvenlik rolünü seçin.

5. **Tamam**'ı seçin.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Human Resources'ta bir Azure Active Directory uygulaması ekleme

1. Dynamics 365 Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.
2. Listeye yeni bir kayıt ekleyin ve aşağıdaki alanları ayarlayın:

    - **İstemci kimliği**: **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** değerini girin.
    - **Ad**: **LinkedIn Talent Hub HRIS tümleştirmesi** gibi daha önce oluşturduğunuz Power Apps güvenlik rolünün adını girin.
    - **Kullanıcı kimliği**: Personel yönetiminde veri yazma izni olan bir kullanıcı seçin.

### <a name="create-the-table-in-dataverse"></a>Tabloyu Dataverse'te oluşturma

> [!IMPORTANT]
> LinkedIn Talent Hub ile tümleştirme, Human Resources için Dataverse'te sanal tablolara bağlıdır. Kurulumda bu adım için bir önkoşul olarak, sanal tablolar yapılandırmalısınız. Sanal tabloların nasıl yapılandırılacağı hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).

1. Human Resources'ta **Dataverse tümleştirmesi** sayfasını açın.

2. **Sanal tablolar** sekmesini seçin.

3. **LinkedIn dışa aktarılan aday**'ı bulmak için varlık listesini varlık etiketine göre filtreleyin.

4. Varlığı ve ardından **Oluştur/Yenile**'yi seçin.

## <a name="exporting-candidate-records"></a>Aday kayıtlarını dışa aktarma

Kurulum tamamlandıktan sonra, işe alma ve İnsan kaynakları (HR) uzmanları, işe alınan aday kayıtlarını LinkedIn Talent Hub'dan Human Resources'a dışa aktarmak için LinkedIn Talent Hub'daki **HRIS'e Dışarı Aktar** işlevini kullanabilirler.

### <a name="export-records-from-linkedin-talent-hub"></a>LinkedIn Talent Hub'dan kayıtları dışa aktar

Bir aday işe alma sürecinden geçip işe alındığında, aday kaydını LinkedIn Talent Hub'dan Human Resources'a dışa aktarabilirsiniz.

1. LinkedIn Talent Hub'da yeni çalışanın çalışacağı projeyi açın.

2. Bir aday kaydı seçin.

3. **Aşamayı değiştir**'i ve ardından **İşe alındı**'yı seçin.

4. Aday için üç nokta menüsünde (**...**) **HRIS'e Dışa Aktar**'ı seçin.

5. **HRIS'e Dışa aktar** bölmesinde, dışa aktarılması gereken bilgileri girin:

    - **HRIS sağlayıcısı** alanında **Microsoft Dynamics 365 Human Resources**'ı seçin.
    - **Başlangıç tarihi** alanında yeni çalışan için bir değer seçin.
    - **İş unvanı** alanına, yeni çalışanın işi için bir iş unvanı girin.
    - **Konum** alanına, çalışanın çalışacağı konumu girin.
    - Çalışanın e-posta adresini girin veya doğrulayın.

![LinkedIn Talent Hub'da HRIS'e Dışa Aktar bölmesi.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Human Resources'ta işe almayı tamamlama

LinkedIn Talent Hub'dan Human Resources'a dışa aktarılan aday kayıtları **personel yönetimi** sayfasının **işe alınacak adaylar** bölümünde görüntülenir.

1. Human Resources'da, **Personel yönetimi** sayfasını açın.

2. **İşe alınacak adaylar** bölümünde, Seçilen aday için **İşe al**'ı seçin.

3. **Yeni çalışanı işe al** iletişim kutusunda, kaydı inceleyin ve gerekli bilgileri ekleyin. Ayrıca, adayın işe alındığı pozisyon numarasını da seçebilirsiniz.

Gerekli bilgiler girildikten sonra, çalışan kayıtlarını oluşturmak ve çalışanların işe başlamasını sağlamak için standart işlemlerinize devam edebilirsiniz.

Aşağıdaki ayrıntılar içe aktarılır ve yeni çalışan kaydına dahil edilir:

- Adı
- Soyadı
- İstihdam başlama tarihi
- E-posta adresi
- Telefon numarası

## <a name="see-also"></a>Ayrıca bkz.

[Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Microsoft Dataverse nedir?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
