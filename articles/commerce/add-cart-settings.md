---
title: Sepete ürün ekle ayarlarını uygulama
description: Bu konu "Sepete ürün ekle" ayarlarını kapsar ve bunların Microsoft Dynamics 365 Commerce'te nasıl uygulanacağını açıklar.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c1d29b84d79ab503580478a1553514ddf992ca46
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/17/2021
ms.locfileid: "6637989"
---
# <a name="apply-add-product-to-cart-settings"></a>Sepete ürün ekle ayarlarını uygulama

[!include [banner](includes/banner.md)]

Bu konu **Sepete ürün ekle** ayarlarını kapsar ve bunların Microsoft Dynamics 365 Commerce'te nasıl uygulanacağını açıklar.

Bir Dynamics 365 Commerce e-ticaret sitesindeki alışveriş sepetine bir ürün eklendiğinde, farklı iş akışları desteklenir. Örneğin, site kullanıcısı alışveriş sepeti sayfasına götürülebilir. Alternatif olarak, kullanıcı geçerli sayfada kalabilir ancak ürünün alışveriş sepetine eklendiğini bildiren bir bildirim alır.

Farklı iş akışlarını desteklemek için, **Sepete ürün ekle** alanı, Commerce site oluşturucudaki **Ayarlar \> Uzantılar**'da kullanılabilir. İlgili iş akışını uygulamak için aşağıdaki ayar seçeneklerinden birini seçin:

- **Sepet sayfasına git** - Kullanıcılar sepete bir öğe ekledikten sonra sepet sayfasına gönderilir.
- **Bildirim göster** - Kullanıcı sepete bir öğe eklediğinde bir onay bildirimi gösterilir ve ürün ayrıntıları sayfasına (PDP) göz atmaya devam edebilir.
- **Mini sepet göster** – Kullanıcılar alışveriş sepetine bir öğe eklediğinde mini sepet içerikleri gösterilir. Kullanıcılar sepetteki tüm öğeleri inceleyebilir ve hazır olduklarında ödemeye geçebilir.
- **Bildirimler modülünü kullanarak bildirim göster** – Kullanıcılar alışveriş sepetine bir öğe eklediğinde, bildirimler modülü bir onay bildirimi göstermek için kullanılır. Bu ayar seçeneğinin çalışması için, bildirimler modülünün sayfa üst bilgisine eklenmesi gerekir.
- **Sepet sayfasına gitme** - Kullanıcılar sepete bir öğe ekledikten sonra geçerli sayfada kalır.

Aşağıdaki şekilde, site oluşturucusundaki **Sepete ürün ekle** ayar seçeneklerinin bir örneği gösterilir.

![Site oluşturucusundaki Sepete ürün ekle ayar seçeneklerinin örneği](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - **Sepete ürün ekle** site ayarları Dynamics 365 Commerce 10.0.11 sürümünden itibaren kullanılabilir. Dynamics 365 Commerce'in eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. appsettings.json dosyasını güncelleştirme hakkında bilgi için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - **Mini sepeti göster** ayar seçeneği Dynamics 365 Commerce Sürüm 10.0.20 itibarıyla kullanılabilir. Dynamics 365 Commerce'in eski sürümlerinden birini güncelleştiriyorsanız, appsettings.json dosyasını el ile güncelleştirmeniz gerekir. appsettings.json dosyasını güncelleştirme hakkında bilgi için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Aşağıdaki şekilde Fabrikam sitesindeki "Sepete eklendi" onay bildirimine bir örnek gösterilmektedir.

![Fabrikam sitesindeki "Sepete eklendi" onay bildirimi örneği](./media/ecommerce-addtocart-notifications.PNG)

Aşağıdaki şekilde Adventure Works sitesindeki "Sepete eklendi" onay bildirimine bir örnek gösterilmektedir.

![Adventure Works sitesindeki "Sepete eklendi" onay bildirimi örneği](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Mağaza seçicisi modülü](store-selector.md)
