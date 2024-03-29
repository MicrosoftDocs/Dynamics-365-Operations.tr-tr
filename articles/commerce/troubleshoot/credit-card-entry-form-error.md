---
title: Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor
description: Bu makale, ödeme yöntemi bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269768"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>Kredi kartı giriş sayfası ödeme sırasında hata görüntülüyor

[!include [banner](../../includes/banner.md)]

Bu makale, **ödeme yöntemi** bölümü yüklenmediğinde ve hata iletisi gösterildiğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Çevrimiçi bir mağazanın ödeme sayfasını açtığınızda, **ödeme yöntemi** bölümü yüklenmiyor ve şu hata iletisi görüntüleniyor: "Bir sorun oluştu. Lütfen daha sonra yeniden deneyin."

![Ödeme modülü hatası.](media/payment-module-error.jpg)

## <a name="resolution"></a>Çözüm

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Commerce Scale Unit önbelleğinin süresinin dolmasını bekleyin

Çevrimiçi mağazanın ödeme sayfasındaki ödeme servisi ayarları Commerce Scale Unit'te önbelleğe alınır ve e-ticaret sitesinde görüntülenmesi 15 dakika kadar sürebilir. Bu ödeme servisi ayarları satıcı hesap kimliği, bulut API anahtarı ve ödeme yöntemiyle ilişkili çeşitli yapılandırma ayarları ile ilgili değişiklikleri içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi kanalı ayarlama](../channel-setup-online.md)
