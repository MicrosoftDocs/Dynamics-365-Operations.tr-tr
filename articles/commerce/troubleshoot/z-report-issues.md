---
title: Z raporunun veri mutabakatı ile ilgili sorunlar
description: Bu makalede, kullanıcıların Commerce Headquarters'ta bir Z raporunun veri mutabakatıyla karşılaşabilecekleri sorunlar açıklanır. Ayrıca, gelecekteki oluşumların engellenmesine yardımcı olabilecek olası kök nedenler ve çözümler da açıklanmaktadır.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832145"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Z raporunun veri mutabakatı ile ilgili sorunlar

[!include [banner](../../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce Headquarters'taki bir Z raporunun veri mutabakatıyla ilgili sorunlar yaşarsanız yardımcı olabilecek sorun giderme kılavuzu sağlanmaktadır. Kullanıcıların veri mutabakatlarıyla karşılaşabilecekleri, olası kök nedenlerinde ve gelecekteki oluşumların engellenmesine yardımcı olabilecek sorunları açıklar.

## <a name="description"></a>Açıklama

- Z raporunda gösterilen tutarlar ve hesaplanan deyimde gösterilen toplamlar arasında uyuşmazlık var.
- Yönetim Merkezindeki hareket, yanlış sayıda satır öğelerine sahip veya satır toplamıyla hareketle ilgili toplam arasında uyuşmazlık var.
- Yönetim Merkezindeki bir vardiyada gösterilen hareket sayısı, Z raporundaki hareket sayısından azdır.
- Ekstre deftere nakli önceki nedenlerden biri nedeniyle başarısız oldu.

### <a name="root-cause"></a>Ana neden

Daha önce açıklanan belirtilerin en yaygın ana nedeni, kanal veritabanında tekrarlanan işlem kimliklerinin oluşturulmasına neden olur. Yinelenen hareket kimlikleri aşağıdaki nedenler sebebiyle oluşabilir:

- Modern Satış Noktası (MPOS) yerel veri tabanı depolaması bozulmuştur.
- MPOS çevrimdışı modda bazı hareketler sağlar ve çevrimdışı veritabanına erişimi olmayan bir hesap kullanılarak yeniden etkinleştirilir.
- Hareket kodlarının oluşturulmasına ilişkin özelleştirmeyle ilgili bir sorun var.

## <a name="resolution"></a>Çözüm

Genellikle Commerce, sıralı hareket kodları oluşturmak için bir numara serisine dayanır. Sistem herhangi bir nedenle bir numara serisinin kullanıldığını belirleyemez ise tekrarlanan bir hareket kodu oluşturulur. 

Tekrarlanan hareket kodu sorununu düzeltmek için, hareket verilerinin düzelip düzeltilmediğini denetlemek için bir destek bileti oluşturun. Bazı durumlarda (örneğin, Headquarters'ta veri kaybı olmaması gibi), veri onarımı mümkün değildir veya gerekli değildir.

Gelecekte bu sorunun engellenmesine yardımcı olmak için, Yönetim Merkezindeki **Yinelenen hareket kodları önlemek üzere yeni hareket kodunu etkinleştir** seçeneğini etkinleştirmelisiniz. Bu özellik, Commerce sürüm 10.0.19'te eklenmiştir. Her hareket için benzersiz bir hareket kodu oluşturulmasını sağlayarak, sıralı hareket kodlarının oluşturulmasını önlemeye yardımcı olur. Bu özellik hakkında daha fazla bilgi için bkz. [Yinelenen hareket kimliklerini önleme](../channel-setup-retail.md#ensure-unique-transaction-ids).
