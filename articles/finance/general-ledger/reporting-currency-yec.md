---
title: Yıl sonu kapanışı çalıştırıldığında bakiye dışı para birimini raporlama
description: Bu makalede, yıl sonu kapanışı çalıştırıldığında raporlama para biriminin bakiye dışı olabileceği açıklanmaktadır.
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850270"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>Yıl sonu kapanışı çalıştırıldığında bakiye dışı para birimini raporlama

**Genel muhasebe kapatma ve yıl sonu kapatma arasında farkındalık** (**Farkındalık** özelliği) özelliğini etkinleştirdikten sonra kapatılan genel muhasebe hareketleri artık genel muhasebe yıl sonu kapanışı çalıştırıldığında sonraki mali yılın açılış bakiyesine dahil edilmez. Genel muhasebe hareketlerinin dışlanması, mali yıl için bir raporlama para birimi tanımlanmışsa, yıllık kapanış saatinde müşteriler için bir özel durum oluşturabilir.

Genel muhasebe kapatma yalnızca hesap para birimi için gerçekleştirilir. Genel muhasebe hareketleri kapatıldığında, doğrulama yalnızca muhasebe para birimi cinsinden hesap para birimi kredileri eşit olduğunu onaylar. Bu genel muhasebe hareketlerinin raporlama para birimi tutarları doğrulanmaz ve bunlar için Borçlar eşit değildir. Ayrıca, genel muhasebe kapatma, raporlama para biriminde bir kazanç/kaybı otomatik olarak hesaplamaz ve deftere nakletmez.

Bu sınırlamalar nedeniyle, genel muhasebe kapatma işlemi tamamlandığında raporlama para biriminde bir kazanç/kayıp hareketi bulunmalıdır. Genel muhasebe kapanışıyla ilgili kazanç/kayıp dahil değilse, yıl sonu kapanışı çalıştırıldığında bakiye dışı bir ileti gösterilir.

Aşağıdaki örnekte, bu soruna yıl sonu kapanışı çalıştırılmadan önce adreslenmesi adımları verilmiştir.

## <a name="example-setup"></a>Örnek kurulumu

Bu örneği ayarlamak için, **Farkındalık** özelliğini etkinleştirin ve genel muhasebe kapatma için 110180 ana hesap ayarlayın. Aşağıdaki şekil DEMF tüzel kişiliğinde deftere nakledilen genel muhasebe hareketlerini gösterir. DEMF hesap para birimi ABD Doları (USD) ve raporlama para birimi ise Euro (Euro).

![Raporlama para birimi cinsinden deftere nakledilen genel muhasebe hareketleri.](./media/reporting-currency-1.png)

**Genel muhasebe kapatma** sayfası 110180 ana hesap genel muhasebe hareketlerini gösterir. Kılavuzu seçin ve tutun (veya sağ tıklayın) ve sonra **Sütun ekle**'yi seçin. Hareket para birimi, muhasebe para birimi ve raporlama para birimi miktarlarının tümünün gösterilmesi için **Raporlama para biriminde tutar** sütununu ekleyin.

![Raporlama para birimi sütunu genel muhasebe kapatma sayfasına eklenen tutar.](./media/Ledger-settlement2.png)

100,00 EUR için ilk iki genel muhasebe hareketi tek bir grup olarak kapatılır, 200,00 EUR sonraki iki genel muhasebe hareketi başka bir grup olarak kapatılamayabilir. (Bu iki hareket farklı kapatma koduna sahip olacaktır.) Bu kurulum, kuruluşların farklı zamanlarda kapatılan ve farklı kapatma tarihlerine sahip birden çok genel muhasebe hareketi grubuna sahip olmasını gösterir. Kapatma tamamlandıktan sonra, **genel muhasebe kapatmaları** sayfası, **Kapatılmış** durumunda olan hareketleri göstermek üzere filtre uygulandığında aşağıdaki bilgileri gösterir.

![Genel muhasebe kapatmaları sayfasında kapatılan hareketler.](./media/Settled-trans-filtered3.png)

**Genel muhasebe kapatmaları** sayfasında **Tutar** sütununu seçin ve basılı tutun (veya sağ tıklayın) ve sonra toplamları göstermek için **Bu sütun için toplamı** seçin. **Raporlama para birimi** sütunlarındaki tutar için bu adımı yineleyin. Kapatma işlemi için hesap para biriminin farkı 0 (sıfır) olmalıdır. Ancak raporlama para birimi için kapatma tutarı doğrulaması yapılmaz. Aşağıdaki şekil raporlama para birimi için -27,79 USD farkını gösterir.

![Raporlama para birimi için fark.](./media/Difference4.png)

## <a name="year-end-close"></a>Yıl sonu kapanışı

Yıl sonu kapanışı 2022 için de çalışıyorsa, işlem, bakiye dışında bir hata ile sona erer. Bu hata, raporlama para biriminin 0 (sıfır) ile ilgili bir genel muhasebe kapanış tutarı olmadığı için doğrudan oluşur.

