---
title: "Yardım sistemini bağlama"
description: "Bu konu, Microsoft Dynamics 365 for Operations için Yardım sisteminin bileşenleri açıklar ve bu bileşenleri nasıl bağlanacağınıza genel bakış ve özel yardımın nasıl oluşturulacağının bir özetini sunar."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Yardım sistemini bağlama

Bu konu, Microsoft Dynamics 365 işlemleri için Yardım sisteminin bileşenleri açıklar. Bu bileşenleri bağlamak nasıl bir bakış sağlar ve özel oluşturmak nasıl bir özetini yardımcı olur. 

<a name="help-architecture"></a>Yardım mimarisi
-----------------

Sistem işlemleri yardımcı olmak için Dynamics 365 bölümlerini aşağıda gösterilmiştir. Ürünün Yardım sisteminin işlemleri sitesinde https://docs.microsoft.com yanı sıra, iş süreci Modeler ömrü Hizmetleri (LCS) depolanan görev kılavuzları için Dynamics 365 gelen makaleleri çeker. 
**Not:** listelenen özellikleri diyagramdaki bir yıldız işareti (\*) planlanan, ancak henüz kullanılabilir değil. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Yardım sistemine bağlanma
Kullanarak **sistem parametreleri** sayfa, sistem yöneticileri bir uygulama için Yardım sisteminin parçaları bağlayın. [![Sistem parametreleri formundaki Yardım ayarları ile](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) üzerinde **sistem parametreleri** sayfasında, aşağıdaki adımları izleyin:

1.  **Önemli:** açtığınız ilk kez **yardımcı** sekmesinde, ömrü hizmetlerine bağlanmak gerekir. Formun ortasýndaki bağlantıyı tıklatın, bağlantı için bekleyin, iletişim kutusunu kapatmak ve ı mutlaka **Tamam** almak için **sistem parametreleri** sayfa. [![Bağlanmak için LCS](./media/connect-to-lcs-crop-1024x365.png "LCS için bağlanma")](./media/connect-to-lcs-crop.png)
2.  Bağlanmak için Lifecycle Hizmetleri projesini seçin.
3.  Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.
4.  BPM kitaplıklarının görüntülenme sırasını ayarlayın. Bu **Yardım** bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.

Bu adımları tamamladıktan sonra **Yardım** bölmesini açabilir ve **Görev kılavuzları** sekmesini tıklatabilirsiniz. Dynamics 365 for Operations'da o anda bulunduğunuz sayfaya uygulanan görev kılavuzlarını görürsünüz. Görev kılavuzu bulunamadıysa, anahtar sözcükler girerek aramanızı daraltabilirsiniz.

### <a name="showing-translated-task-guides"></a>Çevrilmiş görev kılavuzları gösteriliyor

Çevrilmiş görev kılavuzları içinde Mayıs 2016 ilk sevk edildiği APQC birleşik kitaplığı ve Başlarken kitaplığı. Dynamics 365 for Operations içinde yerelleştirilmiş görev kılavuzu yardımını görmek için Mayıs ayı kitaplığına bağlı olduğunuzdan emin olun. Görev kılavuz görünür dil, her kullanıcı için dil ayarları tarafından denetlenir **seçenekleri**&gt;**Tercihler**. **Not:** Pek çok görev kılavuzu çevrilmiş olsa da şu anda Dynamics 365 for Operations istemcisi çevrilmiş görev kılavuz adlarını göstermemektedir. Ayrıca, Şubat 2016'de yayımlanan görev kılavuzları çeviri Mayıs Kitaplığı'nda bulunur. Ek çevirilerle güncelleştirilmiş bir kitaplık yayımlayacağız.

-   Görev kılavuzu çevrildiyse, görev kılavuzunu açtığınızda, görev kılavuzundaki tüm metin seçmiş olduğunuz dilde görüntülenir.
-   Görev kılavuzu çevrilmediyse, açtığınızda, yalnızca bazı metinler (kontrollerin metinleri) seçmiş olduğunuz dilde görüntülenir.

## <a name="creating-custom-help"></a>Özel yardım oluşturma
Uygulamanızı yansıtan görev kayıtları oluşturarak ve bunları bir LCS İş Süreci Kitaplığına kaydederek Dynamics 365 for Operations uygulamanız için özel yardım oluşturabilirsiniz. Ortaklar için, bir kitaplığı şirket kitaplığına yükseltirseniz ve bir çözüme eklerseniz, müşterileriniz tarafından kullanılabilir olacaktır. Ayrıca APQC Birleştirilmiş global kitaplığın bir kopyasını oluşturabilirsiniz ve ardından kopyayı açabilir, kopyadan görev kayıtlarını açarak onları değiştirebilir ve değişiklik yaptığınız kayıtları kaydedebilirsiniz. Daha fazla bilgi için bkz: [eğitim veya belge olarak kullanmak için bir görev kaydı oluşturmak nasıl](../user-interface/task-recorder.md).

<a name="see-also"></a>Ayrıca bkz.
--------

[Help overview](help-overview.md)

[Görev Kaydedici genel bakış](../user-interface/task-recorder.md)

[Belge veya eğitim olarak kullanmak için görev kaydı oluşturma](../user-interface/task-recorder-training-docs.md)

[Dynamics 365 yaşam döngüsü (dış bağlantı) görev Kaydedicisi'ni kullanarak Hizmetleri içinde işlemleri için yeni eğitim kitaplıkları oluşturma](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


