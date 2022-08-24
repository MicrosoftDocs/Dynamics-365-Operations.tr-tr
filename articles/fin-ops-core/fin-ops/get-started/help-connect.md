---
title: Finans ve operasyon uygulamaları için Yardım deneyimini yönetme
description: Bu makalede, bazı Microsoft Dynamics 365 uygulamaları için Yardım sisteminin bileşenleri hakkında bilgi verilmektedir.
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 35dc37f6669a3f47dd82917be0e84d0b8698e8f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282480"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için Yardım deneyimini yönetme

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Bu makalede; Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources gibi finans ve operasyon uygulamaları için Yardım sisteminin bileşenlerine dair genel bir bakış sunulmaktadır. Bu makalede, bu bileşenlerin nasıl bağlanacağı açıklanmakta ve özel Yardım oluşturma sürecinin bir özetini sağlanmaktadır.

## <a name="help-architecture"></a>Yardım mimarisi

Finans ve operasyon uygulamaları, [Microsoft Dynamics 365 belgeleri](/dynamics365/) sitesinde yayınlanan kavramsal genel bakışları ve diğer konuları içerir. Bu içeriğe daha sonra ürün içi **Yardım** bölmesinden erişilebilir. Aşağıdaki örnek Yardım sisteminin bölümlerini gösterir.

[![Yardım mimarisi.](./media/help-architecture.png)](./media/help-architecture.png)

Ürün içi Yardım sistemi, docs.microsoft.com ve bağlı diğer web sitelerinden makaleler alır. Ayrıca Microsoft Dynamics Lifecycle Services (LCS) içindeki İş Süreci Modelleyici'de (BPM) saklanan görev kılavuzlarını da çeker.

## <a name="adding-task-guides"></a>Görev kılavuzları ekleme

> [!NOTE]
> **Görev kılavuzları** sekmesi şu anda Human Resources veya Commerce'te mevcut değildir. <!--We are currently working to enable this functionality in a future release.--> Ancak, Human Resources'ın Başlarken deneyimindeki görev kılavuzları, temel işlevselliği sağlamak üzere kullanılabilir kalıyor. Hem Human Resources hem de Commerce için [Microsoft Dynamics 365 belgeleri](/dynamics365/) sitesinde yordamsal Yardım mevcuttur.

**Sistem parametreleri** sayfasında sistem yöneticileri, bir uygulama için ilgili görev kılavuzu kitaplıklarına erişimi yapılandırabilir.

> [!NOTE]
> - Yardım'ı yapılandırmak için uygulamanın dağıtıldığı kiracıyla aynı kiracıda bir hesap kullanarak oturum açmanız gerekir.
> - LCS kitaplığına, uygulamanın yerel bir sanal sabit sürücüde (VHD) çalışan bir örneğinden bağlanılamaz.

[![Yardım ayarlarıyla Sistem Parametreleri formu.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Çözüm için görev kılavuzlarını yapılandırmak üzere **Sistem parametreleri** sayfasındaki şu adımları izleyin.

> [!IMPORTANT]
> **Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir. Formun ortasındaki bağlantıyı seçtiğinizden emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri** sayfasına ulaşmak için **Tamam**'ı seçin.
>
> [![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlanın.")](./media/connect-to-lcs-crop.png)

1. Bağlanmak için Lifecycle Hizmetleri projesini seçin.
2. Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.
3. BPM kitaplıklarının görüntülenme sırasını ayarlayın. Görüntüleme sırası, kitaplıklardaki görev kayıtlarının **Yardım** bölmesinde hangi sırayla görüneceğini belirler.

Bu adımları tamamladıktan sonra, **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesini seçebilirsiniz. Şimdi, finans ve operasyon uygulamalarında içinde bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz. Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.

### <a name="showing-translated-task-guides"></a>Çevrilmiş görev kılavuzları gösteriliyor

Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'nda ve Başlangıç Kitaplığı'nda yayımlandı. Yerelleştirilmiş görev kılavuzu Yardım öğesini görüntülemek için Dynamics 365 çözümünüzün Mayıs 2016 kitaplığına bağlı olduğundan emin olun. Kullanıcılar, **Seçenekler** &gt; **Tercihler** altındaki dil ayarlarını değiştirerek görev kılavuzunun görüntülendiği dili değiştirebilir.

> [!NOTE]
> Birçok görev kılavuzu çevrilmiş olmasına rağmen istemci, şu anda çevrilmiş görev kılavuzu adlarını göstermez. Ayrıca Mayıs 2016 kitaplığındaki çeviriler yalnızca Şubat 2016'da yayımlanan görev kılavuzları için mevcuttur. Microsoft, ek çeviriler içeren güncelleştirilmiş bir kitaplık yayımlayacak.
>
> - Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.
> - Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.

## <a name="adding-custom-help"></a>Özel Yardım ekleme

Özel Yardım oluşturmak için görev kılavuzlarını kullanabilir veya **Yardım** bölmesine, özel bir Yardım web sitesi bağlayabilirsiniz.

### <a name="create-custom-help-by-using-task-guides"></a>Görev kılavuzları kullanarak özel Yardım oluşturma

Uygulamanızı yansıtan görev kayıtları oluşturarak ve ardından bunları LCS'deki bir İş süreci kitaplığına kaydederek desteklenen uygulamalar için özel Yardım oluşturabilirsiniz. Human Resources için özel görev kılavuzları oluşturamazsınız.

Bir ortaksanız ve bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz müşterileriniz tarafından kullanılabilir olacaktır. Ayrıca APQC Birleştirilmiş Kitaplığı'nın bir kopyasını oluşturabilir ve ardından kopyadaki görev kayıtlarını açabilir, düzenleyebilir ve değişikliklerinizi kaydedebilirsiniz. Daha fazla bilgi için bkz. [Görev kaydedici kaynakları](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Özel bir Yardım sitesini bağlama

Finans ve operasyon uygulamaları, nadiren kullanıma hazır biçimlerinde kullanılır. Bunun yerine çözüm, kuruluşun ihtiyaçlarına göre özelleştirilir ve genişletilir. Yardım deneyimini de özelleştirebilir ve genişletebilirsiniz. Örneğin, ürün içi **Yardım** bölmesine özel Yardım ekleyebilirsiniz.

Microsoft, özel Yardım'ı **Yardım** bölmesine dağıtmanıza ve bağlamanıza yardımcı olacak bir araç seti sağlamıştır. **Yardım** bölmesine bağlı özel bir Yardım çözümünü nasıl ayarlayabileceğiniz hakkında bilgi için bkz. [Özel Yardım'a genel bakış](../../dev-itpro/help/custom-help-overview.md).

Yardım'ı özelleştirmek için araçlar ve işlemler konusunda Microsoft ile işbirliği yapmak istiyorsanız [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) adresindeki formu doldurun.

## <a name="see-also"></a>Ayrıca bkz.

[Yardım sistemi](help-overview.md)  
[Özel Yardım'a genel bakış](../../dev-itpro/help/custom-help-overview.md)  
[Görev kaydedici kaynakları](../../dev-itpro/user-interface/task-recorder.md)  
[Görev Kaydedici ile belge veya eğitim oluşturma](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Özel Yardım, GitHub havuzu](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