![Genel muhasebe kapatma tutarının 0 (sıfır) olmadığını belirten hata iletisi.](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>Raporlama para birimi kazanç/kaybını deftere nakletme

Yıl sonu kapatmanın başarıyla çalıştırılabilmesi için raporlama para birimi tutarındaki fark, genellikle kazanç veya kayıp olarak ve genel muhasebe kapanışının dahil edilmesi gerekir. Raporlama para birimi kazancı/kaybı birden çok şekilde deftere nakledilebilir:

- Ana hesap borç hesapları veya alacak hesapları ise, bu belgelerin AR/AP kapanışının gerekli kazanç/kayıp olduğunu üretecektir. Bu muhasebe girişinin, fatura, ödemeler, alacak dekontları vb. ile ilgili genel muhasebe hareketleri kapatıldığında genel muhasebe kapanışına eklenmesi gerekir.
- Ana hesap, borç hesapları veya alacak hesabı dışında bir hesapta ise, kazanç/kayıp el ile girilmelidir. Kazanç/zarar deftere nakledildiğinde, muhasebe girişiyle ilgili ayrıntı düzeyi organizasyonunuz tarafından belirlenir.
- Her ana hesap için, deftere nakledilmesi gereken raporlama para birimi kazanç/kayıp tutarını tanımlayın.

Daha önce açıklandığı gibi, bu deftere nakil işlemi **Genel muhasebe kapatmaları** sayfasında yapılabilir.

1. Kazancı/zararı nakletmek istediğiniz tarih aralığına filtre uygulayın. Ayda bir kazanç/kayıp deftere nakli planlıyorsanız, her ay için filtre uygulayın. Her mali yıl için bir kazanç/kayıp deftere nakli planlıyorsanız, tüm yıla ait filtre.
2. Ana hesapta filtre.
3. Yalnızca **Kapatılan** hareketler görünecek şekilde durumu filtreleyin.
4. **Raporlama para birimi cinsinde tutar** sütununa toplamı ekleyin.
5. Kazancı/kaybı daha parçalı bir düzeyde deftere nakletmek istiyorsanız, kapatma kodu, mali boyutlar vb. üzerinde ek filtre uygulayabilirsiniz. **Raporlama para birimi cinsinde tutar** sütunu için toplam tutar, kazanç/zararın deftere nakledileceği tutarı gösterir.
6. **Genel muhasebe \> Günlük girişleri \> Raporlama para birimi düzeltme günlükleri**'ne gidin.
7. Kazanç/kayıp için hareketi girin. Bu günlük, yalnızca raporlama para biriminde bir düzeltmeyi deftere nakleder. Deftere nakledilen hareket para birimi ve hesap para birimi tutarları her zaman 0'dır (sıfır). Bu günlük daha önce kullanılmamışsa, **Genel muhasebe \> Günlük kurulumu \> Günlük adları** içinde **Raporlama para birimi ayarlamasının** günlük türüne sahip bir günlük adı oluşturmanız gerekebilir.
8. Ana hesap el ile girişe izin vermiyorsa bu ayarlama deftere nakledilemez. Bu nedenle **Ana hesap** sayfasında **El ile giriş yapma** parametresine izin verme özelliğini geçici olarak kapatmanız gerekebilir.

![Günlük fişi sayfasında el ile giriş.](./media/Manual-entry6.png)

Düzeltme günlüğünü deftere naklettikten sonra, **Genel muhasebe kapatmaları** sayfasına dönün ve kazanç/kaybı deftere naklettiğiniz ana hesabı seçin. Kazanç/kayıp ayarlaması genel muhasebe kapanışına dahil edilmiş olmalıdır. Raporlama para birimi tutarı netten 0'a (sıfır) sahip olmadığı için, önceki hareketleri kapatıp yeniden kapatamazsınız, ancak bu zamanın kazanç/kayıp olmasını sağlayabilirsiniz. Kazancın/kaybın nakledilmesinde ve genel muhasebe kapanışlarında bu kazanç/zararın kapanışının kuruluşunuza göre nasıl olmasını istediğinize kadar kesin.

Aşağıdaki şekil 200 EUR hareketlerinin kapatılmamış olduğunu ve daha sonra kapatma için yeniden işaretlenmesini göstermektedir. Bu kez, kazanç/kayıp ayarlamasını dahil eder.

![Genel muhasebe ödemeleri sayfasında kazanç/kayıp ayarlaması.](./media/gain-loss7.png)

Hareketler kapatıldıktan sonra, **Durum** filtresini, sayfa **Kapatılmış** hareketleri gösterecek şekilde değiştirin. **Raporlama para birimi cinsinden tutar** sütunu toplamı şimdi 0 (sıfır). Yıl sonu kapanışı şimdi başarıyla çalıştırılabilir.

![Başarılı yıl sonu kapanışı.](./media/Zero-settled8.png)
