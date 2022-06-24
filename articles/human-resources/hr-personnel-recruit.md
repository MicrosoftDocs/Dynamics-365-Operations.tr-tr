---
title: İş adaylarını işe alma
description: Bu makalede, Dynamics 365 Human Resources'da adayların nasıl işe alınacağı açıklanmaktadır.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 743c78d3526db2707630229d4cf21531f9641dd6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879264"
---
# <a name="recruit-job-candidates"></a>İş adaylarını işe alma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources işe alma isteklerini yönetmenize yardımcı olur. Ayrıca, çalışanların iş adaylarına sorunsuz şekilde geçiş yapmanıza yardımcı olur. Organizasyonunuzda ayrı bir işe alma uygulaması kullanılıyorsa, işe alma işleminiz aşağıdaki adımları içerebilir:<!--note from editor: Should this be a numbered list? These steps do seem to follow a particular order.-->

- İşe alma isteğinizi İnsan Kaynakları girin.
- İşe alma uygulamasından İnsan Kaynakları aday başvurularını alın.
- Aday onaylama işlemini İnsan Kaynakları tamamlayın.

Ayrı bir işe alma uygulaması kullanmıyorsanız, İnsan Kaynakları adayların da el ile yönetilmesini sağlayabilirsiniz.

> [!NOTE]
> Bir yönetici veya geliştiricisiyseniz Human Resources'ı üçüncü taraf işe alma uygulamasıyla tümleştirmek istiyorsanız [Dataverse tümleştirmesini yapılandırma](hr-admin-integration-common-data-service.md) ve [Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md) sayfalarına gidin
>
> [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) işe alma tümleştirme uygulamalarını da bulabilirsiniz.
>
## <a name="enable-recruiting-requests-on-the-merged-infrastructure"></a>Birleştirilmiş altyapıda işe alma isteklerini etkinleştirme

İşe alma isteklerini İK işe alma modülünde göndermek istiyorsanız, önce **İK Kullanıcı deneyimi** ve **İşe alma işlem yönetimi** özelliklerini etkinleştirmelisiniz.

Özellikler etkinleştirildikten sonra, aşağıdaki adımlarla işlevi seçin: 
1. **Human resources** > **Kurulum** > **Human resources parametreleri**'ne gidin.
2.  **İşe alma** sekmesinde, **İşe alma etkinleştirildi** alanını **Evet** olarak ayarlayın.
3. **İşe alma deneyimi** açılır menüsünde, **İK işe alma** seçeneğini belirleyin.  
4. **Kaydet**'e tıklayın. 

> [!Note] 
> **İK işe alma** seçildiğinde, **İşe alma projeleri** (eski) kullanılamaz. 


## <a name="add-a-recruiting-request-location"></a>İşe alma isteği Ekle konumu

Kuruluşunuzun birden çok konumu varsa, bu dosyaları ekleyerek bunları ekleyebilirsiniz ve böylece istek, yeni işe çalıştığınız yerdeki bir yerleşim seçebilir. Yerleşim, proje nakline dahil edilecek.

1. Arama çubuğunda, **İşe alma istek konumunu** girin.
2. **Yeni**'yi seçin.
3. **İşe alma istek yerleşimi** alanına yerleşim adını girin.

    ![İşe alma isteği Ekle konumu.](./media/hr-recruit-0a-add-location.png)

4. **Açıklama** alanında konum için bir açıklama girin.
5. **Konum** altında, **Ekle**'yi seçin. **Yeni adres** iletişim kutusu görünürse, konumun adresini girin.<!--note from editor: Please make the address in this image less plausible. Via the fictitious guidelines on CELAweb: For street addresses, you should use sequential numbers, common street names, and incorrect zip codes (e.g., 4567 Main St Buffalo, NY 98052). (See https://microsoft.sharepoint.com/sites/CELAWeb-Copyrights-Trademarks-And-Patents/SitePages/trademarks-fictitious-names.aspx)-->

    ![Adresi girme.](./media/hr-recruit-0b-address.png)

