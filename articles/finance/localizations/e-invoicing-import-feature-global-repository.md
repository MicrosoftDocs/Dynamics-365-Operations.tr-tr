---
title: Özellikleri Genel depodan içeri aktarma
description: Bu makalede, Genel depodan Genelleştirme özelliklerinin nasıl içeri aktarılacağı açıklanmaktadır.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278326"
---
# <a name="import-features-from-the-global-repository"></a>Özellikleri Genel depodan içeri aktarma

[!include [banner](../includes/banner.md)]

Genel depo, yapılandırma sağlayıcınızla paylaşılan Elektronik faturalama özellikleri içerir. Microsoft tarafından sağlanan tüm Elektronik faturalama özellikleri tüm şirketlerle paylaşılır. Microsoft'un genel havuzda yayımlanan ve yayımladığı tüm Elektronik faturalama özelliklerine otomatik olarak erişebilirsiniz.

Yapılandırma sağlayıcınızla paylaşılan Elektronik faturalama özellikleriyle çalışmaya başlamak için, bunları Genel depodan Regulatory Configuration Service (RCS) örneğine alın. Sonra, Elektronik raporlama (ER) yapılandırmaları ve işlem ardışık düzenleri gibi özellik ayrıntılarını gözden geçirin.

## <a name="import-a-feature-from-the-global-repository"></a>Bir özelliği Genel depodan içeri aktarma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Genel depodan içe aktarma özelliği** aramasını açmak için **İçe aktar**'ı seçin.
4. Belirli bir yapılandırma sağlayıcısının Genel depoda bulunan Elektronik faturalama özelliklerine göz atması için kuruluşunuzun RCS örneğini eşitlemek üzere **Eşitle**'yi seçin. Eşitleme tamamlandıktan sonra, kullanılabilir Elektronik faturalama özelliklerinin listesi Genel depodan güncelleştirilir. Bu güncelleştirme birkaç dakika sürebilir.
5. İçe aktarılacak özelliği ve ardından **İçe aktar** seçeneğini belirleyin.

İçe aktarılan Elektronik faturalama özelliğini görüntülemek için doğru yapılandırma sağlayıcısının seçildiğinden emin olun. Varsayılan olarak, etkin konfigürasyon sağlayıcısı tarafından oluşturulan özellikler otomatik olarak filtrelenir. Microsoft konfigürasyon sağlayıcısı gibi diğer sağlayıcılar tarafından oluşturulan özellikleri görüntülemek için filtreyi ayarlayabilirsiniz.

Artık içe aktarılan özellikle çalışabilirsiniz. İçe aktarılan özelliği şablon olarak kullanarak ayrıntılarını gözden geçirebilir ve yeni bir özellik oluşturabilirsiniz.

> [!NOTE]
> Bir özelliği yalnızca şu anda etkin olan bir konfigürasyon sağlayıcısı tarafından oluşturulmuşsa değiştirebilirsiniz. Özgün özelliği temel olarak kullanarak yeni bir özellik oluşturabilirsiniz. Daha sonra gerekli değişiklikleri yapabilir veya parametreleri ayarlayabilirsiniz.

Genelleştirme özelliklerini şirketinizle paylaşan Microsoft veya başka bir şirket içe aktardığınız özellikleri güncelleştirdiğinde, güncelleştirilmiş sürümleri kontrol etmek için **Genelleştirme özellikleri** çalışma alanındaki **İlgili ayarlar** bölümünde **Özellik güncelleştirmelerini kontrol et**'i seçebilirsiniz.

Şablon olarak kullandığınız bir özellik için güncelleştirmeler olduğunu görürseniz, Genel depodaki yayınlanan özelliklerin listesini eşitledikten sonra yeni bir sürüm alabilirsiniz.
