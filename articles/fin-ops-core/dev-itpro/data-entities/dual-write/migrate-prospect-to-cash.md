---
title: Aday müşteriden nakde verilerini Veri Tümleştiriciden çift yazmaya geçirme
description: Bu makalede, Aday müşteriden nakde verilerinin Veri Tümleştiriciden çift yazmaya nasıl geçirileceği açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 8e5c11e535bd61e9955a4abf1491e88991ee40f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894280"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Aday müşteriden nakde verilerini Veri Tümleştiriciden çift yazmaya geçirme

[!include [banner](../../includes/banner.md)]

Veri tümleştiricisi için kullanılabilen Müşteri adayınden nakde çözümü çift yazma ile uyumlu değil. Bunun nedeni, Müşteri adayından nakde çözümünün bir parçası olarak gelen hesap tablosundaki msdynce_AccountNumber dizinidir. Bu dizin varsa aynı müşteri hesabı numarasını iki farklı tüzel kişilik için oluşturamazsınız. Müşteri adayından nakde verilerini Ceri Tümleştiricisi'nden çift yazmaya taşıyarak çift yazmaya sıfırdan başlangıç yapmayı seçebilir veya Müşteri adayından nakde çözümünün son sürümünü yükleyebilirsiniz. Bu makale, her iki yaklaşımı da kapsamaktadır.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Veri Tümleştirici Müşteri adayından nakde çözümünün son sürümünü yükleme

**PC2 Sürüm 15.0.0.2**, veri tümleştirici Müşteri adayından nakde çözümünün son sürümü olarak kabul edilir. [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C)'ten indirebilirsiniz.

El ile yüklemeniz gerekir. Yükleme sonrasında, msdynce_AccountNumber dizininin kaldırılması dışında her şey tamamen aynı kalır.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Aday müşteriden nakde verilerini Veri Tümleştiriciden çift yazmaya geçirme adımları

Aday müşteriden nakde verilerinizi Veri Tümleştiriciden çift yazmaya geçirmek için aşağıdaki adımları izleyin.

