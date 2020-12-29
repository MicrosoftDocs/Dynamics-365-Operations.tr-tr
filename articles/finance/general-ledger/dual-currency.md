---
title: Çift para birimi
description: Bu konu, raporlama para biriminin Microsoft Dynamics 365 Finance için muhasebe para birimi olarak kullanıldığı çift para birimi hakkında bilgi sağlar.
author: kweekley
manager: AnnBe
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8b71b571b03e8fa2648c90258bbcaa020baeabc0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448661"
---
# <a name="dual-currency"></a>Çift para birimi

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations 8.1 (Ekim 2018) sürümünde tanıtılan işlev, raporlama para biriminin başka amaçla ve ikinci muhasebe para birimi olarak kullanılmasını sağlar. Bu işlevselliğe *çift para birimi* de denir. Çift para birimi değişiklikleri, bir parametre veya konfigürasyon anahtarı ile devre dışı bırakılamaz. Raporlama para birimi ikinci muhasebe para birimi olarak kullanıldığından, raporlama para biriminin yayın mantığında hesaplanma yöntemi değişti.

Ayrıca çeşitli modüller, farklı süreçlerde raporlama para birimini izleme, bildirme ve kullanmak için geliştirilmiştir. Etkilenen modüller şunlardır:

- Genel muhasebe 
- Mali raporlama 
- Borç hesapları
- Alacak hesapları 
- Nakit ve banka yönetimi 
- Sabit kıymetler 
- Konsolidasyonlar

Yükseltme işleminden sonra Nakit para ve banka yönetimi ile sabit kıymetler için belirli adımları tamamlamalısınız. Bu nedenle, bu konunun ilgili bölümlerini dikkatlice okuduğunuzdan ve anladığınızdan emin olun.

## <a name="posting-process"></a>Nakil süreci

Genel muhasebeye muhasebe girişi oluşturan tüm hareketler için nakil mantığı değiştirildi. Raporlama para biriminin önceden nasıl hesaplandığı aşağıda verilmiştir:

Hareketin para birimi tutarı \> Muhasebe para birimi tutarı \> Raporlama para birimi tutarı

Örneğin, bir hareket Kanada doları (CAD) para birimi cinsinden girilir. CAD tutarı, ABD Doları (USD) olan muhasebe para birimine çevrilir. USD tutarı, euro (EUR) olan raporlama para birimine çevrilir. Bu nedenle CAD ve USD ile USD ve EUR arasındaki döviz kurları mevcut olmalıdır

Yeni hesaplama aşağıdaki gibidir:

Hareket para birimi tutarı \> Muhasebe para birimi tutarı

Hareket para birimi tutarı \> Raporlama para birimi tutarı

Bu değişiklik nedeniyle artık CAD ve USD ile CAD ve EUR arasındaki döviz kurları mevcut olmalıdır.

## <a name="reports-and-inquiries"></a>Raporlar ve sorgular

Çeşitli raporlar ve sorgular artık hem raporlama para birimi tutarlarını hem de muhasebe para birimi tutarlarını gösterir. Her rapor ve sorgulama güncelleştirilmedi. Örneğin, yalnızca hareketin para birimi cinsinden tutarları gösteren raporlar değiştirilmedi.

Değişiklikler iki şekilden birini izler:

- Rapor veya sorgunun muhasebe para birimi ve raporlama para birimi tutarlarını göstermek için yeterli alanı varsa raporlama para birimi tutarları eklenir.
- Rapor ya da sorgu her iki para biriminde de tutarları göstermek için yeterli alana sahip değilse kullanıcıların gösterilen para birimini seçmesi için bir seçenek eklendi.

Çeşitli raporlar ve sorgular için mantık, raporlama para birimi ile muhasebe para birimi aynıysa veya raporlama para birimi tüzel kişiliğin genel muhasebesinde tanımlı değilse raporlama para birimi tutarlarını zapt etmek için eklenebilir.

## <a name="financial-journals"></a>Mali günlükler

