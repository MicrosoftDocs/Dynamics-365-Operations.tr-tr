---
title: Deftere nakil tanımları
description: Bu makalede, nakil tanımları ve bu tanımların nasıl belirlenip bağlantı verildiği hakkında bilgiler verilmektedir. Desteklenen nakil türleri ve belgeler ile ilgili olarak, muhasebe girişlerindeki ana hesapları ve finansal boyutları sınıflandırmak için nakil profilleri yerine nakil tanımlarını kullanabilirsiniz.
author: ShylaThompson
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans, LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.custom: 15741
ms.assetid: 1495e7e0-2e39-464c-8da9-f55b1ca1c6bb
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22a261c1ac139d5caa51e05ff90675eca89e40fd804ff7e87a7c69a18c1f3e4e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753516"
---
# <a name="posting-definitions"></a>Deftere nakil tanımları

[!include [banner](../includes/banner.md)]

Bu makalede, nakil tanımları ve bu tanımların nasıl belirlenip bağlantı verildiği hakkında bilgiler verilmektedir.
Desteklenen nakil türleri ve belgeler ile ilgili olarak, muhasebe girişlerindeki ana hesapları ve finansal boyutları sınıflandırmak için nakil profilleri yerine nakil tanımlarını kullanabilirsiniz. Desteklenen belgeleri ve nakil türlerini **İşlem nakil tanımları** sayfasında görebilirsiniz. 

Nakil tanımlarını kullanmaya başlatmak için **Genel muhasebe parametreleri** sayfasındaki **Nakil tanımlarını kullan** seçeneğini seçin. Nakil tanımlarını kullanıyor olsanız dahi, orijinal girişler ve desteklenmeyen nakil türleri ve belgeleri için nakil profillerini yine de mutlaka tanımlanmanız gerekir. 

Satın alma siparişleri için sorumluluk muhasebesini ve satın alma talepleri için ön sorumluluk muhasebesini etkinleştirmek için nakil tanımlarını kullanmalısınız.

## <a name="defining-posting-definitions"></a>Nakil tanımlarının tanımlanması
Eşleşme kriterlerini belirlemek ve bir eşleşme meydana geldiğinde oluşturulması gereken girişleri tanımlamak için **Nakil tanımları** sayfasını kullanın. Eşleştirme kriterleri, muhasebe dağılımları olarak orijinal girişler için değerlendirilir. 

**Nakil tanımları** sayfasında ayrıca satırların değerlendirileceği siparişi kontrol etmek için giriş satırlarına öncelik numaraları da atayabilirsiniz. En düşük öncelik numarasına sahip satırlar ilk olarak değerlendirilir. Örneğin, önceliği 1 olan tüm satırlar değerlendirilir ve ardından önceliği 2 olan satırlar değerlendirilir ve işlem bu şekilde devam eder. Bir eşleşme bulunduğunda, diğer eşleştirme ölçütleri dikkate alınmaz. Ayrıca, sadece grupta orijinal işlemle eşleşen kriterleri üretilen girişleri oluşturur. 

**Nakil tanımını test et** sihirbazını kullanarak nakil tanımlarınızı doğrulayabilirsiniz. Bir nakil tanımı için bir örnek orijinal giriş tanımladıktan sonra oluşturulan girişleri görürsünüz. 

Nakil tanımı sürülerini geçerlilik tarihleri ile birlikte kullanabilirsiniz. Örneğin, yeni bir mali yılda farklı bir muhasebe hesabına nakletmek üzere bir nakil tanımının gelecek bir sürümünü oluşturabilirsiniz. 

İşlem türlerine nakil tanımları atamak için **İşlem nakil tanımları** sayfasını kullanın.

## <a name="linking-posting-definitions"></a>Nakil tanımlarının ilişkilendirilmesi
Nakil tanımları oluştururken bir nakil tanımını başka bir nakil tanımıyla ilişkilendirebilirsiniz. İlişkilendirdiğiniz tanım için kriterler, mevcut nakil tanımına ait kriterlere ilave olarak düşünülür. Bu özellik zaman kazandırır, çünkü başka bir tanım için halihazırda girdiğiniz için, **Nakil tanımları** sayfasında **Girişler** hızlı sekmesi altına kriterleri mevcut nakil tanımı için tekrar girmenize gerek kalmaz. 

Şemalarda veya tablolarda kullanabilirsiniz tüm bağlantılar bulunur. Mevcut nakil tanımı ile çakışmaları önlemek için ilişkilendirdiğiniz nakil tanımlarındaki satırların benzersiz olduğundan emin olun. 

Aşağıdaki kısıtlamalar, nakil tanımlarında bağlantılar oluştururken geçerlidir:

-   Verilen nakil tanımı başka bir nakil tanımına veya başka bir nakil tanımından bağlanabilir, ancak her ikisi aynı anda gerçekleştirilemez. Ancak, bir nakil tanımı birden fazla nakil tanımına bağlanabilir.
-   Bağlantıları sadece aynı modülde bulunan nakil tanımları arasında ayarlayabilirsiniz.
-   Bir nakil tanımını herhangi bir işlem türüne atayabilirsiniz, ancak işlem türünün mutlaka nakil tanımıyla aynı modülde olması gerekir. Bir işlem türünün hangi modülde olduğunu görmek için **İşlem nakil tanımları** sayfasını kullanın.


Daha fazla bilgi için bkz. [Deftere nakil tanımı örnekleri](example-posting-definitions.md). 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]