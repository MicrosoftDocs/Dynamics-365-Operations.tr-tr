---
title: Attract'te genişletilebilirlik
description: Bu konu, Microsoft Dynamics 365 Talent- Attract'i Microsoft Power Platform'u kullanarak nasıl genişletebileceğinizi açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ddc6593431585ed79cc15f7ede5daf856f11b959
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527254"
---
# <a name="extensibility-in-attract"></a>Attract'te genişletilebilirlik

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Talent, Common Data Service üzerine kuruludur ve Microsoft Power Platform ve Common Data Service için sunduğu özellikler kullanılarak çeşitli şekillerde genişletilebilir. Bu nedenle, Microsoft Power Apps ve Microsoft Power Automate kullanarak sistemi yapılandırabilir ve kişiselleştirebilirsiniz. Ayrıca Microsoft Power BI kullanarak kişilerle ilgili ilave analitik alabilirsiniz. Ayrıca, Power Apps ve Web içeriği (iframe) gibi yeni özel etkinlikler işe alma işlemini her zamankinden daha uyarlanabilir yapar. Bu etkinlikleri kullanarak iş gereksinimlerinizi ve işlemleri işe alma işlemine uyarlayabilirsiniz ve hem işe alma ekibi hem adayların sorunsuz ve özelleştirilmiş deneyim yaşadığından emin olabilirsiniz.

## <a name="extending-option-sets-in-attract"></a>Attract'te seçenek kümelerini genişletmek