Genel günlük ve satıcı fatura günlüğü gibi mali günlükler, paporlama para birimi hakkındaki ek bilgileri içermesi için güncelleştirildi. Günlük ve fiş için toplamlar şimdi raporlama para birimi cinsinden gösterilir. Raporlama para biriminin döviz kuruyla ilgili bilgileri şimdi ek olarak, günlük satırlarının **Genel** sekmesinde görebilirsiniz. Bu nedenle, hareketleri girerken, raporlama para biriminin döviz kurunu devreden çıkarabilirsiniz.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Satıcı faturaları, satış siparişleri ve satış sözleşmeleri
Satıcı faturaları, satış siparişleri ve satış sözleşmeleri, raporlama para birimi için sabit bir döviz kuru içerecek şekilde güncelleştirildi. Hareket para birimi farklı olduğunda, sabit bir döviz kuru hem muhasebe para birimi hem de raporlama para birimi için tanımlanabilir. Muhasebe para birimi ve raporlama para birimi aynıysa, sabit döviz kuru raporlama para biriminin sabit oranı olarak muhasebe para biriminin sabit oranı kullanılarak eşitlenmiş olarak tutulur. Bu yapılandırma için raporlama para birimi sabit döviz kuru değiştirilemez. Muhasebe para birimi ve raporlama para birimi farklı olduğunda, hareket girişi sırasında hem muhasebe para birimi hem de raporlama para birimi için sabit döviz kuru tanımlanabilir. Raporlama para birimi genel muhasebede tanımlanmazsa, **Raporlama para birimi sabit döviz kuru** alanı etkinleştirilmez ve raporlama para birimi tutarı hesaplanmaz.

## <a name="module-changes"></a>Modül değişiklikleri

Aşağıdaki modüller raporlama para birimini ikinci bir muhasebe para birimi olarak kullanır:

