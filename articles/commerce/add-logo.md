---
title: Logo ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914639"
---
# <a name="add-a-logo"></a>Logo ekleme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize logo ekleme yöntemi açıklanmıştır.

## <a name="overview"></a>Genel Bakış

Sitenizi yapılandırdığınızda, büyük olasılıkla yaptığınız ilk şeyden biri şirketinizi veya marka amblemini sitenin başlığına eklemektir. Dynamics 365 Commerce çevrimiçi başlangıç kiti, bu görevi kolaylaştıran bir modül sağlar.

Bir logoyu doğrudan bir şablon, düzen veya sayfaya ekleyebilirsiniz. Bu şekilde, belirli sayfalarda veya sayfa gruplarında görünen logoyu kolayca değiştirebilirsiniz. Ancak bu konu, logonuzu sitenizdeki tüm sayfalarda yeniden kullanılabilen bir başlık parçasına eklediğiniz en sık kullanılan senaryoyu kapsamaktadır.

## <a name="prerequisites"></a>Önkoşullar

Sitenizin tüm sayfalarına logo ekleyebilmeniz için önce bu görevleri tamamlamanız gerekir.

1. Ambleminizi, **varlıklar** sayfasından erişebileceğiniz dijital varlıklar yöneticisine yükleyin.
1. Başlık parçası oluşturun. Parçaların nasıl oluşturulacağı ve kullanılacağı hakkında daha fazla bilgi için bkz. [Parçalarla çalışma](work-with-fragments.md).
1. Başlık parçasının, mizanpaj ve modül seçenekleri için sitenizin sayfalarının kullandığı şablona dahil edin. Şablonlar hakkında daha fazla bilgi için, bkz. [Şablonlarla çalışma](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Üstbilgi parçasına Logo ekle

Sitenizin üstbilgi parçasına logo eklemek için aşağıdaki adımları izleyin.

1. Soldaki gezinti bölmesinde, **Parçalar**'ı seçin ve sonra oluşturduğunuz başlık parçasını seçin.
2. **Ödeme yap** seçin.
3. **Üstbilgi** yuvasını ve **amblem** yuvasını genişletin.
4. **Logo** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
5. Logo modülünü seçin.
6. Daha sonra sağdaki Özellikler bölmesinde, logo modülünü logonuzu gösterecek şekilde yapılandırın.
7. Üstbilgi parçasını kaydedin, giriş yapın ve yayımlayın.

Güncelleştirilmiş başlık parçasını yayımladıktan sonra, başlık parçasını içeren şablonu kullanan tüm site sayfaları logonuzu gösterecektir.

## <a name="additional-resources"></a>Ek kaynaklar

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Favicon ekleme](add-favicon.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)

