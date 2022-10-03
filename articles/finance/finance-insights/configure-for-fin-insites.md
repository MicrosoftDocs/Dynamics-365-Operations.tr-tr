---
title: Finance Insights için Yapılandırma
description: Bu makalede, sisteminizin Finance Insights'ta sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573207"
---
# <a name="configuration-for-finance-insights"></a>Finance Insights için Yapılandırma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights, kuruluşunuza güçlü tahmin araçları sunmak için Microsoft Dynamics 365 Finance işlevlerini Dataverse, Azure ve AI Builder işlevleriyle bir araya getirir. Bu makalede, sisteminizin Finance Insights'ta sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır. Bu makaledeki yordamları başarıyla tamamlamak için, [Power Portal yönetim merkezinde](https://admin.powerplatform.microsoft.com/) Sistem yöneticisi ve Sistem Özelleştirici erişimine, Dynamics 365 Finance'te Sistem Yöneticisi erişimine ve Microsoft Dynamics Lifecycle Services'te (LCS) ortam oluşturma erişimine sahip olmanız gerekir.

> [!NOTE]
> Finance Insights'ı ayarlamak için aşağıdaki yordamlar, 10.0.21 ve üzeri Microsoft Dynamics 365 Finance sürümleri için geçerlidir.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance'i dağıtma

Ortamları dağıtmak için aşağıdaki adımları uygulayın.

1. LCS'de bir Dynamics 365 Finance ortamı oluşturun veya güncelleştirin. Ortam, sürüm 10.0.21 veya daha sonraki sürüm gerektirir.

    > [!NOTE]
    > Ortam, yüksek kullanılabilirlik (HA) ortamı olmalıdır. (Bu ortam türü aynı zamanda Katman 2 ortamı olarak da bilinir.) Daha fazla bilgi için bkz. [Ortam planlama](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning).

2. Finance Insights'ı bir korumalı alanda yapılandırıyorsanız tahminlerin çalışabilmesi için üretim verilerini ilgili ortama kopyalamanız gerekebilir. Tahmin modeli, tahminleri oluşturmak için birkaç senelik verileri kullanır. Contoso demo verileri, tahmin modelini yeterince geliştirmek için yeterli tarihsel veri içermez. 

## <a name="configure-your-azure-ad-tenant"></a>Azure AD kiracınızı konfigüre edin

Dataverse ve Microsoft Power Platform uygulamaları ile kullanılabilmesi için Azure Active Directory'nin (Azure AD) yapılandırılması gerekir. Bu konfigürasyon, LCS içindeki **Proje güvenlik rolü** alanında kullanıcıya **Proje Sahibi** rolünün veya **Ortam Yöneticisi** rolünün atanmasını gerektirir.

Aşağıdaki kurulumun tamamlandığını doğrulayın:

- Power Portal yönetim merkezinde **Sistem yöneticisi** ve **Sistem Özelleştirici** erişiminiz var.
- Finance Insights eklentisini yükleyen kullanıcıya bir Dynamics 365 Finance veya eşdeğer bir lisans uygulanır.
- Aşağıdaki Azure AD uygulamaları, Azure AD'de kayıtlıdır.

    |  Uygulama                             | Uygulama kodu                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Mikro Hizmetleri CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Uygulamanın Azure AD'de kayıtlı olduğunu doğrulamak için **Tüm Uygulamalar** listesini kontrol edin. Daha fazla ayrıntı için bkz. [Kurumsal uygulamaları görüntüleme](/azure/active-directory/manage-apps/view-applications-portal).
  
    Uygulama Azure AD'de kayıtlı değilse desteğe başvurun.
  
## <a name="configure-dataverse"></a>Dataverse'ı yapılandırma

Finance Insights için Dataverse'ü yapılandırmak için aşağıdaki adımları uygulayın.

- LCS'de, ortam sayfasını açın ve **Power Platform Tümleştirme** bölümünün zaten ayarlı olduğunu doğrulayın.

    - Dataverse zaten ayarlıysa Finance ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.
    - Dataverse henüz ayarlı değilse **Kurulum**'u seçin. Dataverse ortamının kurulumu bir saate kadar sürebilir. Kurulum başarıyla tamamlandığında, Finance ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.
    - Bu tümleştirme varolan bir Microsoft Power Platform ortamıyla ayarlandıysa, bağlı ortamın devre dışı durumda olmadığından emin olmak için yöneticinize başvurun.

        Daha fazla bilgi için bkz. [Power Platform tümleştirmesini etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md). 

        Microsoft Power Platform yönetim sitesine erişmek için şuraya gidin: <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights eklentisini yapılandırma

Daha önce Finance Insights eklentisini yüklediyseniz, aşağıdaki yordamı gerçekleştirmeden önce bu eklentiyi kaldırın.

> [!NOTE]
> Veri gölü eklentisini LCS ile zaten yüklediyseniz, Finance Insights bunu tahmin etmek için gerekli verileri kaydetmek için kullanacaktır. Veri gölü eklentisini henüz LCS'de yüklemediyseniz, Finance Insights eklentisi sizin için yönetilen bir veri gölü oluşturacaktır.

Bu adımları izleyip, Finance Insights eklentisini yükleyin.

1. LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.
2. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.
3. **Finance Insights** eklentisini seçin.
4. Hüküm ve koşulları kabul edin ve sonra **Yükle**'yi seçin.

Eklentinin yüklenmesi birkaç dakika sürebilir.

## <a name="one-last-thing"></a>Bir son şey...

Eklenti başarıyla yüklendikten sonra, Dynamics 365 Finance'te **Özellik yönetimi** çalışma alanında Finance Insights özelliklerini etkinleştirebilmek bir saatten fazla sürebilir. Bu süreyi beklemek istemiyorsanız, **Insights sağlama durumu denetimi** işlemini el ile çalıştırabilirsiniz. 

1. Dynamics 365 Finance'te, **Sistem yönetimi \> Kurulum \> Süreç otomasyonu**'na gidin.
2. **Arka plan işlemleri** sekmesinde, **Insights sağlama durumu denetimini** bulun ve **Düzenle**'yi seçin.
3. **Sonraki yürütme** alanını geçerli saatten 30 dakika önce olacak şekilde ayarlayın.

   Bu değişiklik, **Insights sağlama durumu denetimi** işlemini hemen çalışacak şekilde zorlayacaktır.

   **Insights sağlama durumu denetimi** işlemi başarıyla çalıştırıldıktan sonra, **Özellik yönetimi** çalışma alanında Finance Insights özelliklerini etkinleştirebilirsiniz.

> [!NOTE]
> **İçgörü sağlama durumu kontrolü** işlemi çalışmazsa **Sistem yönetimi** > **Sorgular** > **Toplu işler** öğesine gidin. **Süreç otomasyonu yoklama sistemi** alanında, işlemi başlatmak için değeri **Bekleniyor** olarak değiştirin. 
> 
## <a name="feedback-and-support"></a>Geri bildirim ve destek

Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Finance Insights (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
