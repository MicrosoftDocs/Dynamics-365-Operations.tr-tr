---
title: Satış noktası (POS) uygulaması ve kullanıcı dili ayarları
description: Bu makale, Modern POS (MPOS) ve Bulut POS'daki dil ayarlarının nasıl değiştirileceğini açıklar.
author: jblucher
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 15490885b5ce366edbab669893f3c3e36585f308
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863359"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Satış noktası (POS) uygulaması ve kullanıcı dili ayarları

[!include [banner](includes/banner.md)]

Bu makale, Modern POS (MPOS) ve Bulut POS'daki dil ayarlarının nasıl değiştirileceğini açıklar.

## <a name="overview"></a>Genel Bakış
Modern POS (MPOS) ve Bulut POS dil ayarları ve çevirilerin mağaza ve kullanıcı ayarları arasında farklılık gösterebildiği ortamları destekler. Örneğin, mağaza müşterileri için yaygın olarak İngilizce kullanılan bir bölgede bulunabilir ancak bazı çalışanlar uygulamayı Fransızca çevirileri ile kullanmayı tercih edebilir.

## <a name="data-language"></a>Veri dili

Kullanıcının ayarları ne olursa olsun, MPOS ve Bulut POS veriler için kullanılan çevirileri belirlemek üzere her zaman mağazanın dil ayarlarını kullanır. Bu, tüm kullanıcıların ve müşterilerin tutarlı bir deneyimi olmasını garanti eder. Veri örnekleri:

- Ürünler
- Öznitelikler ve değerler
- Kategori adları
- Yazdırılan veya e-postayla gönderilen hareket girişleri
- Ödeme yöntemi adları
- Satır görüntüleme iletileri

Kullanıcı oturum açmadan önce bilinmediğinden ana POS oturum açma ekranı için de mağazanın dili kullanılır. Mağazanın dili için kullanılabilir çeviri yoksa, POS şirketin diline döner.

### <a name="configuring-the-stores-language-setting"></a>Mağazanın dil ayarını yapılandırma

Mağazanın dil ayarı **Genel &gt; Bölgesel Ayarlar &gt; Dil** altındaki **Mağaza** sayfasında bulunan **Tüm mağazalar**'dan ayarlanır. Her mağaza için bir dil seçmek üzere açılır listeyi kullanın.

## <a name="user-interface-language"></a>Kullanıcı arabirimi dili

POS kullanıcısının dil ayar,ı uygulama kullanıcı arabiriminde kullanılan çevirileri belirler. Bu, tüm etiketleri, menüleri ve veri kabul edilmez listeleri içerir. Bunun tek istisnası POS düğme grupları üzerinde görüntülenen metindir. Düğme grupları çevirileri desteklemez ve bunlar her zaman metinleri düğmede tanımlandığı şekilde gösterir. Çevrilen düğmeleri desteklemek için, ayrı düğme grupları kopyalayıp korumanız ve bunları uygun şekilde kullanıcılara atamanız gerekir.

### <a name="configuring-the-users-language-setting"></a>Kullanıcının dil ayarını yapılandırma

POS kullanıcısının dil ayarı **Perakende ve Ticaret &gt; Dil** menüsünde bulunan **Çalışan** sayfasındaki **Tüm çalışanlar** öğesinden ayarlanır. Ana Profil öğesinden ayarlanmaz. Bu ayar POS tarafından kullanılmaz. Kullanıcının dili ayarlanmamışsa veya çevirilerin mevcut olmadığı bir dile ayarlanmışsa, POS mağazanın diline döner.

| &nbsp;      | Kullanıcı Arabirimi dili                   | Veri dili (ürünler, makbuz biçimleri, satır görüntüleme, vs.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Şirket** | Varsayılan Değer                    | Varsayılan Değer                                                       |
| **Mağaza**   | Şirketi geçersiz kılar          | Şirketi geçersiz kılar                                             |
| **Kullanıcı**    | Mağazayı veya şirketi geçersiz kılar | Hiçbir Zaman                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]