---
title: Satıcı faturası otomasyonu için kurulum seçenekleri (Önizleme)
description: Bu makalede, satıcı faturası otomasyonunu ayarlama ve yapılandırma için kullanılabilen seçenekler açıklanmaktadır.
author: sunfzam
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86ad68b3dc08bf2c57ab5f9bc6c65bc37c0901e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874855"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Satıcı faturası otomasyonu için kurulum seçenekleri

[!include [banner](../includes/banner.md)]

Bu makalede, satıcı faturası otomasyonunu ayarlama ve yapılandırma için kullanılabilen seçenekler açıklanmaktadır. Fatura otomasyonu özellikleri aşağıdaki kurulum parametresi türlerini kullanır:

- İçe aktarılan faturalardaki peşinatlar otomatik olarak uygulanacak parametreler.
- İçe aktarılan satıcı faturalarını iş akışı sistemine gönderme ve deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarına eşleştirmeye yönelik parametreler.
- İşleme otomasyonu arka plan görevleriyle ilgili parametreler. İşlem otomasyonu çerçevesi, içe aktarılan satıcı faturalarını iş akışı sistemine göndermek için kullanılır. Ayrıca, deftere nakledilen ürün giriş satırlarını bekleyen satıcı fatura satırlarıyla otomatik olarak eşleştirmek ve ürün giriş satırlarıyla otomatik olarak eşlenen manuel faturalar için fatura eşleştirme doğrulaması gerçekleştirmek amacıyla da kullanılır. Farklı iş süreçleri seçili bir işlemin ne sıklıkta çalıştırılacağını tanımlamak için bu çerçeveyi kullanır. **Ürün girişini fatura satırlarıyla eşleştir** ve **Satıcı faturalarını iş akışına gönder** arka plan işlemlerindeki kullanılabilir sıklıklar **Saat** ve **Günlük**'tür.

Bir arka plan göreviyle ilgili bilgileri ayarlamak veya görüntülemek için, **Sistem Yönetimi \>Kurulum \> İşlem otomasyonları**'na gidin **Arka plan görevi** sekmesini seçin.

Satıcı faturası deftere nakli aracılığıyla içe aktarma işleminden temassız otomasyon elde etmek için, bir satıcı faturası iş akışı ayarlamanız gerekir. İş akışı ayarlamak için **Borç hesapları > Kurulum > Borç hesapları iş akışları**'na gidin. Faturanın el ile müdahale olmadan başlangıçtan bitişe kadar işlendiğinden emin olmak için, iş akışı yapılandırmanıza otomatik deftere nakil görevi eklemeniz gerekir.

## <a name="parameters-for-automatically-applying-prepayments-in-imported-invoices"></a>İçe aktarılan faturalardaki peşinatlar otomatik olarak uygulanacak parametreler

- **İçe aktarılan faturalar için ön ödemeyi otomatik olarak uygula** – Bu seçenek **Evet** olarak ayarlandığında, sistem, satıcı faturaları içe aktarıldığında ilgili satınalma siparişi için var olan peşinatlar otomatik olarak arar. Uygulanabilecek peşinatlar bulunursa, alınan satıcı faturalarındaki peşinatlar uygulamak için ek bir satır eklenir.
- **Ön ödeme uygulaması hatası durumunda takip etme otomasyon sürecini engelle** – Bu seçenek **Evet** olarak ayarlandığında, ön ödeme uygulanmazsa faturalar bloke edilir. Makbuz eşleştirme süreci ve bir iş akışı işlemine gönderim gibi diğer otomatikleştirilmiş işlemler gibi, fatura otomasyon işlemi de ön ödeme el ile uygulanarak bloke faturaları çekmez. 

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>İçe aktarılan satıcı faturalarını iş akışı sistemine gönderme parametreleri

İçe aktarılan satıcı faturalarını iş akışı sistemine göndermek içim belirli parametreler kullanılır. Ayrıca, bazı parametreler deftere nakledilen ürün girişi satırlarını otomatik olarak bekleyen satıcı fatura satırlarıyla eşleştirmek için de kullanılır. **Borç hesapları parametreleri** sayfasının **Satıcı faturası otomasyonu** sekmesinde ayarlamanız gereken parametreler aşağıdaki bölümler arasında bölünmüştür:

- Satıcı faturaları iş akışı
- Ürün girişlerini otomatik olarak eşleştir

Aşağıdaki parametreler kullanılabilir:

