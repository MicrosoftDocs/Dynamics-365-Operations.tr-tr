---
title: "Attract'ta genişletilebilirlik"
description: "Bu konu, Microsoft Dynamics 365 for Talent - Attract uygulamasını Microsoft Power platformunu kullanarak nasıl genişletebileceğinizi açıklar."
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
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: tr-tr
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Attract'ta genişletilebilirlik

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent, Uygulamalar İçin Common Data Service (CDS) platformu üzerine kuruludur ve Microsoft Power Platform gücü ve Uygulamalar İçin Common Data Service (CDS) sunduğu özellikler kullanılarak çeşitli şekillerde genişletilebilir. Bu nedenle, Microsoft PowerApps ve Microsoft Flow kullanarak sistemi yapılandırabilir ve kişiselleştirebilirsiniz. Ayrıca Microsoft Power BI kullanarak kişilerle ilgili ilave analitik alabilirsiniz. Ayrıca, PowerApps ve Web içeriği (iframe) gibi yeni özel etkinlikler işe alma işlemini her zamankinden daha uyarlanabilir yapar. Bu etkinlikleri kullanarak iş gereksinimlerinizi ve işlemleri işe alma işlemine uyarlayabilirsiniz ve hem işe alma ekibi hem adayların sorunsuz ve özelleştirilmiş deneyim yaşadığından emin olabilirsiniz.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power platformdan yararlanın 

Attract'taki tüm veriler Common Data Service for Apps'te bulunduğundan kendi iş ihtiyaçlarınıza Attract ile birleştirmek için Microsoft Power platformdan araçları kullanabilirsiniz.

### <a name="powerapps"></a>PowerApps

Attract verilerinize bağlanan ve mantık eklemek için Microsoft Excel'deki ifadeler gibi ifadeler kullanan uygulamaları kolayca oluşturmak için PowerApps kullanabilirsiniz. PowerApps kullanarak oluşturduğunuz uygulamaları web, Apple iOS ve Google Android cihazlarda çalıştırabilirsiniz.

Örneğin, üniversite mesleki fuarlarının işe alanlar için daha kolay olmasını sağlayın: Özgeçmişleri taramalarını ve adayları Attract'taki bir pozisyona göndermelerini sağlayan hafif bir uygulama oluşturun. Alternatif olarak, kuruluşunuzun uyumluluk gereksinimlerini karşılamaya yardımcı olan bir uygulama oluşturabilirsiniz. PowerApps ve bu uygulamaları oluşturmak için nasıl kullanılacağı hakkında daha fazla bilgi için [Common Data Service for Apps'e veri entegre edin](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Microsoft Flow'u, Attract verilerinin üstünde çalışan otomatik iş akışları oluşturmak için kullanabilirsiniz. Yüzlerce sık kullanılan uygulamalar ve hizmetlere kod yazmak zorunda olmadan kolayca bağlanabilirsiniz. Common Data Service for Apps'teki Attract işi, Aday ve Başvuru varlıklarıyla etkileşimde olan akışlar oluşturarak, çeşitli eylemleri otomatikleştirebilirsiniz. Örneğin, bir aday teklifi kabul ettiğinde, işe alma takımına bir bildirim gönderilir veya haber Twitter'da bildirilir. Akışlar hakkında daha fazla bilgi için, [Microsoft Flow belgelerine](https://docs.microsoft.com/en-us/flow/) bakın.

### <a name="power-bi"></a>Power BI

Power BI, Attract verilerinizle daha ayrıntılı bir anlayış sağlayan özel raporlar ve panolar oluşturma ve görüntüleme olanağı sağlar. Power BI ve etkileşimli raporlar ve panolar oluşturma hakkında daha fazla bilgi için bkz [Power BI belgeleri](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Özel faaliyetler 

İş işlem şablonu düzeyinde veya yeni bir iş oluşturduğunuz sırada PowerApps uygulamaları ve Web içeriği (iframe) etkinlikleri gibi özel etkinlikler ekleyebilirsiniz. Bu etkinlikler işe alma işlemini özelleştirmenizi ve Attract'a, kuruluşunuzun benzersiz iş mantığını getirmenizi sağlar.

#### <a name="powerapps-activity"></a>PowerApps faaliyeti 

PowerApps faaliyeti, işi veya iş süreci şablonu oluşturanın işe alma akışı içine bir PowerApps uygulaması gömmesini sağlar. Uygulamayı oluşturup yayınladığınızda uygulama kimliğini faaliyet konfigürasyonlarına girebilirsiniz. Bir PowerApps uygulaması kullanarak, verileri Common Data Service for Apps'te okuyabilir ve yazabilirsiniz. Uygulamayı bir akışa bağlayabilirsiniz. Örneğin, iş verenlerin telefon görüşmeleri gerçekleştirirken form doldurmak için kullandığı bir uygulamanız var. Bu durumda, uygulamayı başvuranın bir iş başvuru sürecinde ileriye alınabilir olup olmadığını belirlemek için akışa bağlayabilirsiniz. Bu aktivite türü yalnızca işe alma ekibinin üyeleri tarafından görüntülenebilir. PowerApps faaliyetini yapılandırma hakkında daha fazla bilgi için bkz. [Attract'taki faaliyetler](./activities-attract.md).

> [!NOTE]
> PowerApps faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

#### <a name="web-content-iframe-activity"></a>Web içeriği (iframe) faaliyeti

Web içeriği (iframe) faaliyeti, iş alım sürecinde veya Aday portalında oluşturduğunuz özel bir web çözümü gömmenizi sağlar. Veri okuma ve yazmayı doğrudan Common Data Service for Apps'ten yapabilirsiniz. Ayrıca, akışları tetikleyen veya Microsoft Azure işlevlerinden yararlanan çözümü özelleştirebilirsiniz. Web içeriği faaliyetini yapılandırma hakkında daha fazla bilgi için bkz. [Attract'taki faaliyetler](./activities-attract.md).

> [!NOTE]
> Web içeriği faaliyeti, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.

