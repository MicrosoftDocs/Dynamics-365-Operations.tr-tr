---
title: Otomatik olarak ön ödemeleri satıcı faturalarına uygula
description: Bu konu, satıcı faturalarına ön ödemelerin otomatik olarak uygulanması yeteneğini açıklamaktadır.
author: sunfzam
ms.date: 10/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: b1ea73a50f5adaa1a00c9ddfa8c983375e0d47be
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675753"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Otomatik olarak satıcı faturalarına uygula

[!include [banner](../includes/banner.md)]

Bu konu, satıcı faturalarına ön ödemelerin otomatik olarak uygulanması yeteneğini açıklamaktadır. Bir ön ödeme, satınalma sözleşmesinin bir parçası olarak bir satınalma siparişi için oluşturulabilir. Bir satıcı faturası alındıktan sonra, borç hesaplarını kapatmak için satıcı faturasından kullanılabilir. Yeni özellik, satıcı faturası içe aktarıldığında sistemin ilgili peşinatlar aramak için bir satıcı faturasında satınalma siparişi numaralarının otomatik olarak kullanılmasına olanak tanır.

Ön ödemeler bulunursa ve uygulanabiliyorsa, ön ödemeleri uygulamak için satırlar mevcut fatura satırlarına eklenir. Peşinat satırları fatura eşleştirme sürecinde hiçbir zaman dikkate alınmazlar.

Aşağıdaki noktalar, farklı satınalma işlemleri izleninceye kadar peşinatların nasıl uygulanacağını tanımlar:

- **Her satınalma siparişi için bir satıcı faturası** – Satınalma siparişindeki ön ödeme, satıcı faturasına uygulanır.
- **Birden fazla satınalma siparişi için bir satıcı faturası** – Tüm satınalma siparişlerindeki ön ödemeler, satıcı faturasına uygulanır.
- **Her satınalma siparişi için birden fazla satıcı faturası** – Satınalma siparişindeki ön ödeme, öncelikle satıcı faturasına uygulanır. Ön ödeme tutarı fatura tutarını aşarsa, ön ödeme uygulaması başarısız olur ve ön ödemeyi el ile uygulamanız gerekir.
- **Birden fazla satınalma siparişi için birden fazla satıcı faturası** – Satınalma siparişlerindeki ön ödemeler, öncelikle ilgili satıcı faturasına uygulanır. Ön ödeme tutarı fatura tutarını aşarsa, ön ödeme uygulaması başarısız olur ve ön ödemeleri el ile uygulamanız gerekir. Ön ödemeler sonrasında kalan tüm ön ödemeler ilk faturaya uygulandıktan sonra, bunlar izleyen faturalara uygulanabilir.

Sistem bir ön ödeme uygulamaya çalışırsa, ancak uygulama başarısız olduysa, davranış, **Ön ödeme uygulama hatası durumunda takip otomasyonu işlemini engelle** ayarına bağlıdır:

- **Evet** – "Ön ödemeyle ilgili otomatik uygulama: Başarısız oldu" hata iletisi, otomasyon geçmişine eklenir ve fatura bekleyen satıcı faturaları listesinde kalır. Ön ödeme el ile uygulanıncaya kadar fatura bloke olarak kalacaktır.

    Peşinatları el ile uygulamak için, bekleyen satıcı faturasına gidin. **Fatura ayrıntıları** sayfasında, bloke edilecek fatura için, **Otomatik olarak işleme dahil et** seçeneğini **Hayır** olarak ayarlayın. Şimdi ön ödemeyi el ile uygulayabilirsiniz. Ön ödeme uygulandıktan sonra, faturanın otomatik olarak işlenebilir olması için **Otomatik olarak işlenmek üzere dahil et** seçeneğini tekrar **Evet** olarak ayarlayın.

    **Otomatik işleme dahil et** seçeneğini **Hayır** olarak ayarlayıp tekrar **Evet**'e ayarlayarak, ön ödeme uygulamasını da atlayabilirsiniz. Şu iletiyi alırsınız: "Satınalma siparişi için bir ön ödeme zaten var. Seçili satıcı faturası için bunu yok saymak istiyor musunuz?" **Evet**'i seçin. Otomatik süreç yeniden çalıştırıldığında, "Ön ödeme uygulaması el ile atlandı" iletisi otomasyon geçmişine eklenir ve satıcı faturası bloke edilmez.

- **Hayır** – İzleme otomasyon süreçleri devam edecek. Ön ödemeyi kapatma sırasında yine de uygulayabilirsiniz.
