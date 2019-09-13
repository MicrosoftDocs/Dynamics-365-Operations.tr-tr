---
title: Kuruluşlar ve kuruluş hiyerarşilerine genel bakış
description: Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17291
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e35abeef2ef79dd994fac7d0ee0578591427b595
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864780"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Kuruluşlar ve kuruluş hiyerarşilerine genel bakış

[!include [banner](../includes/banner.md)]

Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.

## <a name="organizations"></a>Kuruluşlar

Microsoft Dynamics 365 for Finance and Operations'te, şu dahili organizasyon türlerini tanımlayabilirsiniz: tüzel kişilikler, işletme birimleri ve ekipler.

Tüm dahili organizasyonlar **Taraf** varlığı türleridir. Bu nedenle, bu organizasyonlar adres ve iletişim bilgilerini depolamak için adres defterini kullanırlar. Kişi ya da organizasyon olabilecek olan bir taraf, bir veya daha fazla adres defterine ait olabilir.

### <a name="legal-entities"></a>Tüzel kişilikler

Tüzel kişilik, kayıtlı veya asal bir yapıya sahip olan bir organizasyondur. Tüzel kişilikler yasal sözleşmelere girebilir ve performanslarını raporlayacak bildirimler hazırlamaları gerekir.

Bir şirket, tüzel kişilik türüdür. Bu Microsoft Dynamics 365 for Finance and Operations sürümünde, oluşturabileceğiniz tek tüzel kişilik türü şirketlerdir ve her bir tüzel kişilik bir şirket kimliği ile ilişkilendirilir. Bu ilişkilendirmenin nedeni programdaki bazı işlevsel alanların şirket kimliğini veya DataAreaId'ı kendi veri modellerinde kullanmasıdır. Bu işlevsel alanlarda, şirketler veri güvenliği için bir sınır olarak kullanılır. Kullanıcılar, yalnızca oturum açmış oldukları şirketin verilerine erişebilir.

### <a name="operating-units"></a>İşletme birimleri

Bir işletme birimi bir işletmenin ekonomik kaynaklarının ve yönetimsel işlemlerinin kontrolünü bölmek için kullanılan bir kuruluştur. Bir işletme birimindeki kişiler az bulunur kaynakların kullanımını en üst düzeye çıkarmak, süreçleri geliştirmek ve performansları için hesap verme görevlerine sahiptirler.

Microsoft Dynamics 365 for Finance and Operations altında, işletme birimleri türleri maliyet merkezlerini, iş birimlerini, değer akışlarını, departmanları ve perakende kanallarını içerir. Aşağıdaki tabloda her bir işletme birimi türü hakkında daha fazla bilgi bulabilirsiniz.

| Faaliyet birimi türü | Açıklama | Amaç |
|---------------------|-------------|---------|
| Maliyet merkezi         | Yöneticilerin bütçelenmiş ve fiili harcamalardan sorumlu olduğu bir işletme birimi. | Tüzel kişilikleri kapsayan iş süreçlerinin yönetimi ve operasyonel kontrolü için kullanılır. |
| İş birimi       | Stratejik iş hedeflerini karşılamak için oluşturulan yarı özerk bir işletme birimi. | Organizasyonun tüzel kişiliklerden bağımsız olarak hizmet verdiği sektörlere veya üretim hatlarına dayalı mali raporlama için kullanılır. |
| Değer akışı        | Bir veya birden fazla üretim akışını kontrol eden bir işletme birimi. | Yaygın olarak, bir ürün veya hizmeti müşteriye sunmak için gereken faaliyetleri ve akışları kontrol etmek üzere yalın imalatta kullanılır. |
| Departman          | Bir organizasyonun, satış veya muhasebe gibi belirli bir görevi gerçekleştiren bir kategorisini veya işlevsel parçasını temsil eden bir işletme birimi. | İşlevsel alanları raporlamak için kullanılır. Bir departmanın kar ve zarar sorumluluğu olabilir ve bir maliyet merkezleri grubundan oluşabilir. |
| Perakende kanalı      | Bir tuğla ve dibek mağazasını, bir çevrimiçi mağazayı veya çevrimiçi bir pazarı temsil eden bir işletme birimi. | Tüzel kişilikler dahilinde veya boyunca bir veya daha fazla mağazanın yönetimi ve operasyonel kontrolü için kullanılır. |

### <a name="teams"></a>Takımlar

Bir ekip, üyelerin ortak bir sorumluluğu, çıkarı veya hedefi paylaştığı bir organizasyondur. Ekipler organizasyonel hiyerarşilerde kullanılamaz.

## <a name="organizational-hierarchies"></a>Organizasyonel hiyerarşiler

İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyonel hiyerarşiler oluşturun. Örneğin, tüzel kişilikler için vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz. Yasal olarak gerekmeyen ama dahili kontrol için kullanılan mali bilgileri raporlamak için işletme birimlerine dayalı bir hiyerarşi oluşturun. Örneğin, satınalma politikalarını, kurallarını ve iş süreçlerini kontrol edecek bir satınalma hiyerarşisi oluşturabilirsiniz.

Her bir hiyerarşi, Microsoft Dynamics 365 for Finance and Operations için bir amaç taşımaktadır. Bir hiyerarşinin amacı, hiyerarşiye dahil edilebilecek organizasyon türlerini belirlemektir. Amaç ayrıca bir hiyerarşinin hangi uygulama senaryolarında kullanılabileceğini de belirler.

Bir hiyerarşi içindeki kuruluşlar parametreleri, politikaları ve hareketleri paylaşabilir. Bir organizasyon, ana organizasyonun parametrelerini devralabilir veya bu parametreleri değiştirebilir. Ancak, ürün ve adres defteri gibi paylaşılan master verileri, tüm organizasyon için geçerlidir ve tek tek organizasyonlar tarafından üstüne yazdırılamazlar. Organizasyon ve hiyerarşi oluşturmak dikkatli planlama gerektirir. Daha fazla bilgi için, bkz. [Organizasyonel hiyerarşiyi planlama](plan-organizational-hierarchy.md).
