---
title: Karma müşteri siparişleri
description: Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4cb448670af9a6ddce8008be008cf3b0ff76bbce65053bf4618ea6668c4568d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739541"
---
# <a name="hybrid-customer-orders"></a>Karma müşteri siparişleri

[!include [banner](includes/banner.md)]

Bir karma müşteri siparişi, hem müşteri tarafından mağazadan alınabilecek ürünler içeren hem de daha sonra çekilecek veya sevk edilecek tek bir sipariştir.

Commerce'te içerisinde, bir müşteri siparişi için tüm ürünleri yerine getirmeyi veya yalnızca seçilen ürünleri yerine getirmeyi seçebilirsiniz. Yerine getirilmek üzere işaretlenmiş ürün satırları, sipariş oluşturulduktan sonra otomatik olarak faturalanır, sipariş oluşturulduktan sonra çekilecek bir sipariş için de aynı şey geçerlidir. Karma siparişlerde kalan tutar, ürün çekme ve sevk satırlarındaki depozito yüzdesini, yürütülecek satırların toplam tutarına eklenerek belirlenir. Sistem, karma siparişler için müşteri sipariş modur ve nakit ve taşı modları arasında şöyle geçiş yapar:

- Sepetteki tüm ürünler **Teslim alınan taşıma** olarak ayarlanmışsa, sipariş Öde ve Al hareketi olarak ele alınır.
- Sepetteki tüm veya bazı satırlar **Çekme** veya **sevk nakliyesi** olarak ayarlanmışsa, sipariş Müşteri sipariş hareketi olarak ele alınır.

Bir sepet satırı seçildiyse ve **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git** seçiliyse, sadece belirli sepet satırları bu teslim yöntemiyle ayarlanır. Bu durumda, işlem akışı her zaman olduğu gibi devam eder. Ancak, **Seçileni çek**, **Seçileni sevk et** veya **Seçileni al git**, sepet satırı seçmeden seçildiyse, tüm sepet satırlarını listeleyen yeni bir sayfa açılır. Bu ekranda, bir teslim yöntemi ayarlamak için birden fazla satırı aynı anda seçebilirsiniz. Satırları seçmek için bu yöntemi kullandığınızda, satıra daha önce atanan tüm teslim yöntemleri geçersiz kılınır.

## <a name="additional-resources"></a>Ek kaynaklar

[Modern POS'taki (MPOS) müşteri siparişleri](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]