1. Son tam eşitlemeyi yapmak için Aday müşteriden nakde Veri Tümleştirici işlerini çalıştırın. Bu şekilde, her iki sistemin (Finans ve Operasyon uygulamaları ve müşteri etkileşimi uygulamaları) de tüm verilere sahip olduğundan emin olursunuz.
2. Olası veri kaybını önlemek için, Aday müşteriden nakde verilerini Microsoft Dynamics 365 Sales'dan Excel dosyasına veya virgülle ayrılmış değerler (CSV) dosyasına dışarı aktarın. Aşağıdaki varlıklardan verileri aktarın:

    - [Hesap](#account-table)
    - [Başvur](#contact-table)
    - [Fatura](#invoice-table)
    - Fatura ürünleri
    - [Sipariş](#order-table)
    - [Ürünler sipariş et](#order-products-table)
    - [Ürünler](#products-table)
    - [Teklif](#quote-and-quote-product-tables)
    - [Teklif ürünleri](#quote-and-quote-product-tables)

3. Aday müşteriden nakde çözümünü Sales ortamından kaldırın. Bu adım, Aday müşteriden nakde çözümü tarafından sunulan sütunları ve ilgili verileri kaldırır.
4. Çift yazma çözümünü yükleyin.
5. Bir veya daha fazla tüzel kişilik için Finans ve Operasyon uygulamasıyla müşteri etkileşimi uygulaması arasında çift yazma bağlantısı oluşturun.
6. Çift yazma tablo eşlemelerini etkinleştirin ve gerekli başvuru verileri için başlangıç eşitlemesini çalıştırın. (Daha fazla bilgi için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).) Gerekli verilere örnek olarak müşteri grupları, ödeme koşulları ve ödeme zamanlamaları verilebilir. Hesap, teklif, teklif satırı, sipariş ve sipariş satırı tabloları gibi başlatma gerektiren tablolar için çift yazma eşlemelerini etkinleştirmeyin.
7. Müşteri etkileşimi uygulamasında **Gelişmiş Ayarlar \> Sistem Ayarları \> Veri Yönetimi \> Yinelemeleri algılama kuralları**'na gidin ve tüm kuralları devre dışı bırakın.
8. 2. adımda listelenen tabloları başlatın. Yönergeler için, bu makalenin geri kalan bölümlerine bakın.
9. Finans ve Operasyon uygulamasını açın ve hesap, teklif, teklif satırı, sipariş ve sipariş satırı tablo eşlemeleri gibi tablo eşlemelerini etkinleştirin. Ardından ilk eşitlemeyi çalıştırın. (Daha fazla bilgi için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).) Bu işlem; Finans ve Operasyon uygulamasından işleme durumu, sevkiyat ve fatura adresleri, sahalar ve ambarlar gibi ek bilgileri eşitler.

## <a name="account-table"></a>Hesap tablosu

1. **Şirket** sütununda, **USMF** gibi bir şirket adı girin.
2. **İlişki Türü** sütununda, statik değer olarak **Müşteri**'yi girin. Her hesap kaydını iş mantığınızda müşteri olarak sınıflandırmak istemeyebilirsiniz.
3. **Müşteri Grup Kodu** sütununda, Finans ve Operasyon uygulamasındaki müşteri grubu numarasını girin. Aday müşteriden nakde çözümündeki varsayılan değer **10**'dur.
4. **Hesap Numarası** ile ilgili herhangi bir özelleştirme olmadan Aday müşteriden nakde çözümünü kullanıyorsanız **Taraf Numarası** sütunundaki **Hesap Numarası** değerini girin. Özelleştirmeler varsa ve taraf numarasını bilmiyorsanız bu bilgiyi Finans ve Operasyon uygulamasından çekin.

## <a name="contact-table"></a>İlgili kişi tablosu

1. **Şirket** sütununda, **USMF** gibi bir şirket adı girin.
2. CSV dosyasındaki **IsActiveCustomer** değerini temel alarak aşağıdaki sütunları ayarlayın:

    - **IsActiveCustomer** CSV dosyasında **Evet** olarak ayarlanmışsa **Satış yapılabilir** sütununu **Evet** olarak ayarlayın. **Müşteri Grup Kodu** sütununda, Finans ve Operasyon uygulamasındaki müşteri grubu numarasını girin. Aday müşteriden nakde çözümündeki varsayılan değer **10**'dur.
    - **IsActiveCustomer**, CSV dosyasında **Hayır** olarak ayarlanmışsa **Satış yapılabilir** sütununu **Hayır** olarak ayarlayın ve **İlgili Kişi** sütununu **Müşteri** olarak ayarlayın.

3. **İlgili Kişi** özelleştirmesi olmayan bir Aday müşteriden nakde çözümü kullanıyorsanız aşağıdaki sütunları ayarlayın.

    - CSV dosyasındaki ilgili kişi numarasını (**msdynce\_contactnumber**) **İlgili kişi** tablosundaki ilgili kişi numarasına (**msdyn\_contactnumber**) geçirin.
    - **Taraf Numarası** sütununda **İlgili Kişi Numarası** tablosundaki değerleri kullanın.
    - **Hesap Numarası/İlgili Kişi Kodu** sütununda **İlgili Kişi Numarası** tablosundaki değerleri kullanın.

## <a name="invoice-table"></a>Fatura tablosu

**Fatura** tablosundaki veriler tek bir yöne (Finans ve Operasyon uygulamasından müşteri etkileşimi uygulamasına) akacak şekilde tasarlandığından başlatma gerekli değildir. Gerekli tüm verileri Finans ve Operasyon uygulamasından müşteri etkileşimi uygulamasına geçirmek için ilk eşitlemeyi çalıştırın. Daha fazla bilgi için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).

## <a name="order-table"></a>Sipariş tablosu

1. **Şirket** sütununda, **USMF** gibi bir şirket adı girin.
2. CSV dosyasındaki **Sipariş Kodu** sütununun değerini **Satış Siparişi Numarası** sütununa kopyalayın.
3. CSV dosyasındaki **Müşteri** sütununun değerini **Fatura müşteri numarası** sütununa kopyalayın.
4. CSV dosyasındaki **Sevkiyat Ülkesi/Bölgesi** sütununun değerini **Sevkiyat Ülkesi/Bölgesi** sütununa kopyalayın. Bu değere örnek olarak **ABD** ve **Amerika Birleşik Devletleri** gösterilebilir.
5. **Talep Edilen Giriş Tarihi** sütununu ayarlayın. Giriş tarihi kullanmıyorsanız, CSV dosyasındaki **Talep Edilen Teslim Tarihi**, **Karşılandığı Tarih** ve **Gönderildiği Tarih** sütunlarını kullanın. Bu değere örnek olarak **2020-03-27T00:00:00Z** verilebilir.
6. **Dil** sütununu ayarlayın. Bu değere örnek olarak **en-us** verilebilir.
7. **Madde tabanlı** sütununu kullanarak **Sipariş Türü** sütununu ayarlayın.

## <a name="order-products-table"></a>Sipariş ürünleri tablosu

- **Şirket** sütununda, **USMF** gibi bir şirket adı girin.

## <a name="products-table"></a>Ürünler tablosu

**Ürünler** tablosundaki veriler tek bir yöne (Finans ve Operasyon uygulamasından müşteri etkileşimi uygulamasına) akacak şekilde tasarlandığından başlatma gerekli değildir. Gerekli tüm verileri Finans ve Operasyon uygulamasından müşteri etkileşimi uygulamasına geçirmek için ilk eşitlemeyi çalıştırın. Daha fazla bilgi için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Teklif ve Teklif ürünü tabloları

**Teklif** tablosu için bu makalenin önceki kısımlarında yer alan [Sipariş tablosu](#order-table) bölümündeki talimatları izleyin. **Teklif ürünü** tablosu için [Sipariş ürünleri tablosu](#order-products-table) bölümündeki talimatları izleyin.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
