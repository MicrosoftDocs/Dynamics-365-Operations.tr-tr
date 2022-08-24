---
title: Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme
description: Bu makalede, Microsoft Dynamics 365 Sales'daki Microsoft Dynamics 365 Supply Chain Management'ta fiyatlandırma altyapısının nasıl kullanılacağı açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 727e60ceee3f5c8c33d2da93128eedc1dc7bcb9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288971"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, ticari sözleşmeleri, Fiyat listelerini, müşteri bağlılık programı programlarını, yükseltmeleri ve iskontoları işleyen bir fiyatlandırma altyapısı içerir. Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır. Çift yazmayı kullandığınızda, Microsoft Dynamics 365 Sales içindeki **Teklif** ve **Sipariş** sayfalarındaki Supply Chain Management'tan fiyatlandırma motorunu kullanırsınız.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Sales'da Supply Chain Management fiyatlandırma altyapısını kullan

1. Sales'da **satışlar \>siparişlere** gidin.
1. Yeni sipariş oluşturmak için **Yeni**'yi seçin veya **Siparişlerim** listesinde mevcut siparişi seçin.
1. Yeni siparişi satırı ekleyin.
1. Yeni bir sipariş oluşturuyorsanız, eylem bölmesinde **Fiyat siparişi** seçeneğini belirleyin. Mevcut bir siparişi güncelliyorsanız eylem bölmesinde **Yeniden hesapla** seçeneğini belirleyin.
1. Aşağıdaki sütunlar otomatik olarak doldurulur:

    - Ayrıntı Tutarı
    - İskonto yüzdesi
    - İskonto
    - Ön Navlun Tutarı
    - Navlun Tutarı
    - Toplam Vergi
    - Toplam Tutar

> [!NOTE]
> Teklifler oluşturduğunuzda benzer bir işlem de geçerlidir.

## <a name="how-it-works"></a>Nasıl çalışır

Satış sırasında bir sipariş oluşturduğunuzda, bu sipariş, satış içinde girdiğiniz değerleri kullanarak Supply Chain Management ile eşitlenir. Satışlarda **Fiyat siparişi** veya **Fiyat teklifi**'ni seçtiğinizde, Supply Chain Management, Supply Chain Management'ta tanımlanan ticari anlaşma kurallarına göre her bir sipariş satırı için fiyatı ve toplam siparişi hesaplar. Yeni hesaplanan değerler daha sonra Satışlarla yeniden eşitlenir.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Supply Chain Management'ta ticari anlaşma değerlendirme seçeneklerini ayarlayın

Supply Chain Management'ı, satış içinde oluşturulan bir siparişin fiyatını hesaplarken ticari sözleşmeleri dikkate alarak veya dikkate almamasını sağlayacak şekilde konfigüre edebilirsiniz. Bu seçeneği ayarlamak için aşağıdaki adımları izleyin.

1. Supply Chain Management ortamınızda oturum açın.
1. **Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.
1. **Fiyatlar** sekmesinde, **Ticari sözleşme değerlendirme** hızlı sekmesinde, gereksinim duyduğunuz şekilde **Manuel giriş** ilkesi satırını ekleyin veya kaldırın. Bu ilkenin varlığı veya yokluğu, Supply Chain Management fiyatlandırma motorunun satışta girilen satış fiyatından otomatik olarak sahip olup olmayacağını denetler.

    - **Ticari sözleşme değerlendirme** kurulumunda **Manuel giriş** ilkesi *yoksa*, Supply Chain Management fiyat yöneticisidir. Bir kullanıcı Satışlar içindeki eylem bölmesinde **Fiyat siparişini** veya **Fiyat teklifini** seçtiğinde, Supply Chain Management fiyatlandırma motoru çağrılır ve Satış için girilen satış fiyatının, Supply Chain Management'ta hesaplanan satış fiyatına eşit olmadığı sürece üzerine yazılır.
    - **Ticari sözleşme değerlendirme** kurulumunda **Manuel giriş** ilkesi *varsa*, Satışlar fiyat yöneticisidir. Bir kullanıcı Satışlar içindeki eylem bölmesinde **Fiyat siparişini** veya **Fiyat teklifini** seçtiğinde, Satışlara girilen satış fiyatının otomatik olarak üzerine yazılması engellenir.
    - Satışlarda, **Birim başına bir fiyat** ve/veya **İskonto** değeri *0* (sıfır) olan sipariş satırları ve teklif satırları özel bir durum olarak kabul edilir. İlgili bir ticari anlaşma fiyatı kullanılabilirse, Supply Chain Management **Ticari anlaşma değerlendirme** kurulumuna bakılmaksızın bu alanlara *her zaman* uygulanır.

    Bu durumların her birine örnek olarak, aşağıdaki senaryolara bakın.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Örnek senaryo 1: Manuel giriş seçeneği olmadan ticaret anlaşması değerlendirmesi

Bu senaryoda, Supply Chain Management'taki **Ticari anlaşma değerlendirmesi** kurulumu, **Manuel giriş** ilkesini *dahil etmez*. Satış kullanıcısı, satış fiyatı içinde sıfır olmayan bir satış fiyatına sahip bir sipariş satırı girer ve Supply Chain Management'ta bulunan madde için herhangi bir satış fiyatı tanımlanmamıştır.

