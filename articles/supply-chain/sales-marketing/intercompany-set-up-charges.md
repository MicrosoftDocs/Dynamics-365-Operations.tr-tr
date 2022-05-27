---
title: Şirketlerarası siparişlerdeki masrafları ayarlama
description: Bu konuda, şirketlerarası siparişlerde masrafların nasıl ayarlanacağı açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 27633e09bfcf41fbbe5449b0d3b5f283eaf7ee13
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673676"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Şirketlerarası siparişlerdeki masrafları ayarlama

[!include [banner](../../includes/banner.md)]

Şirketlerarası siparişlere eklenecek masrafları ayarlayabilirsiniz. Şirketlerarası satış siparişine masraf eklendiğinde, şirketlerarası satınalma siparişiyle otomatik olarak eşitlenir. Bu işlem iki türlü de geçerlidir: şirketlerarası satış siparişinden satınalma siparişine ve diğer türlü.

Masrafı şirketlerarası bir yüzde olarak tanımlayarak şirketlerarası satış siparişine kâr eklemek için masrafları da kullanabilirsiniz.

Şirketlerarası siparişlere uygulanacak masrafları ayarladığınızda, orijinal satış siparişinin net tutarından şirketlerarası satış siparişi için dahili kâr hesaplamasını etkinleştirirsiniz. Şirketlerarası satıcınız size maliyet fiyatından satış yapıyorsa bunu yapmak isteyebilirsiniz. Aşağıdaki yordamda, bunun şirketlerarası müşteriler için nasıl yapılacağı açıklanmaktadır. Satıcılar için aynı yordamı kullanabilirsiniz.

1. **Alacak hesapları \> Kurulum \> Masraflar \> Müşteri masraf grupları**'na gidin.
1. Bir masraf grubu oluşturun.
1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin. Müşteri hesabı bağlantısını seçin. Eylem Bölmesi'nde, **Müşteri** sekmesini ve sonra **Satış siparişi** hızlı sekmesini seçin.
1. Alanda düzenlemeleri etkinleştirmek için Eylem Bölmesi'nde **Düzenle**'yi seçin. **Giderler grubu** alanında, 2. adımda ayarladığınız şirketlerarası masraflar grubunu seçin.
1. **Alacak hesapları \> Kurulum \> Masraflar \> Otomatik masraflar**'a gidin.
1. İlgili alanları doldurarak masrafları ayarlayın.
1. **Müşteri ilişkisi** alanında, 2. adımda ayarladığınız şirketlerarası masraflar grubunu seçin.
1. **Satır** hızlı sekmesinde, **Kategori** alanında **Şirketlerarası yüzde**'yi seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
