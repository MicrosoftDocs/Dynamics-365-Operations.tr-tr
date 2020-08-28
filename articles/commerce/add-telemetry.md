---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686826"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme

[!include [banner](includes/banner.md)]

Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.

## <a name="overview"></a>Genel Bakış

Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır. Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir. Çoğu web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<head\>** öğesine istemci tarafı kodu eklemenizi gerektirir.

> [!NOTE]
> Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a>Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun

Sayfa parçası, kendi kullandıkları şablondan bağımsız olarak, sitenizdeki tüm sayfalar arasında satır içi veya harici kod kodunu yeniden kullanmanızı sağlar.

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a>Satır içi Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun

Site oluşturucuda satır içi betik kodunuz için yeniden kullanılabilir bir sayfa parçası oluşturmak üzere aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni sayfa parçası** iletişim kutusunda, **Satır içi betik**'i seçin.
1. **Sayfa parçası adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.
1. Oluşturduğunuz sayfa parçasının altında, **varsayılan satır içi kod** modülünü seçin.
1. Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin. Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.
1. **Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a>Harici Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun

Site oluşturucuda sharici betik kodunuz için yeniden kullanılabilir bir sayfa parçası oluşturmak üzere aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni sayfa parçası** iletişim kutusunda, **Harici betik**'i seçin.
1. **Sayfa parçası adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.
1. Oluşturduğunuz sayfa parçasının altında, **varsayılan harici kod** modülünü seçin.
1. Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin. Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.
1. **Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a>Bir şablona kod kodu içeren bir sayfa parçası ekler

Site oluşturucuda şablona komut kodu dahil eden bir sayfa parçası eklemek üzere aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.
1. Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.
1. **HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Sayfa parçası Ekle**'yi seçin.
1. Kodunuz için oluşturduğunuz parçayı seçin.
1. **Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Bir şablona doğrudan harici bir komut dosyası veya satıriçi komut dosyası ekleme

Bir satır içi veya harici bir kodu, tek bir şablon tarafından denetlenen bir sayfa kümesine doğrudan eklemek istiyorsanız, önce sayfa parçası oluşturmanız gerekmez.

### <a name="add-an-inline-script-directly-to-a-template"></a>Bir şablona doğrudan satıriçi komut dosyası ekleme

Site oluşturucuda bir şablona doğrudan satır içi komut dosyası eklemek için aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.
1. Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.
1. **HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül ekle** iletişim kutusunda, **satır içi betik** 'u seçin.
1. Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin. Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.
1. **Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

### <a name="add-an-external-script-directly-to-a-template"></a>Bir şablona doğrudan harici komut dosyası ekleme

Site oluşturucuda bir şablona doğrudan harici komut dosyası eklemek için aşağıdaki adımları izleyin.

1. **Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.
1. Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.
1. **HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül ekle** iletişim kutusunda, **Harici betik** 'u seçin.
1. Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin. Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.
1. **Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Favicon ekleme](add-favicon.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)