1. Bir kullanıcı, Satışlarda, **Birim başına fiyat** değeri 1 ABD doları (USD) olan bir sipariş satırı oluşturur.
1. Sipariş satırı, 1 USD satış fiyatıyla Supply Chain Management'a eşitlenir.
1. Satışlarda, kullanıcı, eylem bölmesindeki **Fiyat siparişini** seçer.
1. Supply Chain Management ilgili fiyat ve iskontoları arar ve toplamları hesaplar. Supply Chain Management'ta maddenin satış fiyatı bulunmadığından, hesaplama satırı 0 USD satış fiyatına sahip olacak şekilde güncelleştirir.
1. Satırın yeni satış fiyatı Satışlarla geri eşitlenir.
1. Sonuç olarak Satışlarda, satış fiyatı 0 USD olan bir sipariş satırı olur.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Örnek senaryo 2: Manuel giriş seçeneği ile ticaret anlaşması değerlendirmesi

Bu senaryoda, Supply Chain Management'taki **Ticari anlaşma değerlendirmesi** kurulumu, **Manuel giriş** ilkesini *dahil eder*. Bir Satış kullanıcısı, satışlarda sıfır olmayan bir satış fiyatına sahip bir sipariş satırı girer. Supply Chain Management, sipariş edilen madde için 2 USD satış fiyatını ayarlayan bir ticaret anlaşması içerir.

1. Bir kullanıcı, Satışlarda, **Birim başına fiyat** değeri 1 USD olan madde için bir sipariş satırı oluşturur.
1. Sipariş satırı, 1 USD satış fiyatıyla Supply Chain Management'a eşitlenir.
1. Satışlarda, kullanıcı, eylem bölmesindeki **Fiyat siparişini** seçer.
1. Supply Chain Management'ta **Ticari anlaşma değerlendirmesi** kurulumu **Manuel giriş** ilkesini içerdiği için satış fiyatı değişmez, geçerli ticari anlaşma farklı bir satış fiyatı belirtmesine rağmen.
1. Satış fiyatı, Satış ve Supply Chain Management'ta değişmeden kalır.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Örnek senaryo 3: Satışta sıfır satış fiyatına sahip bir madde için ticaret anlaşması değerlendirmesi

Bu senaryoda, Supply Chain Management'taki **Ticari anlaşma değerlendirmesi** kurulumu, **Manuel giriş** ilkesini *dahil eder*. Satış kullanıcısı, satışlarda 0 (sıfır) satış fiyatına sahip bir sipariş satırı girer. Supply Chain Management, sipariş edilen madde için 2 USD satış fiyatını ayarlayan bir ticaret anlaşması içerir.

1. Satışlarda, bir kullanıcı 0 USD değerli **Birim fiyatı** değerine ve 0 USD **Satır iskontosu** değerine sahip bir sipariş satırı oluşturur.
1. Sipariş satırı, 0 USD satış fiyatıyla Supply Chain Management'a eşitlenir.
1. Satış fiyatı 0 (sıfır) olan bir sipariş satırı aldığından, Supply Chain Management, **Manuel giriş** seçeneği etkin olmasına rağmen fiyatlandırma motorunu çağırır. Fiyatlandırma altyapısı ticari sözleşme tarafından oluşturulan 2 USD satış fiyatını döndürür ve Supply Chain Management'ta sipariş satırını güncelleştirir.
1. Güncelleştirilmiş satış fiyatı henüz Satışta sipariş satırıyla eşitlenmemiş.
1. Satışlarda, kullanıcı, eylem bölmesindeki **Fiyat siparişini** seçer.
1. Supply Chain Management'taki sipariş satırı 2 USD satış fiyatını tutar; bu durum şimdi Satışlarla geri eşitlenir. Bu nedenle, Satışlarda sipariş satırının **Birim fiyatı** değeri 0 USD'den 2 USD'ye güncelleştirilir.
1. Satışlarda kullanıcı, 0,50 USD değerinde yeni bir **Satır iskontosu** girer. Satışlar, satırın **Genişletilmiş tutar** değerinin 1,50 USD olduğunu hesaplar.
1. Sipariş satırı, 0.50 USD **Sipariş iskontosu** değeriyle Supply Chain Management'a eşitlenir.
1. Satışlarda, kullanıcı, eylem bölmesindeki **Fiyat siparişini** seçer.
1. Satışta sipariş satırı için hiçbir fiyat veya iskonto değişikliği yapılmaz.

## <a name="limitations"></a>Sınırlamalar

Sales içindeki sütunlar doldurulduğunda, aşağıdaki sınırlamalar geçerlidir:

- Supply Chain Management'ta bulunan masraf ve gider tahsisatının kurulumu Sales içinde çoğaltılmaz.
- Fiyatlandırma, Supply Chain Management'ta satış siparişi satırı sayfasındaki **Perakende Kanalı** sütununda belirtilen özel perakende fiyatlandırmasını dikkate almıyor.
- Supply Chain Management'ın **ticari kesinti Yönetimi** bölümünde tanımlanan iskontolar dikkate alınmazlar.
- Fiyatlandırmada satış sözleşmeleri dikkate alınmaz.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
