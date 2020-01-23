---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914551"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.

## <a name="overview"></a>Genel Bakış

Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır. Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir. Çoğu Web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<baş\>** öğesine istemci tarafı kodu eklemenizi gerektirir.

> [!NOTE]
> Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Komut dosyası kodunuz için yeniden kullanılabilir bir parça oluşturun

Kodunuz için bir parça oluşturduktan sonra, sitenizdeki tüm sayfalar arasında yeniden kullanılabilir.

1. **Parçalar \> Yeni sayfa parçası**'na gidin.
2. **Harici kod** seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.
3. Parça hiyerarşisinde, az önce oluşturduğunuz parçanın **Komut dosyası enjektörleri** alt modülünü seçin.
4. Sağdaki Özellik bölmesinde, istemci tarafı komut dosyanızı ekleyin ve istediğiniz şekilde diğer yapılandırma seçeneklerini ayarlayın.

## <a name="add-the-fragment-to-templates"></a>Parçayı şablonlara Ekle

1. **Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.
2. Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.
3. **HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **parça Ekle**'yi seçin.
4. Kodunuz için oluşturduğunuz parçayı seçin.
5. Şablonu kaydedin ve giriş yapın.

> [!NOTE]
> İşlemi bitirdikten sonra, parçayı ve ana şablonu yayımlamanız gerekir. 

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Favicon ekleme](add-favicon.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

