---
title: Commerce sohbeti modülü proaktif sohbet parametreleri
description: Bu makalede, Microsoft Dynamics 365 Commerce'teki Commerce sohbeti modüllerinin proaktif sohbet parametreleri açıklanmaktadır.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: f3cff89a25ff84414e7fdd32cbb26404c2080187
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691105"
---
# <a name="commerce-chat-module-proactive-chat-parameters"></a>Commerce sohbeti modülü proaktif sohbet parametreleri

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'deki Customer Service için Çok Yönlü Kanal ile Commerce Sohbeti ve Power Virtual Agents sohbet modülleri ile Commerce Sohbeti proaktif sohbet parametreleri açıklanmaktadır.

## <a name="proactive-chat-properties"></a>Proaktif sohbet özellikleri

Proaktif sohbet özellikleri, Commerce site oluşturucuda Customer Service için Çok Yönlü Kanal ile Commerce Sohbeti ve Power Virtual Agents modülleri ile Commerce Sohbeti'nin özellikler bölmesinde bulunur.

> [!NOTE]
> Varsayılan olarak burada listelenen tüm proaktif sohbet özellikleri boştur. Bu özellikler hakkında daha fazla bilgi edinmenizi ve bunları yalnızca gerektiğinde ayarlamanızı öneriyoruz. Bu yaklaşım, hatalı proaktif sohbetlerin tetiklenmesini azaltmaya yardımcı olur.

### <a name="proactive-chat"></a>Proaktif Sohbet

| Kolay ad | Açıklama | Varsayılan değer |
|---------------|-------------|---------------|
| Etkin | Farklı tetikleyicilere dayalı olarak müşterilere proaktif bir şekilde katılın. | Devre dışı |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. | Boş |

### <a name="wait-time-proactive-chat"></a>Bekleme Süresi (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Bekleme süresi (sn) | Proaktif sohbet tetiklenmeden önce site kullanıcılarının site sayfasında harcadıkları süre (saniye cinsinden). |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="number-of-page-visits-proactive-chat"></a>Sayfa Ziyaretleri Sayısı (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Sayfa ziyareti sayısı | Proaktif bir sohbet tetiklenmeden önce sayfa ziyareti sayısı. Site kullanıcıları öncelikle tanımlama bilgisi onay başlığında bulunan istemi kabul etmelidir. |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="specific-pages-proactive-chat"></a>Belirli Sayfalar (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Sayfalar | Ziyaret edildiğinde, proaktif sohbeti tetikleyecek sayfaların listesi. |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="from-specific-pages-proactive-chat"></a>Belirli Sayfalardan (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Sayfalar | Kullanıcılar bunlardan uzaklaştığında, proaktif sohbeti tetikleyecek sayfaların listesi. |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="specific-countryregion-proactive-chat"></a>Belirli Ülke/Bölge (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Ülke kodu | Belirtilen ülkelerden veya bölgelerden ziyaret eden kullanıcılar, proaktif bir sohbet tetikler. Ülke/bölge kodları iki büyük harf olmalıdır (örneğin **ABD**). |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="date-range-proactive-chat"></a>Tarih Aralığı (Önleyici Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Başlangıç Tarihi (gg/aa/yyyy) | Proaktif bir sohbetin tetikleneceği tarih veya sonrası. |
| Bitiş Tarihi (gg/aa/yyyy) | Proaktif bir sohbetin tetikleneceği tarih veya öncesi. |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="total-amount-in-cart-proactive-chat"></a>Sepetteki Toplam Tutar (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Minimum | Kullanıcılar sepet sayfasını ziyaret ederken, proaktif bir sohbeti tetikleyecek olan alışveriş sepetindeki minimum parasal tutar (dahil). |
| Maksimum | Kullanıcılar sepet sayfasını ziyaret ederken, proaktif bir sohbeti tetikleyecek olan alışveriş sepetindeki maksimum parasal tutar (dahil). |
|Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="total-number-of-items-in-cart-proactive-chat"></a>Sepetteki Toplam Öğe Sayısı (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Minimum | Kullanıcılar sepet sayfasını ziyaret ederken, proaktif bir sohbeti tetikleyecek olan alışveriş sepetindeki minimum öğe sayısı (dahil). |
| Maksimum | Kullanıcılar sepet sayfasını ziyaret ederken, proaktif bir sohbeti tetikleyecek olan alışveriş sepetindeki maksimum öğe sayısı (dahil). |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

### <a name="specific-products-in-cart-proactive-chat"></a>Sepetteki Belirli Ürünler (Proaktif Sohbet)

| Kolay ad | Açıklama |
|---------------|-------------|
| Ürün kimliği/SKU | Kullanıcılar sepet sayfasını ziyaret ederken, önleyici bir sohbeti tetikleyecek ürün kimlikleri/stok tutma birimi (SKU) numaralarının listesi. |
| Sohbet selamlaması | Proaktif sohbet tetiklendiğinde kullanılan selamlama iletisi. |

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce sohbeti özelliklerine genel bakış](commerce-chat-overview.md)

[Customer Service için Çok Yönlü Kanal modülüyle Commerce Sohbeti](commerce-chat-module.md)

[Power Virtual Agents modülü ile Commerce Sohbeti](chat-module-pva.md)
