---
title: Genelleştirme özelliği bileşenleri
description: Bu makalede, Genelleştirme özellik bileşenlerine dair genel bir bakış sağlanmaktadır.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891502"
---
# <a name="globalization-feature-components"></a>Genelleştirme özelliği bileşenleri

[!include [banner](../includes/banner.md)]

Genelleştirme özelliği, Elektronik raporlama (ER) konfigürasyonlarında veri dönüşümü kurallarını tanımlayan bir bileşen kümesidir. Bu bileşenler, elektronik belgeleri işlemek ve sonra bunları harici kanallardan almak veya göndermek için yönergeler içerir. Bunlar ayrıca, gelen iş verileri için bir özelliğin ne zaman çalıştırılması gerektiğini tanımlayan koşulları içerir.

Tüm bileşenler birbirine bağlıdır. Genelleştirme özellikleri bu bağımlılığın oluşturulmasını ve korunmasını, kullanım ömrü yönetimi ve bileşen kümesinin sürüm oluşturma özelliklerini desteklemek için kolaylaştırır.

## <a name="access-electronic-invoicing-feature-components"></a>Elektronik faturalama özellik bileşenlerine erişim 

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.

    Genelleştirme özelliklerinin birkaç bileşeni vardır. **Elektronik faturalama özellikleri** sayfası, her bileşen için ayrı bir sekme içerir.

    - **Sürüm** – Bu bileşen, özelliğin yaşam döngüsü yönetimini destekler. Bu özelliği, özelliğin farklı sürümlerinin durumunu yönetmek için kullanabilirsiniz.
    - **Yapılandırmalar** – Bu bileşen, işlem kanalında kullanılan ilgili ER formatını ve biçim eşleme yapılandırmalarını yönetmenizi, görüntülemenizi ve düzenlemenizi sağlar.
    - **Ayarlar** – Bu bileşen, bir e-faturalama hizmeti gibi, Genelleştirme servisleri kullanıcılarının ilgili özellik sürümünün kurulumunu yönetme gibi kullanıcılara olanak tanır. Bu nedenle, iletişim ve yanıt kurallarının esnek yapımını destekler.
    - **Ortamlar** – Bu bileşen, bir e-faturalama hizmeti gibi Genelleştirme Hizmetleri kullanıcılarının, özellik sürümü kurulumunun kullanıldığı ortamı yönetmesine olanak tanır. Ayrıca, özellik sürümü kurulumuna erişimi olacak kullanıcılara yetkilendirme izni verir.
    - **Kuruluşlar** – Bu bileşen, kullanıcıların özelliği harici organizasyonlarla paylaşmasına olanak tanır.
    - **Etiketler** – Bu bileşen referans için Genelleştirme şemasında kullanılabilen özellikleri etiketlemenizi sağlar.
