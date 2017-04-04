---
title: "Maliyet muhasebesi analiz güç BI içerik için güvenliği ayarlama"
description: "Bu konu Microsoft Power çift satır düzeyinde güvenlik için Maliyet muhasebesinde erişim düzeyi güvenliğini nasıl yaymak açıklamaktadır. Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen güç BI veri bkz: garantilemeye yarar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Maliyet muhasebesi analiz güç BI içerik için güvenliği ayarlama

Bu konu Microsoft Power çift satır düzeyinde güvenlik için Maliyet muhasebesinde erişim düzeyi güvenliğini nasıl yaymak açıklamaktadır. Bu işlevsellik, kullanıcıların yalnızca erişim izni verilen güç BI veri bkz: garantilemeye yarar.

<a name="overview"></a>Özet
--------

**Maliyet muhasebesi analiz** Microsoft Power BI içerik kullanıcının erişimini sınırlamak için güç BI satır düzeyinde güvenlik kullanır. Maliyet muhasebesi parametrelerinde ayarlanan erişim düzeyini organizasyon hiyerarşisine güvenlik dayanır. Hakkında daha fazla bilgi için **Maliyet muhasebesi analiz** içerik, bkz: güç BI [güç BI içeriği Maliyet muhasebesi analiz](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Kurulum
Güç BI güvenlik erişim düzeyinde yaymak için güç BI içeriğin sahibi adımları izlemelisiniz. **Not:** yayımlayan kullanıcının **Maliyet muhasebesi analiz** güç BI içeriği otomatik olarak sahip olur. Yalnızca bir sahip güvenlik güç BI de ayarlayabilirsiniz. Ayrıca, bir sahip diğer kullanıcılar PowerBI.com ekler kadar sahibi dışında kimsenin herhangi bir veri görebilirsiniz **Maliyet muhasebesi analiz** güç BI içeriği.

1.  Tanım dosyası için güç BI yayımlayın.
2.  PowerBI.com için oturum açın.
3.  Dataset için bulmak **Maliyet muhasebesi analiz** güç BI içeriği.
4.  Güvenlik sayfasını açın. 

    [![Güvenlik sayfasını açma](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  **Maliyet nesne denetleyicisi** rolü zaten oluşturulmuş. Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisinin bir parçası olan diğer üyeler ekleyin. 

    [![Üye ekleme](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Eklenen kullanıcılar **maliyet nesne denetleyicisi** rol tanımı içinde Maliyet muhasebesi erişim düzeyi organizasyon hiyerarşisine göre görmek için izin verilen veri görürsünüz. **Not:** satır düzeyinde güvenlik için döşeme uygular ve Microsoft Dynamics 365 güç BI gömülü işlemleri için raporlar.

## <a name="updating-security"></a>Güvenlik güncelleştirme
Maliyet muhasebesindeki erişim düzeyi güvenliği için yapılan güncelleştirmeler ve güncelleştirmeleri yansıtmak için güç BI istiyorsanız varlık mağaza için güncelleştirmeniz gerekir **Maliyet muhasebesi analiz** güç BI içeriği. Dynamics 365 işlemleri için varlık deposu güncelleştirmeyi tamamladıktan sonra PowerBI.com üzerinde yapıları güncelleştirmeniz gerekir. Bir varlık deposu güncelleştirme yapmak hakkında daha fazla bilgi için bkz: [güncelleştirme varlık deposu](power-bi-integration-entity-store.md#update-entity-store). Sahibi **Maliyet muhasebesi analiz** güç BI içerik gerekir de yaparsanız bir varlık deposu güncelleştirme yeni kullanıcılar için organizasyon hiyerarşisine erişim verilir. Ayrıca sahibi yeni kullanıcılar eklemeniz gerekir **maliyet nesne denetleyicisi** rolü PowerBI.com, böylece onlar için o satır düzeyinde güvenlik uygulanır.

## <a name="disabling-security"></a>Güvenliği devre dışı bırakma
Biz, kuruluşunuzun veri erişimi kısıtlamak istediğini varsayalım. Maliyet muhasebesi çalıştırdığınızda güvenlik parametreleri herhangi bir nedenle devre dışıysa, sahibi kullanıcılar eklemeniz gerekir **maliyet muhasebecisi** güç çift rol bunun yerine. Güvenliği etkinleştirilmiş bir durumdan devre dışı durumuna değiştirirseniz, kullanıcıyı kaldırmak için iyi bir fikir olduğunu **maliyet nesne denetleyicisi** rolü. Ve bunun tersi de güvenlik yeniden etkinleştirirseniz. Kullanıcıların her iki rollere ait olabilir. Her iki rolleri birleşimini Joint erişimidir. Durumunda **Maliyet muhasebesi analiz** güç BI içerik joint erişimine sahip kullanıcılar sınırsız veri erişimi. Hedefiniz erişim sınırlaması uygulamak için ise, kullanıcıların yalnızca atanması gerekir **maliyet nesne denetleyicisi** rolü. Bu satır düzeyinde güvenlik güncelleştirmelerini hemen etkili olur. Etkilenen kullanıcılar tarayıcılarını yenilemeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar
Güç BI satır düzeyinde güvenlik hakkında daha fazla bilgi için bkz: [güç BI modelinizde güvenliği yönetmek](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


