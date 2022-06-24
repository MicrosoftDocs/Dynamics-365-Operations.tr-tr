---
title: Şirket içi kullanım için bir şirketlerarası satış siparişi oluşturma
description: Bu konuda, şirket içi kullanım için şirketlerarası satış siparişinin nasıl oluşturulacağı açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a37b8ab1b3df10cdbd3bbb87410bc3dc70dc0ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873535"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Şirket içi kullanım için bir şirketlerarası satış siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Genellikle, şirketlerarası satınalma siparişine dayalı olarak, bir şirketlerarası satış siparişi otomatik olarak oluşturulur. Ayrıca şirketlerarası müşterinin tüzel kişiliğinde şirketlerarası satınalma siparişi oluşturan bir şirketlerarası satış siparişini el ile de oluşturabilirsiniz.

![Şirketlerarası şirket içi satış süreci](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>El ile şirketlerarası satış siparişi oluşturma

Bu adımları, çizimde gösterildiği gibi B tüzel kişiliğinde gerçekleştirin.

1. **Alacak hesapları \> Satış siparişi \> Tüm satış siparişleri**'sayfasına gidin.
1. Eylem Bölmesi'nde, satış siparişi oluşturmak için **Satış siparişi**'ni seçin.
1. **Satış siparişleri oluşturma** sayfasında bir müşteri hesabı seçin. **Genel** hızlı sekmesinde, **Şirketlerarası** onay kutusunun seçili olduğundan emin olun. Bu, seçilen müşterinin şirketlerarası bir müşteri olduğunu gösterir.
1. Bilgileri girin veya değiştirin, **Tamam**'ı seçin ve ardından sipariş satırlarını her zamanki gibi tamamlayın.

    **Teslimat adresi** alan değeri, şirketlerarası satış siparişi başlığından şirketlerarası satınalma siparişi başlığına kopyalanır. Ürün boyutları dahil olmak üzere **Madde numarası** alan değeri ile **Teslim tarihi** ve **Para birimi kodu** alan değerleri, şirketlerarası satış siparişi satırlarından şirketlerarası satınalma siparişi satırlarına kopyalanır.

1. İlgili şirketlerarası satınalma siparişini görüntülemek için sipariş başlığında **Şirketlerarası**'nı seçin.
1. Şirketlerarası ticaret için eldeki stok hakkında bilgileri görüntülemek için sipariş satırlarında **Şirketlerarası**'nı seçin.

> [!TIP]
> Şirketlerarası satış siparişlerini **Şirketlerarası siparişler** sayfasından görüntüleyebilirsiniz.

> [!NOTE]
> Şirketlerarası ile çalışırken, **Alacak hesapları parametreleri** sayfasındaki **Faturalama sonrasında siparişi sil** onay kutusunun işaretini kaldırmanızı öneririz. Aksi takdirde, ilgili satınalma siparişi silinir. Ayrıca, **Borç hesapları parametreleri** sayfasındaki **Faturalama sonrasında satınalma siparişini sil** onay kutusunu temizlemenizi öneririz.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
