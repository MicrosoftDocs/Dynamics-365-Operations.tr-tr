---
title: Logo ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 583462755838e51b4c988b8da057dbeeee773e0b
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964591"
---
# <a name="add-a-logo"></a>Logo ekleme

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.

Sitenizi yapılandırdığınızda, büyük olasılıkla yaptığınız ilk şeyden biri şirketinizi veya marka amblemini sitenin başlığına eklemektir. Dynamics 365 Commerce çevrimiçi modül kitaplığı, bu görevi kolaylaştıran bir modül sağlar.

Bir logoyu doğrudan bir şablon, düzen veya sayfaya ekleyebilirsiniz. Bu şekilde, belirli sayfalarda veya sayfa gruplarında görünen logoyu kolayca değiştirebilirsiniz. Ancak bu konu, logonuzu sitenizdeki tüm sayfalarda yeniden kullanılabilen bir başlık parçasına eklediğiniz en sık kullanılan senaryoyu kapsamaktadır.

## <a name="prerequisites"></a>Önkoşullar

Sitenizin tüm sayfalarına logo ekleyebilmeniz için önce bu görevleri tamamlamanız gerekir.

1. Logonuzu ortam kitaplığı 'na yükleyin.
1. Başlık parçası oluşturun. Parçaların nasıl oluşturulacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Parçalarla çalışma](work-with-fragments.md).
1. Başlık parçasının, mizanpaj ve modül seçenekleri için sitenizin sayfalarının kullandığı şablona dahil edin. Şablonlar hakkında daha fazla bilgi için, bkz. [Şablonlarla çalışma](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Üstbilgi parçasına Logo ekle

Sitenizin üstbilgi parçasına logo eklemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde **Parçalar** seçin.
1. Oluşturduğunuz başlığı seçin ve sonra **Düzenle**'yi seçin.
1. Üstbilgi modülünü genişletin.
1. Üstbilgi modülünün Özellik bölmesinde logo için bir resim ve bağlantı sağlayın. 
1. Başlık parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.

Güncelleştirilmiş başlık parçasını yayımladıktan sonra, başlık parçasını içeren şablonu kullanan tüm site sayfaları logonuzu gösterecektir.

## <a name="additional-resources"></a>Ek kaynaklar

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Favicon ekleme](add-favicon.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
