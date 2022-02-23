---
title: Dynamics 365 Supply Chain Management'ı (Varlık yönetimi) Dynamics 365 Guides ile tümleştirme
description: Bu konu, günlük servis ve bakım iş akışlarınızda karma gerçeklik kılavuzlarından yararlanmak için Microsoft Dynamics 365 Supply Chain Management'taki Varlık yönetimi modülünün Dynamics 365 Guides ile nasıl tümleştirileceğini açıklar.
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f9ee7f1af8e88f56589c84bfaa063ea005aa353a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439127"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Dynamics 365 Supply Chain Management'ı (Varlık yönetimi) Dynamics 365 Guides ile tümleştirme

Günlük servis ve bakım iş akışlarınızda karma gerçeklik kılavuzlarından yararlanmak için Microsoft Dynamics 365 Supply Chain Management'taki **Varlık yönetimi** modülünü Dynamics 365 Guides ile tümleştirebilirsiniz. Bir kılavuz Varlık yönetimi iş emriyle ilişkilendirilmişse, Supply Chain Management (Dynamics 365) mobil uygulamasında iş emrinin bakım denetim listesini açan bir çalışan bir kılavuzun kullanılabilir olduğunu görür. Çalışan daha sonra kılavuzu Dynamics 365 Guides HoloLens uygulamasında bulabilir ve açabilir.

## <a name="prerequisites"></a>Önkoşullar

Kılavuzları Varlık yönetimi iş emirlerine ekleyebilmeniz için önce aşağıdaki önkoşulları tamamlamanız gerekir:

- [Dynamics 365 Supply Chain Management](../../fin-ops-core/fin-ops/index.md) sürüm 10.0.9 veya üstünü kurun.
- [Supply Chain Management uygulamaları için çift yazmayı açın](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md).
- **MRGuidesFeature** özelliği için [sınırlı dağıtımı açın](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features). (Üretim ortamları için, kiracınızın sınırlı dağırım grubuna eklenmesini sağlamak için öncelikle bir destek bileti göndermeniz gerekir.)
- **Lisans yapılandırması** sayfasında [aşağıdaki yapılandırma anahtarlarını açın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference) :

    - Varlık yönetimi \>Varlık yönetimi karma gerçeklik
    - Karma gerçeklik \> Karma gerçeklik kılavuzu

- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) sürüm 200.0.0.96 veya üstünü kurun.

## <a name="use-dynamics-365-guides-with-asset-management"></a>Dynamics 365 Guides'ı Varlık yönetimi ile kullanma

Bir kılavuzu ilişkilendirmek için, Varlık yönetimindeki bir bakım denetim listesi satırını kullanırsınız. İlişkilendirmeyi bakım denetim listesi şablonu, bakım iş türü veya iş emri aracılığıyla oluşturabilirsiniz, çünkü her üçü de bakım denetim listesi satırları içerir. Bir şablon onu kullanan tüm bakım işi türleriyle ilişkilendirilebileceğinden bir şablon kullanarak zamandan tasarruf edebilirsiniz. Örneğin, bir bakım işi türü ile ilişkilendirilmiş bir kılavuz, iş türünü belirten tüm iş emirleriyle otomatik olarak ilişkilendirilir. Diğer taraftan, bir iş emriyle doğrudan ilişkilendirilmiş olan bir kılavuz yalnızca o iş emri için geçerlidir.

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>Kılavuzu bakım denetim listesi şablonuyla ilişkilendirme

Kılavuzu bakım denetim listesi şablonuyla ilişkilendirmek için aşağıdaki adımları izleyin.