- [Genel muhasebe](#general-ledger)
- [Mali raporlama](#financial-reporting)
- [Borç hesapları](#accounts-payable-and-accounts-receivable)
- [Alacak hesapları](#accounts-payable-and-accounts-receivable)
- [Nakit ve banka yönetimi](#cash-and-bank-management)
- [Sabit kıymetler](#fixed-assets)
- [Konsolidasyonlar](#consolidations)

### <a name="general-ledger"></a>Genel muhasebe

Genel muhasebe üzerinde bir raporlama para birimi tanımlanmışsa, genel muhasebe raporlama para birimi tutarlarını her muhasebe girişinde izler. Bununla birlikte, bu değerler şimdi hareketin para birimi tutarlarından çevrilir.

Aşağıdaki ek değişiklikler **Genel muhasebe** modülünde yapılmıştır:

- Raporlama para birimi için ayrı bir döviz kuru türü genel muhasebe üzerinde tanımlanabilir. Bir organizasyon farklı bir döviz kuru türü kullanmak istemezse raporlama para birimi için döviz kuru türü alanını boş bırakabilirsiniz. Alternatif olarak, muhasebe para birimi için kullanılan aynı döviz kuru türünü seçebilirsiniz. Alanı boş bırakırsanız, sistem muhasebe para birimi için döviz kuru türünü kullanır.
- Yeni bir günlük olan Raporlama para birimi ayarlama günlüğü, genel muhasebe hesaplarına nakledilecek ayarlamaları yalnızca raporlama para biriminde etkinleştirir. Bu günlük yalnızca genel muhasebe hesaplarına nakli etkinleştirir. Şirketlerarasını desteklemez ve para birimi, günlüğün nakledildiği tüzel kişilik raporlama para birimi olmalıdır. Günlük deftere nakledildiğinde, hareketin para birimi ve muhasebe para birimi tutarları 0 (sıfır) olur ve raporlama para birimi tutarı, hareket için girilen tutarla deftere nakledilir. Raporlama para biriminin **Borç hesapları**, **Alacak hesapları**, ve **Sabit kıymetler** modüllerinde kullanım şekli değiştiği için, bu günlük bir yükseltmeden sonra ayarlamalar için kullanılabilir. Örneğin, bu günlüğün nasıl kullanılabileceğini gösterir, söz konusu modüller için bölümlere bakın.
- Hareket, muhasebe ve raporlama para birimi cinsindeki tutarların ayırması için dönem tahsisat işlemi güncelleştirildi. Daha önce tutarlar hareket ve muhasebe para biriminde ayrılırdı ve ardından muhasebe para birimi tutarı, raporlama para birimine çevrilirdi. Bu davranış, genel muhasebe hesabının bakiyesinin raporlama para biriminde kalmasına neden olabilir. Artık tutarlar muhasebe girişinde hesaplanır ve kullanılır, çevrilme hatası olmaz.
- yabancı para birimi yeniden değerleme işlemi raporlama para biriminde tutarlara yeniden değer sağladı. Bununla birlikte, raporlama para birimi tutarı şimdi hareket para birimi tutarında hesaplanır; bu bölümdeki daha önceki [Deftere nakil işlemi](#posting-process) konusunda açıklandığı gibi.
- Genel muhasebedeki birçok rapor ve sorgu, raporlama para birimine zaten sahip, ancak birkaçı değil. Bir örnek **Mizan** liste sayfasıdır. Bu liste sayfası, şimdi hem muhasebe para birimi hem de raporlama para birimi için sütunlar içeriyor. Muhasebe para birimi ve raporlama para birimi aynıysa ya da herhangi bir raporlama para birimi genel muhasebede tanımlanmamışsa raporlama para birimi için sütunların gizli olacağını unutmayın.

### <a name="financial-reporting"></a>Mali raporlama

**Mali raporlama** modülü geliştirmesi, raporlama para birimi tutarlarını bir mali tabloya iki şekilde dahil etmenizi sağlar. Sütun tanımında (yeni işlevsellik) genel muhasebeye nakledilen raporlama para birimi tutarlarını doğrudan rapor edebilirsiniz. Alternatif olarak, tutarları muhasebe para biriminden (var olan işlev) raporlama para birimine çevirmeye devam edebilirsiniz.

Bu değişiklik, sütun tanımındaki **Para birimi görüntüleme** aracılığıyla kullanılabilir. **Genel muhasebeden raporlama para birimi** seçerseniz sütundaki tutarlar çevrilmez. Bunun yerine, doğrudan genel muhasebeden rapor edilir. Sütunun çevrilmiş tutarları göstermesini istiyorsanız **XXXX'e çevir** seçeneğini belirleyin; burada *XXXX*, sütunun göstermesi gereken raporlama para birimidir. Bu durumda, muhasebe para birimi tutarları, mevcut çeviri işlevini kullanarak seçilen para birimine çevrilir.

### <a name="accounts-payable-and-accounts-receivable"></a>Borç hesapları ve Alacak hesapları

**Borç hesapları** ve **Alacak hesapları** modülleri raporlama para birimi tutarlarını izliyor. Bununla birlikte, tutarlar çeşitli süreçler için gösterilmez veya kullanılmaz. Şu değişiklikler yapılmıştır:

- Raporlama para birimi tutarları şimdi hem müşteriler hem satıcılar için hareketlerde gösterilir. Raporlama para birimi tutarları her hareketin açık bakiyesi için de gösterilir.
- Yaşlandırma işlemi güncellendi böylece bir organizasyon yaşlandırma aralıklarını muhasebe para birimi veya raporlama para biriminde görüntüleyebilir.
- Çeşitli sorgu ve raporlar güncellendi, böylece raporlama para birimi tutarlarını gösterir. Örneklere **Müşteri - genel muhasebe mutabakatı** ve **Satıcı - genel muhasebe mutabakatı** raporları dahildir.
- yabancı para birimi yeniden değerleme işlemi raporlama para biriminde tutarlara yeniden değer sağladı. Bununla birlikte, raporlama para birimi tutarı şimdi hareket para birimi tutarında hesaplanır; bu bölümde [Deftere nakil işlemi](#posting-process) konusunda açıklandığı gibi.
- **Yükseltme ile ilgili hususlar:** Yükseltmeden önce, belgeler için (faturalar, ödemeler vb.) için raporlama para birimi tutarları muhasebe para birimi ile hesaplanırdı. Örneğin, bir organizasyon yükseltme yapmadan önce bir fatura deftere nakledilir ve fatura ödenmemiştir. Yükseltme sırasında faturanın muhasebe girişi değiştirilmez. Ancak, yükseltme sonrasında, çift para birimi değişiklikleri geçerlidir. Bu nedenle, fatura için ödeme yapıldığında, ödemenin raporlama para birimi tutarı hareket para birimi tutarı aracılığıyla hesaplanır. Ödeme ve fatura kapatıldığında, raporlama para birimi tutarları şimdi farklı hesaplandığından küçük bir fark, gerçekleşmiş kazanç/kayıp tutarı hesaplanmasında olabilir. Hesaplanan fark önemli kabul edilirse, yeni Raporlama para birimi ayarlama günlüğü , gerçekleşmiş kazanç/kayıp ile Borç hesapları/Alacak hesapları genel muhasebe hesapları arasındaki dengeyi ayarlamak için yalnızca raporlama para biriminde kullanılabilir.

### <a name="cash-and-bank-management"></a>Nakit ve banka yönetimi

Daha önce **Nakit ve banka yönetimi** modülü, her banka hesabının deftere nakledilen hareketleri için bir raporlama para birimi tutarı izlemedi. Yükseltme işleminden sonra, deftere nakledilen yeni hareketler için raporlama para birimi tutarları otomatik olarak izlenir. Bununla birlikte, raporlama para birimi tutarları yardımcı defterdeki daha önce deftere nakledilen hareketlere eklenmelidir.

- **Yükseltme ile ilgili hususlar:** Banka hesap hareketleri önceden yardımcı defterdeki raporlama para birimi tutarlarını takip etmediğinden, bir sihirbaz eklendi; böylece raporlama para birimi tutarlarını banka hesabının hareketlerine ekleyebilirsiniz. Bu sihirbaz yeniden genel muhasebe defterine **nakletmez**. Bunun yerine, genel muhasebedeki raporlama para birimi tutarlarını alır ve onları yardımcı defter tablolarında güncelleştirir.

    - Sihirbazı başlatmak için **Nakit ve banka yönetimi** \> **Kurulum** \> **Banka hesabı hareketlerine raporlama para birimi tutarları ekle**'yi seçin.
    - Sihirbaz, geçerli şirkette raporlama para birimi tutarı 0 (sıfır) olan tüm banka hesapları hareketlerini gösterir. Yalnızca yükseltme işleminden önce deftere nakledilen hareketler dahil edilir.
    - Her banka hesabı hareketi için sihirbaz, karşılık gelen genel muhasebe girişlerini bulur ve varsayılan bir raporlama para birimi tutarı girer. Tutarlar düzenlenebilir, ancak önerilir bunları düzenlemenizi **önermeyiz**. Aksi takdirde, banka hesap bakiyeleri ile genel muhasebe arasında mutabakat mümkün olmayabilir. Bir tutarı düzenlemeniz gereken tek an raporlama para birimi tutarının genel muhasebede bulunmamasıdır. Bu durumda, sihirbaz bir raporlama para birimi için 0 (sıfır) tutarı gösterir.
    - Sihirbazda **İptal et**'i seçerseniz sihirbazı bir sonraki çalıştırmanıza kadar banka hesap hareketleri ve raporlama para birimi tutarlarında yapılan değişiklikler kaydedilir. Ancak, banka hesabı hareketlerinde raporlama para birimi tutarları güncelleştirilmez. Bu güncelleştirme yalnızca sihirbazda **Bitir**'i seçtiğinizde olur. Sihirbazı birden çok kez çalıştırabilirsiniz. Bu nedenle, bir hata yaparsanız yanlış bir raporlama para birimi tutarlarını düzeltebilirsiniz.

- Nakit ve Banka yönetiminde hiçbir işlem değiştirilmedi, ancak çeşitli raporlar ve sorgular, raporlama para birimi tutarlarını gösterecek şekilde güncelleştirildi. Nakit akışı tahmin raporları özel bir durumdur. Raporlama para birimi tutarlarını içerecek şekilde güncelleştirilmedi.

### <a name="fixed-assets"></a>Sabit kıymetler

Daha önce **Sabit kıymetler** modülü, her sabit kıymet defteri nakledilen hareketleri için bir raporlama para birimi tutarı izlemedi. Yükseltme işleminden sonra, deftere nakledilen yeni hareketler için raporlama para birimi tutarları otomatik olarak izlenir. Bununla birlikte, raporlama para birimi tutarları yardımcı defterdeki daha önce deftere nakledilen hareketlere eklenmelidir.

Ayrıca, amortisman sürecinde büyük değişiklikler yapıldı. Bu değişiklikler yükseltme sonrasında kullanıcı eylemi gerektirir. Sabit kıymetleri henüz kullanmasanız bile aşağıdaki değişiklikleri okumanız ve anlamanız önemlidir.

- Amortisman sürecinin raporlama para birimi tutarını belirleme biçimi değişti. Aşağıdaki senaryo, amortismanın raporlama para birimi tutarını daha önceden nasıl belirlediğini ve şimdi nasıl belirlediğini karşılaştırır.



    **Amortisman senaryosu**

    Bir kıymet aşağıdaki tutarlarla alınır ve deftere nakledilir. Raporlama para birimi tutarının genel muhasebede deftere nakledildiğini, ancak Sabit kıymet yardımcı defter tablolarında saklanmadığını unutmayın.

    | Hareket türü | Hareket tutarı | Döviz kuru | Muhasebe para birimi tutarı | Döviz kuru | Raporlama para birimi tutarı |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Alım      | 1.000.000 DKK      | 2,0           | 500.000 USD                | 2.5           | 200.000 EUR               |

    **Raporlama para birimi için önceki amortisman**

    Amortisman teklifi yılın sonunda çalıştırılır ve aşağıdaki tutarları hesaplar.

    | Hareket türü | Hareket tutarı | Döviz kuru | Muhasebe para birimi tutarı | Döviz kuru | Raporlama para birimi tutarı |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Amortisman     | 50.000 USD         | 1,0           | 50.000 USD                 | 2,6           | 19.230,77 EUR             |

    Amortisman teklifi çalıştırıldığında, amortisman yöntemini kullanarak muhasebe para birimi tutarı hesaplanır. Daha sonra o miktarı, USD ile EUR arasındaki geçerli döviz kurunu kullanarak raporlama para birimine çevirir. Nokta oranı kullanıldığında kıymet tamamen raporlama para birimi cinsinden amortisman edemediği için bu çeviri sorunlara neden olur.

    **Raporlama para birimi için yeni amortisman**

    Raporlama para birimi tutarı da amortisman yöntemi kullanılarak hesaplanacak şekilde amortisman süreci değiştirildi. Amortismanın kıymet üzerinde çalıştırılma sonuçları bulunmaktadır.

    | Hareket türü | Hareket tutarı | Döviz kuru | Muhasebe para birimi tutarı | Döviz kuru                                                       | Raporlama para birimi tutarı |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Amortisman     | 50.000 USD         | 1,0           | 50.000 USD                 | 2.5<blockquote>[!NOTE] Bu döviz kuru gösterilse de raporlama para birimine dönüştürmek için kullanılmaz.</blockquote> | 20.000 EUR                |

    Amortisman teklifi çalıştırıldığında, amortisman yöntemini kullanarak muhasebe para birimi tutarını ve raporlama para birimi tutarını hesaplar. Tutarlar daha sonra genel muhasebedeki muhasebe girişinde kullanılır. Raporlama para birimi tutarını belirlemek için çeviri yapılmaz.

- **Yükseltme ile ilgili hususlar:** Sabit kıymet hareketleri önceden raporlama para birimini takip etmediğinden, bir sihirbaz eklendi; böylece raporlama para birimi tutarlarını sabit kıymet defteri hareketlerine ekleyebilirsiniz. Bu sihirbaz yeniden genel muhasebe defterine **nakletmez**. Amortisman teklifinin raporlama para birimi tutarlarını hesaplama biçimi değiştiğinden sihirbazın, bir kurum bir amortisman hareketi girmeden önce önce şirket için çalıştırılması ve tamamlanması **gerekir**.

    - Sihirbazı başlatmak için **Sabit kıymetler** \> **Kurulum** \> **Sabit kıymet defterlerine raporlama para birimi tutarları ekle**'yi seçin.
    - Sihirbaz, geçerli şirkette raporlama para birimi tutarı 0 (sıfır) olan tüm sabit kıymet hareketlerini gösterir. Yalnızca yükseltme işleminden önce deftere nakledilen hareketler dahil edilir.
    - Sihirbaz, raporlama para birimi tutarlarını genel muhasebeden **çekmez**. Önceki senaryoda açıklandığı gibi, genel muhasebeye ilk olarak nakledilen raporlama para birimi tutarları yanlış nokta oranını kullanırdı. Bu tutarların, sabit kıymet yardımcı defterinde görünmemesi gerekir çünkü sonraki amortisman hesaplaması yanlış tutarlar kullanır. Bunun yerine, sihirbaz birinci alım tarihindeki döviz kuru bulur. Ardından yardımcı deftere nakledilmesi gereken raporlama para birimini önermek için döviz kurunu kullanır. Örneğin, sihirbazın önceki senaryoda size gösterebileceğine örnek verilmiştir.

        | Sabit kıymet | Defter      | Hareket türü | Hareket tarihi | Para Birimi | Hareket para birimi cinsinden tutar | Tutar  | Döviz kuru | Raporlama para birimi tutarı |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Alım      | 6/3/2016         | DKK      | 1,000,000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Amortisman     | 6/3/2016         | ABD Doları      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Amortisman     | 6/3/2016         | ABD Doları      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Amortisman     | 6/3/2016         | ABD Doları      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Birçok müşteri, varlık hareketinin ayrıntılarını çalışma kitaplarında izledi. Bu ayrıntılara döviz kurları ve tutarları da dahildir. Bu veriler bir çalışma kitabında varsa, özel bir döviz kuru türü oluşturabilir ve onu çalışma kitabından döviz kurlarıyla güncelleştirebilirsiniz. Bu döviz kuru türü, ardından alım tarihinde bir varsayılan döviz kuru girmek ve raporlama para birimi tutarını hesaplamak için kullanılacaktır. Döviz kuru türü seçilmezse sihirbaz, yardımcı defterdeki döviz kuru türünü kullanır.
    - Döviz kuru ve raporlama para birimi tutarları değiştirilebilir. Döviz kuru değiştirilirse, yeni oranı kullanarak raporlama para birimi tutarı hesaplanır.
    - Sihirbazda **İptal et**'i seçerseniz sihirbazı bir sonraki çalıştırmanıza kadar sabit kıymet defteri hareketleri ve döviz kuru ya da raporlama para birimi tutarlarında yapılan değişiklikler kaydedilir. Ancak, sabit kıymet defteri hareketlerinde raporlama para birimi tutarları güncelleştirilmez. Bu güncelleştirme yalnızca sihirbazda **Bitir**'i seçtiğinizde olur. Sihirbazı birden çok kez çalıştırabilirsiniz. Bu nedenle, bir hata yaparsanız yanlış bir raporlama para birimi tutarlarını düzeltebilirsiniz.
    - Raporlama para birimi tutarları yardımcı defter içinde tamamen güncelleştirildiğinde,  **Sabit kıymet defteri hareketlerinde tüm raporlama para birimi tutarlarını güncelleştirdiniz mi?** seçeneğini **Evet** yapıp **Bitir**'i seçmeniz **gerekir**. Amortisman hesaplamaları, **Sabit kıymet defteri hareketlerinde tüm raporlama para birimi tutarlarını güncelleştirdiniz mi?** seçeneği **Evet**'e ayarlanmadan tamamlanamaz. Bu seçenek **Evet**'e ayarlandığında, sihirbaz artık kullanılabilir değildir.
    - Raporlama para birimi tutarlarıyla birlikte yardımcı defterdeki sabit kıymet hareketleri güncellendikten sonra bu tutarlar, genel muhasebe defterine ilk olarak nakledilen tutarlarla eşleşmez. Bununla birlikte, ilk olarak deftere nakledilen tutarlarla eşleşebilmeleri için Raporlama para birimi ayarlama günlüğü, genel muhasebe defterindeki amortisman genel muhasebe hesaplarının bakiyelerini güncellemek için kullanılabilir.
    - **Veri yönetimi** çalışma alanına eklenen yeni **Kıymet hareketi raporlama para birimi tutarları** sihirbazdan veri dışa aktarmanızı sağlar. Daha sonra verileri, amortisman hareketleri için sabit kıymet yardımcı defterindeki bakiyeyi belirlemek için kullanabilirsiniz. Bakiye, daha sonra genel muhasebedeki raporlama para birimi ayarlama miktarını belirlemek için kullanılabilir.

- **Yükseltme ile ilgili hususlar:** Yeni kurulum alanları sabit kıymetlere eklendi ve amortisman hesaplamasında kullanılır. Sonraki amortisman hesaplamasından önce bu alanları güncelleştirmeniz gerekiyor.

    - Sabit kıymet defteri üzerinde (**Sabit kıymetleri** \> **Defterler**), **Genel** hızlı sekmesi yeni **Raporlama para birimi cinsinden alım fiyatı** alanına sahiptir.
    - Sabit kıymet defteri üzerinde (**Sabit kıymetleri** \> **Defterler**), **Amortisman** hızlı sekmesi yeni **Raporlama para birimi cinsinden beklenen ıskarta değeri** alanına sahiptir.
    - Sabit kıymet parametrelerinde (**Sabit kıymetler** \> **Kurulum** \> **Sabit kıymet parametreleri**), **Genel** hızlı sekmesi yeni **Raporlama para birimi cinsinden minimum amortisman tutarı** alanına sahiptir.
    - Defterlerde (**Sabit kıymetler** \> **Kurulum** \> **Defterler**), **Genel** hızlı sekmesi iki yeni alana sahip: **Raporlama para birimi cinsinden amortismanı yuvarla** ve **Net defter değerini raporlama para biriminde bırak**.

- Amortisman teklifi artık hem muhasebe para birimi hem de paporlama para birimi cinsinden tutarları hesapladığından Sabit kıymet günlüğü, amortisman tutarlarını raporlama para biriminde gösterecek şekilde güncelleştirildi. Amortisman hareketleri için hareket para birimi, her zaman muhasebe para birimidir. Bu nedenle, bu değerler **Borç** ve **Alacak** sütunlarında görünmeye devam eder. İki yeni sütun **Raporlama para birimi cinsinden borç** ve **Raporlama para birimi cinsinden alacak**, kılavuza eklendi.

    - Yeni alanlar yalnızca hareket türü dört amortisman türünden biri olduğunda kullanılabilir: **Amortisman**, **Amortisman düzeltmesi**, **Olağandışı amortisman** veya **Özel amortisman oranı**.
    - Raporlama para birimi tutarları, bir amortisman hareket türü Sabit kıymet günlüğüne girilmişse, yeni sütunlarda görüntülenir. Bu tutarlar değiştirilebilir.
    - Muhasebe para birimi ile genel muhasebede raporlama para birimi aynıysa, tutarlar eşit tutulacaktır. **Alacak** tutarını değiştirirseniz **Raporlama para birimi cinsinden alacak** tutarı otomatik olarak eşleşmesi için değiştirilir.
    - Sabit kıymet günlüğüne başka hareket türü girilirse **Raporlama para birimi cinsinden borç** ve **Raporlama para birimi cinsinden alacak** tutarları, deftere nakilde önce veya sonra, hiçbir zaman gösterilmez. Muhasebe para birimi ve raporlama para birimi tutarları hala genel muhasebe defterine nakledilen fişte mevcuttur.
    
### <a name="consolidations"></a>Konsolidasyonlar
    
Dynamics 365 Finance 10.0.5 (Ekim 2019) sürümünde tanıtılan işlevler, konsolidasyon ve çift para birimi için gelişmiş esneklik sağlayan özellik yönetimi ile işlevi etkinleştirir. Bu işlevi etkinleştirmek için, **Özellik Yönetimi** çalışma alanına gidin ve **Genel muhasebe konsolidasyonlarında çift para birimi işlevini etkinleştir**'i seçin.

Genel muhasebe konsolidasyona göre, muhasebe veya muhasebe para birimi tutarlarını kaynak şirketlerinden konsolide etmek için yeni bir seçenek eklenmiştir. Muhasebe veya raporlama para birimi konsolidasyon şirketinde hesap oluşturma veya raporlama para birimi ile aynıysa tutarlar çevrilmektense doğrudan kopyalanır.

-  Artık, konsolidasyon şirketindeki işlem para birimi olarak kaynak şirketten muhasebe para biriminin mi yoksa raporlama para biriminin mi kullanılacağını seçebilirsiniz.

- Kaynak şirketten gelen muhasebe veya raporlama para birimi tutarları, para birimlerinin aynı olması durumunda, doğrudan konsolidasyon şirketindeki muhasebe veya raporlama para birimi tutarlarına kopyalanacaktır. Para birimlerinin hiçbiri aynı değilse konsolidasyon şirketinde bulunan muhasebe ve raporlama para birimi tutarları Döviz kuru kullanılarak hesaplanır.
