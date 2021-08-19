---
title: Abone olma modülü
description: Bu konu abone olma modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c9c0ed18e3d5fd2521d63f8aa5b0ea668979c57d4de738b9d51a05a1cc0b6e72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730935"
---
# <a name="subscribe-module"></a>Abone olma modülü

[!include [banner](includes/banner.md)]

Bu konu abone olma modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Abone olma modülleri, site sayfalarında haber bültenleri veya promosyonlar için müşteri bilgilerini yakalamak amacıyla kullanılabilir.

Aşağıdaki resimde, Adventure Works site sayfasının alt bilgisindeki bir abone olma modülü örneği gösterilmektedir.

![Adventure Works site sayfasının alt bilgisindeki bir abone olma modülü örneği](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Abone olma modülü, Dynamics 365 Commerce 10.0.20 sürümünden itibaren Commerce modülünde kullanılabilir.
> - Abone olma modülü Adventure Works temalarında görüntülenir.
> - Abone olma modülü, müşteri bilgileri yakalandıktan sonra haber bülteni veya tanıtım e-postalarını göndermek için bir veri eylemi uzantısının bazı pazarlama e-posta sağlayıcılarıyla çalışmasını gerektirir.

## <a name="subscribe-module-properties"></a>Abone olma modülü özellikleri

| Özellik adı | Değerler | Tanım |
|---------------|--------|-------------|
| Başlık       | Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | **Haber bültenine abone ol** veya **%10 indirim için kaydol** gibi bir abone olma modülü metin başlığı. |
| Paragraf     | Paragraf metni | Abone olma modülü, başlık içindeki eyleme çağırma için ek ayrıntılar sağlamak üzere zengin metin biçimindeki paragraf metnini destekler. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Yeni sayfaya abone olma modülü ekleme

Yeni sayfaya abone olma modülü eklemek ve Commerce site oluşturucuda gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Şablonlar**'a gidin ve sitenizin giriş sayfası için pazarlama şablonunu açın (veya yeni bir pazarlama şablonu oluşturun).
1. Varsayılan sayfada **Ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Abone olma** modülünü ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve sitenin giriş sayfasını açın (veya pazarlama şablonunu kullanarak yeni bir giriş sayfası oluşturun).
1. Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Abone olma** modülünü ve **Tamam**'ı seçin.
1. Abone olma modülünün Özellik bölmesinde, **Abone ol** gibi bir başlık ekleyin.
1. **En son eğilimler, stiller ve promosyonlar. Listenizde misiniz? Abone olun ve en son teklifleri alın!** gibi bir paragraf metni ekleyin
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Adventure Works teması](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
