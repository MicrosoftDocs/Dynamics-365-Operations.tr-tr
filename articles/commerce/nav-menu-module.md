---
title: Gezinti menüsü modülleri
description: Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817886"
---
# <a name="navigation-menu-module"></a>Gezinti menüsü modülleri

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu gezinti menüsü modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Genel bakış

Gezinti menüsü modüllerinin başlıca amacı, site kullanıcılarının Dynamics 365 Commerce yönetim merkezinde tanımlanan kanal gezinti hiyerarşisine göre ürün ve site sayfalarına göz atmasına olanak sağlamaktır. Bir gezinti menüsü modülünde yapılandırılan öğeler site üstbilgisi gezintisi olarak görünür. Gezinti menüsü modülleri, bir e-ticaret sitesindeki diğer sayfalara bağlantı sağlayan statik menü öğelerini de destekler.

Gezinti menüsü modülü bir sayfanın üst bilgi modülüne eklenebilir. Fabrikam temasında, gezinti menüsü varsayılan olarak iki düzey gösterir. Starter temasında, gezinti menüsü varsayılan olarak üç düzey gösterir. Düzey sayısını değiştirmek için temada bir görünüm uzantısı gereklidir.

Aşağıdaki çizimde, iki düzey kategori hiyerarşisi ve bazı statik menü öğeleri bulunan Fabrikam sitesi için bir gezinti menüsü örneği gösterilmektedir.
![Gezinti menüsü modülü örneği](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Gezinti menüsü modüllerinin özellikleri

| Özellik adı             | Değer                 | Tanım |
|---------------------------|-----------------------|-------------|
| Kaynak                  | **Perakende**, **El ile yazma**, **Perakende ve el ile yazma** | **Perakende** değeri, Commerce yönetim merkezinde kanal gezinme hiyerarşisinin gezinti menüsünde görüntülenmesini sağlar. **El ile yazma** değeri statik menü öğelerinin oluşturulmasına izin verir. **Perakende ve el ile yazma** değeri, her ikisinin karışımına izin verir. |
| Kategori resimlerini göster | **Doğru** veya **yanlış**    | Etkinleştirildiğinde, bu özellik gezinti menüsündeki kategori resimlerini her kategori için Commerce yönetim merkezinde tanımlandığı şekilde görüntüler. Commerce sürüm 10.0.14'e eklendi. |
| Statik menü öğesi| Değerler dizisi| Bir menü öğesi adını statik site sayfasının bağlantısıyla ilişkilendiren statik menü öğeleri. Menü öğelerini diğer menü öğelerinin altında oluşturabilirsiniz. Varsayılan olarak, statik menüler kök düzeyinde görünür ve varsa kanal gezinme hiyerarşisine eklenir. |

Aşağıdaki çizimde, Fabrikam sitesinin gezinti menüsünde görüntülenen kategori resmi örneği gösterilmektedir.
![Kategori resimlerine sahip bir gezinti menüsü modülü örneği](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Üstbilgi modülüne gezinti menüsü modülü ekleme

Bir üstbilgi modülüne gezinti menüsü modülü ekleme hakkında ayrıntılar için, bkz. [Üstbilgi modülü](author-header-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Tanımlama bilgisi uyumluluğu](cookie-compliance.md)

[Üst bilgi modülü](author-header-module.md)