- **İçe aktarılan faturaları otomatik olarak iş akışına gönder** – Bu seçeneği **Evet** olarak ayarlarsanız içe aktarılan faturalar otomatik olarak iş akışı sistemine gönderilir. Bu seçenek **Hayır** olarak ayarlanırsa, faturaların el ile gönderilmesi gerekir. Bu seçeneği **Evet** olarak ayarlayıp içe aktarma sonuçlarından deftere nakil yoluyla bir temassız işlem etkinleştirirsiniz.

    Bu seçeneği, yalnızca geçerli varlığınız için etkin bir satıcı faturası iş akışı ayarlanmışsa **Evet** olarak ayarlayabilirsiniz. İş akışı ayarlamak için **Borç hesapları \> Kurulum \> Borç hesapları iş akışı**'na gidin.

- **Ürün girişlerini otomatik göndermeden önce fatura satırlarıyla eşleştir** – Bu seçeneği **Evet** olarak ayarlarsanız, eşleşen ürün giriş miktarı fatura miktarına eşit oluncaya kadar içe aktarılan fatura otomatik olarak iş akışı sistemine gönderilemez. Bu seçeneği **Evet** olarak ayarlayıp deftere nakledilen ürün girişlerinin otomatik olarak eşleştirilmesi, üç yönlü eşleştirme ilkesinin tanımlandığı satırlarla aynı şekilde etkinleştirilir. Bu işlem, eşlenen ürün giriş miktarı fatura miktarına eşit oluncaya kadar çalışacaktır. Bu noktada, fatura otomatik olarak iş akışı sistemine gönderilir.

    **Otomatik olarak göndermeden önce ürün girişlerini fatura satırlarıyla eşleştir** seçeneği yalnızca **Fatura eşleştirme doğrulamasını etkinleştir** seçeneği işaretliyse kullanılabilir. Bu seçenek belirlendiğinde, **Ürün girişlerini fatura satırlarıyla otomatik olarak eşleştir** seçeneği otomatik olarak seçilir.

- **Hesaplanan toplamların otomatik iş akışı gönderimi için içe aktarılan toplamlara eşit olmasını gerektir** – Bu seçeneği **Evet** olarak ayarlarsanız, fatura için hesaplanan toplamlar içe aktarılan toplamlara eşit oluncaya kadar fatura otomatik olarak iş akışı sistemine gönderilemez. Bu seçenek **Hayır** olarak ayarlanırsa, fatura otomatik olarak iş akışı sistemine gönderilebilir ancak hesaplanan toplamlar düzeltilene kadar deftere nakledilemez. Fatura tutarını veya satış vergisi tutarını içe aktarmıyorsanız bu seçeneğin **Hayır** olarak ayarlanması gerekir.
- **Ürün girişlerini fatura satırlarıyla otomatik olarak eşleştir** – Bu seçeneği **Evet** olarak ayarlarsanız, deftere nakledilen ürün makbuzlarının, üç yönlü eşleştirme ilkesi için tanımlanan satırları faturalamak üzere otomatik olarak eşleştirilmesi için bir arka plan işlemi kullanılabilir. Bu işlem, eşlenen ürün girişi miktarı fatura miktarına eşit oluncaya veya **Otomatik eşleştirme deneme sayısı** değerine ulaşılıncaya kadar çalışacaktır. İşlem, fatura iş akışı sistemine gönderilene kadar çalıştırılabilir.

    Bu seçenek yalnızca **Fatura eşleştirme doğrulamasını etkinleştir** seçeneğinin işaretlenmiş olması durumunda kullanılabilir.

    **Otomatik eşleştirmeden önce ürün girişlerini fatura satırlarıyla eşleştir** seçeneğini **Evet** olarak ayarlarsanız, bu seçenek **Hayır** olarak ayarlanamaz. Bu seçeneği **Hayır** olarak ayarlamak için önce **Otomatik eşleştirmeden önce ürün girişlerini fatura satırlarıyla eşleştir** seçeneğini **Hayır** olarak ayarlamanız gerekir.

- **Otomatik eşleştirmeyi deneme sayısı** - İşlemin başarısız olması sonucuna varmadan önce, sistemin ürün girişlerini bir fatura satırıyla eşleştirmek için kaç kez deneme yapması gerektiğini seçin. Belirtilen deneme sayısına ulaşıldığında, fatura otomasyon işleminden kaldırılır.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
