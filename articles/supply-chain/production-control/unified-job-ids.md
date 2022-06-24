---
title: İş kimlikleri için birleşik numara serisi
description: Bu özellik, üretim denetimi, üretim yürütmesi, zaman ve katılımcı modülleri için iş kimlikleri oluşturan tek, Birleşik bir numara serisi sağlar.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 301a4bb58f896a2dc0f0cddcd2e29344865ca898
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897559"
---
# <a name="unified-number-sequence-for-job-ids"></a>İş kimlikleri için birleşik numara serisi

[!include [banner](../includes/banner.md)]

Bu özellik, üretim denetimi, üretim yürütmesi, zaman ve katılımcı modülleri için iş kimlikleri oluşturan tek, Birleşik bir numara serisi sağlar. Daha önce, bu modüllerin her biri için farklı bir numara serisi seçebiliyordunuz ve bu da sıraların iki ya da daha fazlası özdeş bir biçim kullandığında iş kimliklerinin çakışmasına neden olabiliyordu. Bu tür bir çakışma veri bozulmasına neden olabilir.

## <a name="turn-on-this-feature-for-your-system"></a>Sisteminiz için bu özelliği etkinleştirme

Sisteminiz bu makalede açıklanan özelliği zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *İş kimlikleri için birleşik numara serisi* özelliğini açın.

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>İş kimlikleri için birleşik numara serisini ayarlama

Bu özellik etkinleştirildikten sonra, Üretim denetimi, üretim yürütmesi ve zaman ve katılımcı modülleri için parametreler sayfalarında bulunan varolan **iş tanımlayıcısı** numara serisi ayarları kullanım dışı bırakılır ve yeni bir **birleşik iş kodu** alanı eklenir. **Birleşik iş kodu** değeri tüm modüllerin aynı numara serisine başvuruda bulunduğunu garanti ederek bu üç modül tarafından paylaşılır. Bu nedenle, iş kimlikleri tüm üç modülde benzersiz olacaktır ve bir çakışma hiçbir zaman gerçekleşmez.

İş kimlikleri için birleşik numara serisini ayarlamak için:

1. Bu özelliği önceki bölümde açıklandığı gibi açın.
1. Birleştirilmiş iş kimlikleriniz için kullanmak istediğiniz numara serisini tanımlayın veya yeni bir tane oluşturun. Daha fazla bilgi için bkz. [Numara serilerine genel bakış](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).
1. **Üretim Denetim parametreleri**, **Üretim yürütme parametreleri** veya **zaman ve katılımcı parametreleri** sayfasına gidin. Hangisini seçtiğinizin bir önemi yoktur, çünkü bu ayarı bu sayfalardan herhangi birinde yaptığınızda, tüm diğer sayfalar otomatik olarak güncelleştirilir.
1. Seçili parametreler sayfanızdaki **numara serileri** sekmesini açın.
1. Daha önce tanımladığınız **numara serisi kodunu** kılavuzun **Birleşik iş kimlikleri** satırına atayın.