Bir **Seçenek Kümesi** (seçme listesi) bir varlığa dahil edilebilecek bir alan türüdür. Bir seçenek kümesini tanımlar. Bir seçenek kümesi, bir formda görüntülendiğinde bir açılır liste denetimi kullanır.  Attract içinde seçenek kümesi olan birden çok alan vardır.  Yeni yeterlilikler, seçenek kümelerini genişletmek için sunmaya başlıyoruz, Reddetme sebep alanı, İstihdam türü alanı ve Kıdem türü alanı.   Ayrıca, eklediğiniz seçenekler için yerelleştirilmiş görüntü etiketleri ekleyebilirsiniz. Daha fazla bilgi için bkz. [Seçenek kümesi etiketlerini özelleştir](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> LinkedIn'e iş ilanı verme özelliği, **İstihdam türü** ve **Kıdem türü** alanının **İş ayrıntıları** sayfasında kullanılmasını gerektirir. Bu alanlardaki varsayılan değerler, LinkedIn tarafından desteklenir ve iş ilanı verildiğinde görüntülenir. Bu nedenle, LinkedIn'e iş ilanları veriyorsanız ve mevcut seçenek kümesi değerlerini bu alanlar için değiştiriyorsanız, iş ilanı yine de verilecektir ancak LinkedIn, özel **İstihdam türü** ve **Kıdem türü** değerlerini görüntülemez.  

Aşağıda, **Reddetme sebebi** alanını işinizle ilgili değerler ile güncelleştirmek için adımlar listelenmiştir.  

1. **Reddetme sebebi** seçenek kümesini genişletmek için [Power Apps Yönetici web sitesi](https://admin.powerapps.com)'ne gidin.
2. Hesabınıza oturum açmanız istenebilir. Dynamics365 ve/veya Office365 içine oturum açmak için kullanıcı adı ve parolanızı verin ve sonra **İlerle**'ye tıklayın.
3. **Ortam** sekmesinde, yönetmek istediğiniz ortamı seçin ve **Ayrıntılar** sekmesine ulaşmak için çift tıklayın.
4. **Ayrıntılar** sekmesinde, **Dynamics 365 Yönetim Merkezi**'ni seçin.
5. Değiştirmek istediğiniz kurulumu seçin ve **Aç**'ı seçin.
6. **Ayarlar**'a gidin ve sonra **Özelleştirmeler**'e gidin ve sonra **Sistemi özelleştir**'i seçin.
7. **Varlıklar**'ı seçerek seçenek kümesini genişletmek istediğiniz varlığı bulun ve grubu genişletin. Bu örnekte, **İş başvurusu varlığı** olacaktır.
8. **Alanlar** seçeneğini seçerek, genişletmek istediğiniz seçenek kümesinin alanına gidin. Bu örnekte **msdyn_rejectionreason** olacaktır. Alana çift tıklayın.
9. **Seçenek Kümesi** alanında **Düzenle**'yi seçin.
10. **+** simgesini seçin.
11. Bir **Etiket** girin.  (Bu, benzersiz bir değer olmalıdır - yineleme olmadan).
12. **Kaydet**'i seçin.
13. Sayfanın üstündeki **Yayımla**'yı seçin.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform avantajlarından yararlanın 

Attract'teki tüm veriler Common Data Service bulunduğundan kendi iş ihtiyaçlarınıza Attract ile birleştirmek için Microsoft Power Platform'dan araçları kullanabilirsiniz.

### <a name="power-apps"></a>Power Apps

Attract verilerinize bağlanan ve mantık eklemek için Microsoft Excel'deki ifadeler gibi ifadeler kullanan uygulamaları kolayca oluşturmak için Power Apps kullanabilirsiniz. Power Apps kullanarak oluşturduğunuz uygulamaları web, Apple iOS ve Google Android cihazlarda çalıştırabilirsiniz.

Örneğin, üniversite mesleki fuarlarının işe alanlar için daha kolay olmasını sağlayın: Özgeçmişleri taramalarını ve adayları Attract'teki bir pozisyona göndermelerini sağlayan hafif bir uygulama oluşturun. Alternatif olarak, kuruluşunuzun uyumluluk gereksinimlerini karşılamaya yardımcı olan bir uygulama oluşturabilirsiniz. Power Apps ve uygulamaları oluşturmak için nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Common Data Service'a veri tümleştirme](https://docs.microsoft.com/powerapps).

### <a name="microsoft-power-automate"></a>Microsoft Power Automate 

Microsoft Power Automate'i, Attract verilerinin üstünde çalışan otomatik iş akışları oluşturmak için kullanabilirsiniz. Yüzlerce sık kullanılan uygulamalar ve hizmetlere kod yazmak zorunda olmadan kolayca bağlanabilirsiniz. Common Data Service içinde, Attract işi, Aday ve Başvuru varlıklarıyla etkileşimde olan akışlar oluşturarak, çeşitli eylemleri otomatikleştirebilirsiniz. Örneğin, bir aday teklifi kabul ettiğinde, işe alma takımına bir bildirim gönderilir veya haber Twitter'da bildirilir. Akışlar hakkında daha fazla bilgi için bkz. [Microsoft Power Automate belgeleri](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>Power BI

Power BI, Attract verilerinizle daha ayrıntılı bir anlayış sağlayan özel raporlar ve panolar oluşturma ve görüntüleme olanağı sağlar. Power BI ve etkileşimli raporlar ve panolar oluşturma hakkında daha fazla bilgi için bkz [Power BIbelgeleri](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Özel faaliyetler 

İş işlem şablonu düzeyinde veya yeni bir iş oluşturduğunuz sırada Power Apps uygulamaları ve Web içeriği (iframe) etkinlikleri gibi özel etkinlikler ekleyebilirsiniz. Bu etkinlikler işe alma işlemini özelleştirmenizi ve Attract'e, kuruluşunuzun benzersiz iş mantığını getirmenizi sağlar.

#### <a name="power-apps-activity"></a>Power Apps etkinliği 

Power Apps faaliyeti, işi veya iş süreci şablonu oluşturanın işe alma akışı içine bir Power Apps uygulaması katıştırmasını sağlar. Uygulamayı oluşturup yayınladığınızda uygulama kimliğini faaliyet konfigürasyonlarına girebilirsiniz. Bir Power Apps uygulaması kullanarak, verileri okuyabilir ve Common Data Service'a yazabilirsiniz. Uygulamayı bir akışa bağlayabilirsiniz. Örneğin, iş verenlerin telefon görüşmeleri gerçekleştirirken form doldurmak için kullandığı bir uygulamanız var. Bu durumda, uygulamayı başvuranın bir iş başvuru sürecinde ileriye alınabilir olup olmadığını belirlemek için akışa bağlayabilirsiniz. Bu aktivite türü yalnızca işe alma ekibinin üyeleri tarafından görüntülenebilir. Power Apps faaliyetini yapılandırma hakkında daha fazla bilgi için bkz. [İşe alım süreçlerindeki faaliyetler](./activities-attract.md).

> [!NOTE]
> Power Apps faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

#### <a name="web-content-iframe-activity"></a>Web içeriği (iframe) faaliyeti

Web içeriği (iframe) faaliyeti, iş alım sürecinde veya Aday portalında oluşturduğunuz özel bir web çözümü gömmenizi sağlar. Veri okuma ve yazmayı doğrudan Common Data Service yapabilirsiniz. Ayrıca, akışları tetikleyen veya Microsoft Azure işlevlerinden yararlanan çözümü özelleştirebilirsiniz. Web içeriği faaliyetini yapılandırma hakkında daha fazla bilgi için bkz. [İşe alım süreçlerindeki faaliyetler](./activities-attract.md).

> [!NOTE]
> Web içeriği faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.
