---
title: Kuruluşlar ve kuruluş hiyerarşilerine genel bakış
description: Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.
author: sericks007
ms.date: 01/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8e8f2c2004582f42c3f464fedf9f3d049b5278f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7992089"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Kuruluşlar ve kuruluş hiyerarşilerine genel bakış

[!include [banner](../includes/banner.md)]

Bir organizasyon, bir iş sürecini gerçekleştirmek veya bir hedefe ulaşmak için birlikte çalışan bir grup insandır. Organizasyonel hiyerarşiler, işinizi meydana getiren organizasyonlar arasındaki ilişkileri temsil eder.

## <a name="organizations"></a>Kuruluşlar

Tüzel kişilikler, işletme birimleri ve ekipler gibi dahili kuruluş türlerini tanımlayabilirsiniz.

Tüm dahili organizasyonlar **Taraf** varlığı türleridir. Bu nedenle, bu organizasyonlar adres ve iletişim bilgilerini depolamak için adres defterini kullanırlar. Kişi ya da organizasyon olabilecek olan bir taraf, bir veya daha fazla adres defterine ait olabilir.

### <a name="legal-entities"></a>Tüzel kişilikler

Tüzel kişilik, kayıtlı veya asal bir yapıya sahip olan bir organizasyondur. Tüzel kişilikler yasal sözleşmelere girebilir ve performanslarını raporlayacak bildirimler hazırlamaları gerekir.

Bir şirket, tüzel kişilik türüdür. Şu anda oluşturabileceğiniz tek tüzel kişilik türü şirketlerdir ve her bir tüzel kişilik, bir şirket kimliği ile ilişkilendirilir. Bu ilişkilendirmenin nedeni programdaki bazı işlevsel alanların şirket kimliğini veya DataAreaId'ı kendi veri modellerinde kullanmasıdır. Bu işlevsel alanlarda, şirketler veri güvenliği için bir sınır olarak kullanılır. Kullanıcılar, yalnızca oturum açmış oldukları şirketin verilerine erişebilir.

### <a name="operating-units"></a>İşletme birimleri

Bir işletme birimi bir işletmenin ekonomik kaynaklarının ve yönetimsel işlemlerinin kontrolünü bölmek için kullanılan bir kuruluştur. Bir işletme birimindeki kişiler az bulunur kaynakların kullanımını en üst düzeye çıkarmak, süreçleri geliştirmek ve performansları için hesap verme görevlerine sahiptirler.

İşletme birimi türleri arasında maliyet merkezleri, iş birimleri, değer akışları, departmanlar ve ticaret kanalları bulunur. Aşağıdaki tabloda her bir işletme birimi türü hakkında daha fazla bilgi bulabilirsiniz.

| Faaliyet birimi türü | Açıklama | Amaç |
|---------------------|-------------|---------|
| Maliyet merkezi         | Yöneticilerin bütçelenmiş ve fiili harcamalardan sorumlu olduğu bir işletme birimi. | Tüzel kişilikleri kapsayan iş süreçlerinin yönetimi ve operasyonel kontrolü için kullanılır. |
| İş birimi       | Stratejik iş hedeflerini karşılamak için oluşturulan yarı özerk bir işletme birimi. | Organizasyonun tüzel kişiliklerden bağımsız olarak hizmet verdiği sektörlere veya üretim hatlarına dayalı mali raporlama için kullanılır. |
| Değer akışı        | Bir veya birden fazla üretim akışını kontrol eden bir işletme birimi. | Yaygın olarak, bir ürün veya hizmeti müşteriye sunmak için gereken faaliyetleri ve akışları kontrol etmek üzere yalın imalatta kullanılır. |
| Departman          | Bir organizasyonun, satış veya muhasebe gibi belirli bir görevi gerçekleştiren bir kategorisini veya işlevsel parçasını temsil eden bir işletme birimi. | İşlevsel alanları raporlamak için kullanılır. Bir departmanın kar ve zarar sorumluluğu olabilir ve bir maliyet merkezleri grubundan oluşabilir. |
| Perakende kanalı      | Bir fiziksel mağazayı, bir çevrimiçi mağazayı veya çağrı merkezini temsil eden bir işletme birimi. | Tüzel kişilikler dahilinde veya boyunca bir veya daha fazla mağazanın yönetimi ve operasyonel kontrolü için kullanılır. |

### <a name="teams"></a>Takımlar

Bir ekip, üyelerin ortak bir sorumluluğu, çıkarı veya hedefi paylaştığı bir organizasyondur. Ekipler organizasyonel hiyerarşilerde kullanılamaz.

## <a name="organizational-hierarchies"></a>Organizasyonel hiyerarşiler

İşlerinize farklı perspektiflerden bakmak ve raporlamak için organizasyonel hiyerarşiler oluşturun. Örneğin, tüzel kişilikler için vergi, hukuki veya yasal raporlamaya yönelik bir hiyerarşi oluşturabilirsiniz. Yasal olarak gerekmeyen ama dahili kontrol için kullanılan mali bilgileri raporlamak için işletme birimlerine dayalı bir hiyerarşi oluşturun. Örneğin, satınalma politikalarını, kurallarını ve iş süreçlerini kontrol edecek bir satınalma hiyerarşisi oluşturabilirsiniz.

> [!NOTE]
> Bir çalışma birimi bir hiyerarşiye eklendikten sonra, çalışma birimi silinemez. 

Her bir hiyerarşi, bir amaç için atanmıştır. Bir hiyerarşinin amacı, hiyerarşiye dahil edilebilecek organizasyon türlerini belirlemektir. Amaç ayrıca bir hiyerarşinin hangi uygulama senaryolarında kullanılabileceğini de belirler.

Bir hiyerarşi içindeki kuruluşlar parametreleri, politikaları ve hareketleri paylaşabilir. Bir organizasyon, ana organizasyonun parametrelerini devralabilir veya bu parametreleri değiştirebilir. Ancak, ürün ve adres defteri gibi paylaşılan master verileri, tüm organizasyon için geçerlidir ve tek tek organizasyonlar tarafından üstüne yazdırılamazlar. Organizasyon ve hiyerarşi oluşturmak dikkatli planlama gerektirir. Daha fazla bilgi için bkz. [Kuruluş hiyerarşinizi planlama](plan-organizational-hierarchy.md).

## <a name="additional-resources"></a>Ek kaynaklar
- [Kuruluş hiyerarşinizi planlama](plan-organizational-hierarchy.md)
- [Kuruluş hiyerarşisi oluşturma](tasks/create-organization-hierarchy.md)
- [Bir tüzel kişilik oluşturma](tasks/create-legal-entity.md)
- [Faaliyet birimi oluşturma](tasks/create-operating-unit.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
