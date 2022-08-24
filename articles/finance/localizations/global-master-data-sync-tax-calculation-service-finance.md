---
title: Vergi Hesaplama Hizmetindeki vergi ayarını Dynamics 365 Finance ile eşitleme
description: Bu makalede, vergi kurulumu ana verilerinin Vergi Hesaplama Hizmetinden Microsoft Dynamics 365 Finance'e nasıl eşitleneceği açıklanmaktadır.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283868"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Vergi Hesaplama Hizmetindeki vergi ayarını Dynamics 365 Finance ile eşitleme

[!include [banner](../includes/banner.md)]

Bu makalede, vergi kurulumu ana verilerinin Vergi Hesaplama Hizmetinden Microsoft Dynamics 365 Finance'e nasıl eşitleneceği açıklanmaktadır.

[Vergi Hesaplamasına Başlarken](global-get-started-with-tax-calculation-service.md) konusundaki gerekli kurulum adımlarını tamamladıktan sonra, aşağıdaki vergi kurulum verileri otomatik olarak Vergi Hesaplama Hizmetinden Finance'e eşitlenir.

## <a name="sales-tax-code"></a>Satış vergisi kodu

| Vergi Hesaplama Servisi           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Vergi kodu.                          | Satış vergisi kodu                      |
| Açıklama                       | Ad                                |
| Kullanıcı girişi                        | Kapatma dönemi                   |
| Kullanıcı girişi                        | Genel muhasebe deftere nakil grubu                |
| Kullanıcı girişi                        | Satış vergisi para birimi                  |
| Negatif vergi oranı konfigüre edilir | Negatif satış vergisi yüzdesine izin ver |

## <a name="tax-value"></a>Vergi değeri

| Vergi Hesaplama Servisi | Finance                   |
| ----------------------- | ------------------------- |
| İlk hareket tarihi   | Başlangıç tarihi                 |
| Son hareket tarihi     | Bitiş tarihi                   |
| Minimum tutar          | Minimum sınır             |
| Maksimum tutar          | Maksimum sınır             |
| Vergi oranı                | Değer                     |
| Kesinti yapılamayan oran     | Kesinti yapılamayan yüzde |

## <a name="tax-limits"></a>Vergi sınırları

| Vergi Hesaplama Servisi | Finance           |
| ----------------------- | ----------------- |
| İlk hareket tarihi   | Başlangıç tarihi         |
| Son hareket tarihi     | Bitiş tarihi           |
| Minimum vergi tutarı      | Minimum satış vergisi |
| Maksimum vergi tutarı      | En yüksek satış vergisi |

## <a name="sales-tax-group"></a>Satış vergi grubu

| Vergi Hesaplama Servisi                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Vergi grubu                                       | Satış vergi grubu                            |
| Bu vergi grubu altındaki vergi kodları                  | Bu satış vergi grubu altındaki satış vergi kodları |
| Vergi kodu, **Muaf** olarak işaretlenir         | Muafiyet                                     |
| Vergi kodu, **Muaf** olarak işaretlenir         | Muafiyet kodu                                |
| Vergi kodu, **Tersine Masraf** olarak işaretlenir | Ters ücret                             |
| Vergi kodu, **Kullanım Vergisi** olarak işaretlenir        | Kullanım vergisi                                    |

## <a name="item-sales-tax-group"></a>Madde satış vergisi grubu

| Vergi Hesaplama Servisi             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Madde vergisi grubu                      | Madde satış vergisi grubu                            |
| Bu madde vergi grubu altındaki vergi kodları | Bu madde satış vergi grubu altındaki satış vergi kodları |

Eşitleme tamamlandıktan sonra, deftere nakil ve raporlama amaçları doğrultusunda Finance'teki kalan parametreleri korumaya devam edin.

> [!NOTE]
> Finance'den vergi kurulumunun Vergi Hesaplama Hizmeti ile eşitlenmesi desteklenmiyor. Varolan bir Finance ortamında, ilk olarak Vergi Hesaplama Hizmetinde vergi kurulumunu oluşturun. Daha sonra, kurulum verilerini Finance ortamına geri eşitleyin.