6. **İlgili kişi bilgileri** altında yerleşimin ilgili kişisinin bilgilerini girin.
7. **Kaydet**'i seçin.

## <a name="add-a-recruiting-request"></a>İşe alma isteği Ekle

Yöneticiler İnsan Kaynakları işe alma istekleri gönderebilir. Ayrı bir işe alma uygulaması kullanırsanız, bu adımlar tamamlandıktan sonra işe alma isteği gönderilir ve işe alma işlemini o uygulamada başlatır. Aksi durumda, iş akışını kendi iç işe alma işleminiz için başlatmak üzere bu yordamı tamamlayın.

1. **Çalışan self servisini** seçin.
2. **Ekibim** sekmesini seçin.
3. **İşe almak için talep**'i seçin.

    ![İşe alma isteği başlatma.](./media/hr-recruit-1-request-to-recruit.png)

4. **Açıklama**, **iş** ve **Tahmini Başlangıç tarihi** alanlarını tamamlayın.

    ![İşe alma isteğini tamamlama.](./media/hr-recruit-2-request-to-recruit.png)

5. **Devam**'ı seçin. Konumlarınıza ilişkin işe alma isteği görüntülenir.
6. **Genel** altında, **İşe alan** açılan listesinden bir işe alan seçin ve **İşe alma isteği konumu** açılan listesinden bir konum seçin.
7. **İş** altında, gerekli tüm bilgileri değiştirin ve sonra **işten ayrıntıları oluştur**'u seçin.

    ![İşten ayrıntı oluşturma.](./media/hr-recruit-3-create-details-from-job.png)

    İşe alma isteğinin geri kalanı girdiğiniz işle ilgili varsayılan bilgilerle doldurulur.

8. **Harici açıklama** altında harici olarak açık bir iş açıklaması girin.
9. **Pozisyonlar** altında, **Ekle** 'yi seçin ve sonra bu işe alma isteği için bir pozisyon seçin.<!--note from editor: In all of these images, are they approved fictitious names, or do they come from sample data included with the app?-->

    ![Pozisyon ekleme.](./media/hr-recruit-4-select-position.png)

10. **Yetenekler**'in altında , **Ekle**'yi seçin ve sonra da bir yetenek seçin.
11. **Eğitim gereksinimleri** altında , **Ekle**'yi seçin ve sonra **Eğitim** ve **Eğitim düzeyi** açılan menülerinden değerleri seçin.

    ![Eğitim gereksinimleri ekleme.](./media/hr-recruit-5-select-educational-requirements.png)

12. **Yorum** altında gerektiği şekilde yorumlar ekleyin.
13. **Dengeleme** altında, **düzey** açılan listesinden bir düzey seçin ve sonra **Düşük eşik**, **Kontrol noktası** ve **Yüksek eşik** ayarlarını gerektiği gibi ayarlayın.
14. İşe alma isteğiniz tamamlandığında ve işe alma işlemini başlatmaya hazır olduğunuzda, menü çubuğunda **Etkinleştir**'i seçin.

    ![İşe alma isteğini etkinleştirme.](./media/hr-recruit-6-activate-recruit-request.png)

15. **Kaydet**'i seçin.

## <a name="view-and-edit-your-recruiting-requests"></a>İşe alma isteklerinizi görüntüleyin ve düzenleyin

Bir yönetici iseniz ve kendi isteklerinizi görüntülemek istiyorsanız:

1. **Çalışan self servisini** seçin.
2. **Ekibim** sekmesini seçin.
3. **Ekip bilgilerim** altında, **İşe alma istekleri** sekmesini seçin.

    ![İşe alma istekleri sekmesini seçme.](./media/hr-recruit-7-recruiting-requests.png)

4. İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.

Bir İK Pro iseniz ve tüm işe alma isteklerini görüntülemek istiyorsanız:

