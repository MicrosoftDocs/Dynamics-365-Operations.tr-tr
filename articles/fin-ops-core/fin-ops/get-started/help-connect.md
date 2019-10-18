---
title: Yardım sistemini bağlama
description: Bu konuda Finance and Operations uygulamaları için Yardım sistemin bileşenleri açıklanmakta, bu bileşenlere nasıl bağlanacağınıza ilişkin bir genel bakış ve özel yardımın nasıl oluşturulacağının bir özeti verilmektedir.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537867"
---
# <a name="connect-the-help-system"></a>Yardım sistemini bağlama

[!include [banner](../includes/banner.md)]

Bu konu Dynamics 365 Finance, Supply Chain Management, Retail ve Talent gibi Finance and Operations uygulamaları için Yardım sistemi bileşenlerini açıklar. Bu bileşenlere nasıl bağlanılacağı ve özel yardım oluşturma hakkında genel bir bakış sağlar.

## <a name="help-architecture"></a>Yardım mimarisi

Aşağıdaki örnek Yardım sisteminin bölümlerini gösterir. Ürün içi Yardım sistemi, Lifecycle Services'deki (LCS) İş Süreci Modelleyici'de depolanan görev kılavuzlarını ve https://docs.microsoft.com adresindeki makaleleri çeker.

> [!NOTE]
> Not: Diyagramda yıldız işareti (\*) ile listelenen özellikler planlanmıştır, ancak henüz kullanılabilir değildir.

[![Yardım mimarisi](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Yardım sistemine bağlanma

> [!NOTE]
> **Görev kılavuzları** sekmesi, şu anda Dynamics 365 Talent veya Retail için kullanılamaz. Bu işlevi gelecekteki bir sürümde etkinleştirmek için çalışıyoruz. Başlarken deneyimindeki Görev kılavuzları, temel işlevselliği kapsamak üzere kullanılabilir kalır. Ayrıca, hem Retail hem de Talent için docs.microsoft.com sitesinde yordamsal yardım bulunur.

**Sistem Parametreleri** sayfasını kullanarak, sistem yöneticileri bir uygulama için Yardım sisteminin parçalarını bağlar.

[![Yardım ayarlarıyla Sistem Parametreleri formu](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

**Sistem parametreleri** sayfası üzerinde, aşağıdaki adımları izleyin:

> [!IMPORTANT]
> **Yardım** sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir. Formun ortasındaki bağlantıya tıkladığınızdan emin olun, bağlantı için bekleyin, iletişim kutusunu kapatın ve **Sistem parametreleri**sayfasına ulaşmak için **Tamam** üzerine tıklayın.
>
> [![LCS'ye bağlan](./media/connect-to-lcs-crop-1024x365.png "LCS'ye bağlan")](./media/connect-to-lcs-crop.png)

1. Bağlanmak için Lifecycle Hizmetleri projesini seçin.
2. Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.
3. BPM kitaplıklarının görüntülenme sırasını ayarlayın. Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.

Bu adımları tamamladıktan sonra, **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesine tıklayabilirsiniz. Şimdi, Finance and Operations uygulamalarında içinde bulunduğunuz sayfa için geçerli olan görev kılavuzlarını göreceksiniz. Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.

### <a name="showing-translated-task-guides"></a>Çevrilmiş görev kılavuzları gösteriliyor

Çevrilmiş görev kılavuzları ilk olarak Mayıs 2016 APQC Birleştirilmiş Kitaplığı'na ve Başlangıç kitaplığına sevk edilmiştir. Finance and Operations uygulamalarında yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs kitaplığına bağlı olduğunuzdan emin olun. Görev kılavuzunun görüntülendiği dil her kullanıcı için **Seçenekler** &gt; **Tercihler** altındaki Dil ayarlarından kontrol edilir.

> [!NOTE]
> Pek çok görev kılavuzu çevrilmiş olsa da şu anda istemci çevrilmiş görev kılavuz adlarını göstermemektedir. Ayrıca, yalnızca Şubat 2016'da yayımlanan görev kılavuzları, Mayıs ayı Kitaplığı'nda çeviri olarak kullanılabilir. Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.
>
> - Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.
> - Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.

## <a name="creating-custom-help"></a>Özel yardım oluşturma

Görev kılavuzlarını özel yardım oluşturmak veya bir web sitesini Yardım panosuna bağlamak için kullanabilirsiniz.

### <a name="create-custom-help-with-task-guides"></a>Görev kılavuzlarıyla özel yardım oluşturmak

Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Finance, Supply Chain Management ve Retail uygulamanız için özel yardım oluşturabilirsiniz. Talent için özel görev kılavuzları oluşturamazsınız.

Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır. Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz. Daha fazla bilgi için bkz. [Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Özel bir siteye bağlanmak

Microsoft, özel yardım sitesini oluşturma ve bağlamak hakkında bir teknik inceleme ve örnek kodu sağlamıştır. Daha fazla bilgi için bkz:

- [Finance and Operations uygulamaları için Özel Yardım Oluşturma (teknik inceleme)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Özel yardım GitHub havuzu](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Ek kaynaklar

[Yardıma genel bakış](help-overview.md)

[Görev kaydedici genel bakışı](../../dev-itpro/user-interface/task-recorder.md)

[Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../../dev-itpro/user-interface/task-recorder-training-docs.md)
