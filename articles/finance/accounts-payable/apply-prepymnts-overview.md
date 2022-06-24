---
title: Otomatik olarak ön ödemeleri satıcı faturalarına uygula
description: Bu makalede, satıcı faturalarına ön ödemelerin otomatik olarak uygulanması özelliği açıklanmaktadır.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 547573d187460a900df7f4927ac062bd9d456729
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900085"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Otomatik olarak satıcı faturalarına uygula

[!include [banner](../includes/banner.md)]

Bu makalede, satıcı faturalarına ön ödemelerin otomatik olarak uygulanması özelliği açıklanmaktadır. Bir ön ödeme, satınalma sözleşmesinin bir parçası olarak bir satınalma siparişi için oluşturulabilir. Bir satıcı faturası alındıktan sonra, borç hesaplarını kapatmak için satıcı faturasından kullanılabilir. Yeni özellik, satıcı faturası içe aktarıldığında sistemin ilgili peşinatlar aramak için bir satıcı faturasında satınalma siparişi numaralarının otomatik olarak kullanılmasına olanak tanır.

Ön ödemeler bulunursa ve uygulanabiliyorsa, ön ödemeleri uygulamak için satırlar mevcut fatura satırlarına eklenir. Peşinat satırları fatura eşleştirme sürecinde hiçbir zaman dikkate alınmazlar.

Aşağıdaki noktalar, farklı satınalma işlemleri izleninceye kadar peşinatların nasıl uygulanacağını tanımlar:

- **Her satınalma siparişi için bir satıcı faturası** – Satınalma siparişindeki ön ödeme, satıcı faturasına uygulanır.
- **Birden fazla satınalma siparişi için bir satıcı faturası** – Tüm satınalma siparişlerindeki ön ödemeler, satıcı faturasına uygulanır.
- **Her satınalma siparişi için birden fazla satıcı faturası** – Satınalma siparişindeki ön ödeme, öncelikle satıcı faturasına uygulanır. Ön ödeme tutarı fatura tutarını aşarsa, ön ödeme uygulaması başarısız olur ve ön ödemeyi el ile uygulamanız gerekir.
- **Birden fazla satınalma siparişi için birden fazla satıcı faturası** – Satınalma siparişlerindeki ön ödemeler, öncelikle ilgili satıcı faturasına uygulanır. Ön ödeme tutarı fatura tutarını aşarsa, ön ödeme uygulaması başarısız olur ve ön ödemeleri el ile uygulamanız gerekir. Ön ödemeler sonrasında kalan tüm ön ödemeler ilk faturaya uygulandıktan sonra, bunlar izleyen faturalara uygulanabilir.

Bir ön ödeme uygulamaya çalışılırsa ancak ön ödeme başarısız olduysa, **Ön ödeme uygulama hatası durumunda takip otomasyonu işlemini engelle** ayarı sonraki adımları belirler:

- **Evet** – "Ön ödemeyle ilgili otomatik uygulama: Başarısız oldu" hata iletisi, otomasyon geçmişine eklenir ve fatura bekleyen satıcı faturaları listesinde kalır. Ön ödeme el ile uygulanıncaya kadar fatura bloke olarak kalacaktır.

Peşinatları el ile uygulamak için, bekleyen satıcı faturasına gidin. **Fatura ayrıntıları** sayfasında, bloke edilecek fatura için, **Otomatik olarak işleme dahil et** seçeneğini **Hayır** olarak ayarlayın. Şimdi ön ödemeyi el ile uygulayabilirsiniz. Ön ödeme uygulandıktan sonra, faturanın otomatik olarak işlenebilir olması için **Otomatik olarak işlenmek üzere dahil et** seçeneğini tekrar **Evet** olarak ayarlayın.

**Otomatik işleme dahil et** seçeneğini **Hayır** olarak ayarlayıp tekrar **Evet**'e ayarlayarak, ön ödeme uygulamasını da atlayabilirsiniz. Şu iletiyi alırsınız: "Satınalma siparişi için bir ön ödeme zaten var. Seçili satıcı faturası için bunu yok saymak istiyor musunuz?" **Evet**'i seçin. Otomatik süreç yeniden çalıştırıldığında, "Ön ödeme uygulaması el ile atlandı" iletisi otomasyon geçmişine eklenir ve satıcı faturası bloke edilmez.

- **Hayır** – İzleme otomasyon süreçleri devam edecek. Ön ödemeyi kapatma sırasında yine de uygulayabilirsiniz.