1. Dynamics 365 Guides PC ve HoloLens uygulamalarını kullanarak bir kılavuz oluşturun. Kılavuz oluşturma hakkında daha fazla bilgi için aşağıdaki konulara bakın:

    - [Kılavuz oluşturmak için PC uygulaması kullanma](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [Hologramlarınızı yerleştirmek için HoloLens uygulaması kullanma](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Supply Chain Management'ta [bir bakım denetim listesi şablonu oluşturun](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template).
1. Oluşturduğunuz kılavuzu yeni bakım denetim listesi şablonundaki bir bakım denetim listesi satırı ile ilişkilendirin:

    1. **Bakım denetim listesi satırları** hızlı sekmesinde, kılavuzu ilişkilendirmek istediğiniz satırı seçin.
    1. **İlişkili kılavuzlar** hızlı sekmesinde, **Kılavuz Ekle**'yi seçin.

        ![Kılavuzu bakım denetim listesi satırıyla ilişkilendirme](media/am-guides-integration-add-guide.png "Kılavuzu bakım denetim listesi satırıyla ilişkilendirme")

    1. **Ad** alanında bir kılavuz seçin ve ardından **Kaydet**'i seçin.

        ![Ad alanında bir kılavuz seçme](media/am-guides-integration-select-guide.png "Ad alanında bir kılavuz seçme")

1. Bakım denetim listesi şablonunu bir iş türüyle ilişkilendirme:

    1. [Bir bakım işi türü oluşturun](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type) veya varolan bir bakım işi türünü seçin.
    1. Eylem Bölmesinde **Bakım işi türü varsayılanları**'nı seçin.

        ![Bakım işi türü varsayılanları düğmesi](media/am-guides-integration-job-defaults.png "Bakım işi türü varsayılanları düğmesi")

    1. Bir satır oluşturun ve **Kaydet**'i seçin.

        ![Satır oluşturma](media/am-guides-integration-add-line.png "Satır oluşturma")

    1. Eylem Bölmesinde, **Bakım denetim listesi**'ni seçin.

        ![Bakım denetim listesi düğmesi](media/am-guides-integration-maintenance-checklist.png "Bakım denetim listesi düğmesi")

    1. **Bakım denetim listesi satırları** hızlı sekmesinde, bir satır ekleyin ve sonra **Tür** alanının değerini **Şablon** olarak değiştirin.

        ![Tür değerini değiştirme](media/am-guides-integration-checklist-lines.png "Tür değerini değiştirme")

    1. **Satır ayrıntıları** hızlı sekmesinde, **Şablon** alanında, kılavuzla ilişkilendirdiğiniz şablonu ve ardından **Kaydet**'i seçin.

        ![Şablon seçme](media/am-guides-integration-checklist-line-details.png "Şablon seçme")

1. [Bir iş emri oluşturun ](work-orders/manually-created-workorders.md#create-work-order) ve ardından kılavuzla ilişkilendirdiğiniz bakım denetim listesi şablonunu kullanan bakım işi türünü seçin. Kılavuz, iş emriyle otomatik olarak ilişkilendirilir.

    ![Bakım işi türü seçme](media/am-guides-integration-create-work-order.png "Bakım işi türü seçme")

1. İş emri ve çalışanlar ile ilişkilendirilmiş kılavuzu görüntüleyin:

    1. İş emrine erişmek için [Varlık yönetimi mobil çalışma alanını](asset-management-mobile-workspace.md) açın.
    1. İş emri için [bakım denetim listesini açın](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job).
    1. İlişkili kılavuzu görmek için bir denetim listesi satırı seçin.

        ![Denetim listesi satırıyla ilişkilendirilmiş kılavuz](media/am-guides-integration-show-guide.png "Denetim listesi satırıyla ilişkilendirilmiş kılavuz")

    1. Kılavuzu HoloLens'te açın.

        ![Kılavuzu HoloLens'te açın](media/am-guides-integration-hololens-select.png "Kılavuzu HoloLens'te açma")

> [!NOTE]
> Ayrıca, bir kılavuzu doğrudan bir iş emrinin veya iş türünün bakım denetim listesinde ilişkilendirebilirsiniz.

> [!IMPORTANT]
> Bir bakım denetim listesi şablonunu varsayılan bir bakım işi türü ile ilişkilendirdiğinizde, şablonla bağlantılı olan kılavuzun **Bakım işi türü varsayılanları** sayfasındaki **İlişkilendirilmiş kılavuzlar** hızlı sekmesinde görünmediğiyle ilgili bilinen bir sorun vardır. Ancak, bu iş türü **İlişkilendirilmiş kılavuzlar** hızlı sekmesindeki bir iş emrine uygulandıktan sonra kılavuz görüntülenecektir.

## <a name="see-also"></a>Ayrıca bkz.

- [Çift yazmaya genel bakış](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [Varlık yönetimine genel bakış](index.md)
