---
title: Attract ve Onboard üzerinden veri dışarı aktarmak
description: Dynamics 365 Talent üzerinden veri dışarı aktarmak - Attract ve Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462773"
---
# <a name="export-data-from-attract-and-onboard"></a>Attract ve Onboard üzerinden veri dışarı aktarmak

[!include [banner](includes/banner.md)]

[Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard Uygulamaları devre dışı kalıyor](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), 1 Şubat 2022 tarihinde Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard ürünlerini devre dışı bırakıyoruz. Başka bir ürüne geçişinize yardımcı olmak için, her iki uygulama da veri dışa aktarma becerisi sağlar.

## <a name="export-data-from-attract"></a>Verileri Attract üzerinden dışa aktar

Verilerinizi, ortamınıza erişimi sınırlamadan verebilirsiniz. Bunu test amacıyla veya veri yapımızı anlamak için yapmak isteyebilirsiniz. Taşımaya hazır olduğunuzda, bu yordamdan sonraki yönergeleri kullanarak atmaya çalışma ortamınıza erişimi kısıtlayın. Verilerinizi yeniden dışa aktardığınızdan emin olun. 

1. [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) gidin.

2. **Veri dışa aktarma** altında, **Veri dışa aktarma talebi**'ni seçin.

   ![[Attract üzerinden bir veri dışa aktarma talep edin](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. **İsteğiniz işleniyor** mesaj kutusu görüntülendiğinde, **Tamam**'ı seçin. Veri dışa aktarma 20 dakika kadar sürebilir, dışa aktarmanızın ebatlarına bağlı olarak.

4. Dışa aktarma işlemi tamamlandığında, yanındaki **İndir** düğmesini seçin. 

   >[!NOTE]
   >Tüm veri dışa aktarma işlemleri yedi gün süreyle kullanılabilir, bu noktada **İndir** bağlantısı geçerliliğini yitirir.</br>
   
Karşıdan yükleme, aşağıdaki klasörler de dahil olmak üzere, Attract verinizi içeren bir .zip dosyası içerir:

| Klasör adı | Tanım |
| --- | --- |
| Yönetici ayarları | Attract yönetim merkezi yapılandırmaları. |
| Adaylar | İşlere veya yetenek havuzlarına eklenen tüm adaylar. |
| E-posta şablonları | Ortam için yapılandırılan tüm e-posta şablonları. |
| İş teklifi paketi şablonları | Tüm iş, oluşturulan paket şablonları ve bunların ilişkili yapılandırmalarını sunar. |
| İş teklifi kural kümeleri |  Tüm kural, teklif yönetimi için karşıya yüklenen dosyaları ayarlar. |
| İş teklifi şablonları | Tüm iş, ortam için oluşturulmuş belge şablonlarını sunar. |
| Açık pozisyonlar | Oluşturulan işler. Silinen işler aktarılmaz. Alt klasörler, aday uygulama ekleri için alt klasörlerle, uygun durumlarda paketleri sunan aday uygulamaları içerir. |
| Açık pozisyon şablonları | Ortamda yapılandırılan İş işlemi şablonları. |
| Yetenek havuzları | Tüm oluşturulan havuzlar, katılımcı listeleri ve yetenek havuzları için aday listeleri. |
| Çalışanlar | Ortamda bulunan tüm çalışanların ve bunların rollerinin listesi. |
| (kök klasör) | Veri yapısı alanlarını açıklayan bir JSON şema dosyası. |

### <a name="restrict-access-to-attract"></a>Attract'e erişimi kısıtla

Geçirmeye hazır olduğunuzda, yönetici olmayanların Attract ortamınıza erişmesini ve verilerinizi dışa aktarmayı kısıtlayın.

>[!IMPORTANT]
>Attract ortamınıza erişimi kısıtlamak kalıcıdır ve geri alınamaz. Yönetici olmayan kullanıcıların ortamınıza erişmeye devam etmesini istiyorsanız, bu adımı atlayın.

1. [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport) gidin.

2. Yönetici olmayanların Attract erişim ortamınıza erişimini kısıtlamak için **Bu uygulama yerleşimi kısıtla** altında, **şimdi erişimi kısıtla**'yı seçin. Erişimin sınırlandırılması, ayrıca deftere nakledilen etkin işlerin deftere nakledilmesini geri alınmasına neden olur.

   ![[Attract'e yönetici olmayanların erişimini kısıtla](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. **Bu kalıcı bir değişikliktir** uyarısını görürseniz, bu ortamdan yönetici olmayanların erişimini kalıcı olarak kısıtlamak için **Erişimi kısıtla**'yı seçin. Bu adımı tamamlamaya hazırsanız **İptal et**'i seçin.

   ![[Erişimi kısıtlamanın kalıcı bir değişiklik olduğu uyarısı](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Attract ortamına erişimi kısıtladıktan sonra, Yöneticiler veri dışa aktarma ve kişi rapor sayfalarına erişmeye devam edebilir.

## <a name="export-data-from-onboard"></a>Verileri Onboard'tan dışa aktar

Hazır olduğunuzda, şablonları, kılavuzları ve aday verilerini Onboard'tan karşıdan yükleyebilirsiniz.

1. [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport) gidin.

2. **Veri dışa aktarma** altında, **Veri dışa aktarma talebi**'ni seçin. 

   ![[Onboard üzerinden bir veri dışa aktarma talep edin](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. **İsteğiniz işleniyor** mesaj kutusu görüntülendiğinde, **Tamam**'ı seçin. Veri dışa aktarma 20 dakika kadar sürebilir, dışa aktarmanızın ebatlarına bağlı olarak.

4. Dışa aktarma işlemi tamamlandığında, yanındaki **İndir** düğmesini seçin. 

   ![[Onboard'tan dışa aktarma verisini indirmek](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Veri dışa aktarma isteğiniz yedi gün süreyle kullanılabilir. Yedi gün sonra, **karşıdan yükleme** bağlantısının süresi dolar ve verilerinizi tekrar yüklemeniz gerekiyorsa, yeni bir dışa aktarma istemeniz gerekir. Yeni dışa veri aktarma işlemi başlattığınızda, yeni verme işlemi başarılı olduktan sonra varolan tüm karşıdan yükleme işlemleri sona erer.

Bu yükleme, aşağıdakileri içeren bir .zip dosyasıdır:

- Onboard şablonlarınızı bir Word belgesi biçiminde içeren bir **Şablonlar** klasörü.

- Onboard kılavuzlarınızı bir Word belgesi biçiminde içeren bir **Guides** klasörü.

## <a name="see-also"></a>Ayrıca bkz.

[Dynamics 365 Talent: Attract ve Dynamics 365 Talent: Onboard Uygulamalarının devre dışı bırakılması](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]