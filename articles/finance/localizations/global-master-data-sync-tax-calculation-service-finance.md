---
title: Vergi Hesaplama Hizmetindeki vergi ayarını Dynamics 365 Finance ile eşitleme
description: Bu konu, vergi kurulumu ana verilerinin Vergi Hesaplama Hizmetinden Microsoft Dynamics 365 Finance'e nasıl eşitleneceğini açıklamaktadır.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a9c11a6f5946d56b9e58a02c37f18adec155661
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687800"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Vergi Hesaplama Hizmetindeki vergi ayarını Dynamics 365 Finance ile eşitleme

[!include [banner](../includes/banner.md)]

Bu konu, vergi kurulumu ana verilerinin Vergi Hesaplama Hizmetinden Microsoft Dynamics 365 Finance'e nasıl eşitleneceğini açıklamaktadır.

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