1. **Personel yönetimi**'ni seçin.
2. **Işe alma istekleri** seçin.

    ![Personel yönetiminde işe alma isteklerini görüntüleme.](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.

## <a name="add-or-edit-a-candidate-profile"></a>Aday profili ekleme veya düzenleme

Kuruluşunuz işe alma isteklerini yönetmek için başka bir uygulamayla tümleşikse, işe alma istekleri o uygulamaya iletilir. İşe alma uygulaması daha sonra aday bilgilerini İnsan Kaynakları geri gönderir. Aksi durumda, kendi iç işe alma işlemlerinizi takip edebilir ve aday bilgilerini el ile girebilirsiniz.

1. **Personel yönetimi**'ni seçin.
2. **Bağlantılar**'ı seçin.
3. **İşe alma** altında **Adaylar**'ı seçin.

    ![Adayları görüntüleme.](./media/hr-recruit-9-candidates.png)

4. Aday eklemek için **Yeni**'yi seçin. Varolan bir adayı düzenlemek için, listeden aday seçin ve **Düzenle**'yi seçin. Aday profili görüntülenir.
5. **Aday Özeti** altında aday bilgilerini gerektiği gibi girin veya düzenleyin.
6. **İşe alma isteği** altında adayı bağlamak için bir işe alma isteği seçin. **Tahmini başlangıç tarihi**, **İşe alma yöneticisi**, **Konum** ve **Açıklama** alanlarını gerektiği gibi tamamlayın.

    ![İşe alma isteğine bağlantı.](./media/hr-recruit-10-link-to-recruiting-request.png)

7. Aday kaydına dahil etmek istediğiniz aşağıdaki alanlardaki tüm bilgileri tamamlayın:

    - **Yorumlar**
    - **Mesleki deneyim**
    - **İletişim bilgileri**
    - **Eğitim**
    - **Yetenekler**
    - **Sertifikalar**
    - **Filtrelemeler**

8. **Kaydet**'i seçin.

## <a name="hire-a-candidate"></a>Adayı işe al

Bir adayı işe almak için hazır olduğunuzda, adayı bir çalışana aktarmak için aşağıdaki yordamı izleyin.

1. **Aday** sayfasında **İşe al**'ı seçin.

    ![Adayı işe alma.](./media/hr-recruit-11-hire.png)

2. **İşe yeni çalışan** sayfasında, **Ayrıntılar** altında tüm alanları doldurun.

    ![Yeni işe alma ayrıntılarını girme.](./media/hr-recruit-12-hire-new-worker.png)

3. **Pozisyon ayrıntıları** altında , bilgileri gerektiği gibi doğrulayın ve değiştirin.
4. **Ekleme listeleri listesi** altında , bu çalışana ait ilgili ekleme denetim listelerini seçin.
5. Çalışan kaydını oluşturmak için **devam** 'ı seçin.

    > [!NOTE]
    > Kuruluşunuzun iş akışlarına bağlı olarak, aday kaydı, bir çalışan kaydı yapılmadan önce ek onay adımlarıyla geçebilir.

## <a name="decide-not-to-hire-a-candidate"></a>Aday işe gerekmediğine karar verme

Bir adayı işe almamaya karar verirseniz, aşağıdaki yordamı izleyerek onları vetele alma işleminden çıkarabilirsiniz. 

1. **Aday** sayfasında **İşe alma**'yı seçin.

    ![Adayı işe alma.](./media/hr-recruit-13-do-not-hire.png)

2. Bir **neden kodu** seçin ve açıklama ekleyin.
3. **Tamam**'ı seçin.

## <a name="dismiss-a-candidate"></a>Adayı kapat

Gerekirse, bir adayı işe aldıktan sonra kapatabilirsiniz. Örneğin, bir aday teklifinizi reddedebilir veya ilk gününde göstermeyebilirsiniz.

- **Aday** sayfasında **Adayı kapat**'ı seçin.

    ![Adayı bırakma.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a>Ayrıca bkz.

[Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[İş gücünüzü düzenleme](hr-personnel-departments-jobs-positions.md)<br>
[İşin bileşenlerini ayarlama](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
