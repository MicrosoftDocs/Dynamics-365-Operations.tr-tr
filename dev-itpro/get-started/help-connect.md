---
title: "Yardım sistemini bağlama"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations için Yardım sisteminin bileşenleri açıklar ve bu bileşenleri nasıl bağlanacağınıza genel bakış ve özel yardımın nasıl oluşturulacağının bir özetini sunar."
author: margoc
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: acb832c422ccb5ddb98d6ddd6b69d2e2c3e11057
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="connect-the-help-system"></a>Yardım sistemini bağlama

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Dynamics 365 for Finance and Operations'un Yardım sisteminin bileşenlerini açıklamaktadır. Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar. 

## <a name="help-architecture"></a>Yardım mimarisi
Aşağıdaki çizim, Finance and Operations Yardım sisteminin bölümlerini gösterir. Ürün içi Yardım sistemi, Dynamics 365 Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de ve https://docs.microsoft.com adresinde bulunan görev kayıtlarıyla Finance and Operations makalelerini çeker. 
> [!NOTE]
> Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir. [![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Yardım sistemine bağlanma
> [!NOTE]
> **Görev kılavuzları** sekmesi Microsoft Dynamics 365 for Talent ve Microsoft Dynamics 365 for Retail için henüz kullanılabilir değildir. Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz. Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği kapsamak üzere kullanılabilir kalır. Yordamlama yardımı da docs.microsoft.com sitesinde, hem Retail hem Talen için kullanılabilir ([docs.microsoft.com/dynamics365/operations](/dynamics365/unified-operations/fin-and-ops/index)).
 

**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar. [![Sistem Parametreleri formu Yardım ayarları](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **Sistem parametreleri** sayfasında şu adımları izleyin:

> [!IMPORTANT]
> **Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir. Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem Parametreleri** sayfasına ulaşmak için **Tamam**'a tıklayın.[![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Bağlanmak için Lifecycle Hizmetleri projesini seçin.
2.  Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.
    - Finance and Operations için, Microsoft içeriği için, 2017 QPC Unified Library for Microsoft Dynamics for Finance and Operations'u seçin. 
    - Retail için bir kütüphaneyi Temmuz'da yayımlayacağız. 
    - Talent için bir kütüphane seçmeniz gerekmez; doğru kütüphane ile bağlantı sizin için gerçekleştirilir. 

3.  BPM kitaplıklarının görüntülenme sırasını ayarlayın. Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.

Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesini tıklatabilirsiniz. Finance and Operations'ta o anda bulunduğunuz sayfayla ilgili görev kılavuzlarını görürsünüz. Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.

### <a name="showing-translated-task-guides"></a>Çevrilmiş görev kılavuzları gösteriliyor

Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir. Finance and Operations içinde yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs kitaplığına bağlı olduğunuzdan emin olun. Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir. 

> [!NOTE]
> Pek çok görev kılavuzu çevrilmiş olsa da şu anda Finance and Operations istemcisi çevrilmiş görev kılavuz adlarını göstermemektedir. Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir. Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.
> -   Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.
> -   Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.

## <a name="creating-custom-help"></a>Özel yardım oluşturma
Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance and Operations ve Retail uygulamanız için özel yardım oluşturabilirsiniz. Talent için özel görev kılavuzları oluşturamazsınız. 

Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır. Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz. Daha fazla bilgi için bkz. [Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../user-interface/task-recorder.md).

<a name="see-also"></a>Ayrıca bkz.
--------

[Yardıma genel bakış](help-overview.md)

[Görev kaydedici genel bakışı](../user-interface/task-recorder.md)

[Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../user-interface/task-recorder-training-docs.md)





