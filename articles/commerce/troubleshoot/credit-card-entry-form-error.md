---
title: Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor
description: Bu konu, ödeme yöntemi bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585568"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor

[!include [banner](../../includes/banner.md)]

Bu konu, **ödeme yöntemi** bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Çevrimiçi bir mağazanın ödeme sayfasını açtığınızda, **ödeme yöntemi** bölümü yüklenmiyor ve şu hata iletisi görüntüleniyor: "Bir sorun oluştu. Lütfen daha sonra yeniden deneyin."

![Ödeme modülü hatası](media/payment-module-error.jpg)

## <a name="resolution"></a>Çözünürlük

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Commerce Scale Unit önbelleğinin süresinin dolmasını bekleyin

Çevrimiçi mağazanın ödeme sayfasındaki ödeme servisi ayarları Commerce Scale Unit'te önbelleğe alınır ve e-ticaret sitesinde görüntülenmesi 15 dakika kadar sürebilir. Bu ödeme servisi ayarları satıcı hesap kimliği, bulut API anahtarı ve ödeme yöntemiyle ilişkili çeşitli yapılandırma ayarları ile ilgili değişiklikleri içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi kanalı ayarlama](../channel-setup-online.md)
