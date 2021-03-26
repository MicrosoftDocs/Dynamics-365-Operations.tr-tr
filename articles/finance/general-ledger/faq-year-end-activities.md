---
title: Yıl sonu faaliyetleriyle ilgili SSS
description: Bu konu başlığı, yıl sonu kapanış faaliyetlerine yardımcı olmak için derlenmiştir.
author: kweekley
manager: tfehr
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a9feafcab5969e9ec8fcbb8a6903d7b59505f6ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249423"
---
# <a name="year-end-activities-faq"></a>Yıl sonu faaliyetleriyle ilgili SSS 

Bu konu başlığı, yıl sonu kapanış faaliyetlerine yardımcı olmak için derlenmiştir. Bu konu başlığındaki bilgiler öncelikle Genel muhasebe ve Borç hesapları için yıl sonu kapanış faaliyetlerine ilişkin sorulara odaklanmaktadır.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Genel muhasebe: Yıl sonu kapanışını çalıştırdığımızı ve geri almadığımızı nasıl anlarım?
Kuruluşların yıl sonu kapanışını yürütmeye çalışıp bunun yerine yıl sonu kapanışını geri almaya çalıştıklarını tespit ettik. Yıl sonu kapanışı gerçekten hızlı bir şekilde sonlanıyorsa veya yıl sonu kapanışı açılış bakiyeleri oluşturmuyorsa **Yıl sonu kapanışı**'ndaki (**Genel muhasebe > Dönem kapanışı > Yıl sonu kapanışı > Mali kapanışı çalıştır**) **Önceki kapanışı geri al** ayarını doğrulayın. 

[![Yıl sonu kapanışını çalıştırma ve yıl sonu kapanışını geri alma](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

**Önceki kapanış geri al** seçimi **Evet** olarak ayarlanırsa önceki yıl sonu kapanışı tersine çevrilir. Geri alma işlemi çalıştırılırken, yıl sonu kapanışı hiç çalıştırılmamış gibi tüm kapanış bakiyesi ve açılış bakiyesi girişleri silinir. Fişler silinir. Yıl sonu kapanışı otomatik olarak yeniden çalıştırılmaz. İşlemi yeniden başlatmanız gerekir, bu kez **Önceki kapanışı geri al** seçeneğini **Hayır** olarak değiştirin. 

> [!NOTE]
> Kapanış bakiyesi girişi isteğe bağlı olarak kapatılan yıl içinde oluşturulur. Bu durum yalnızca **Aktarım sırasında kapanış hareketleri oluştur** adlı Genel muhasebe parametresi **Evet** olarak ayarlanırsa oluşur. Açılış bakiyesi girişi her zaman oluşturulur çünkü bu, gelecek yılın başlangıç bakiyesidir.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Genel muhasebe: Yıl sonu kapanışı için Geri Al ve Sil GL parametresi arasındaki fark nedir?
**Yıl sonu kapanışı** iletişim kutusunda bulunan **Önceki kapanışı geri al** parametresi ile Genel muhasebede (**Genel muhasebe > Dönem kapanışı > Yıl sonu kapanışı > Mali kapanışı çalıştır**) yer alan **Aktarım sırasında yıl sonu kapanışı hareketlerini sil** parametresi arasındaki farkla ilgili bir karışıklık söz konusu olabilir.  

[![Yıl sonu kapanışı için Geri Al ile Sil GL parametresi arasındaki fark](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Yıl sonu kapanışı hiç çalıştırılmamış gibi, tüm kapanış ve açılış bakiyesi girişlerini silmek için yıl sonu kapatma işlemi çalıştırılırken açılan iletişim menüsünde **Önceki kapanışı geri al**'ı seçin. Fişler silinir. Yıl sonu kapanışı otomatik olarak yeniden çalıştırılmaz. Yıl sonu kapanışını çalıştırmak için bu işlemi yeniden başlatmanız gerekir. Bu kez, **Önceki kapanışı geri al** seçeneğini **Hayır** olarak ayarlayın (**Genel muhasebe > Genel muhasebe kurulumu > Genel muhasebe parametreleri**). 

[![Genel muhasebe parametresi ayarı](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Genel muhasebedeki **Aktarım sırasında yıl sonu hareketlerini sil** parametresi, yalnızca yıl sonu kapanışını çalıştırırken (geri alırken değil) kullanılır (**Önceki kapanışı geri al** seçimi **Hayır** olarak ayarlanmıştır). Bu parametre **Evet** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri silinir ve yıl sonu kapanışı yeniden çalıştırılır. Bu işlem, kuruluş son yıl sonu kapanışından sonraki ayarlamalar da dahil olmak üzere tüm hareketlerin kapanış bakiyesi ve açılış bakiyesi girişleri için tek bir muhasebe girişinde deftere naklini istediğinde kullanılır. 

Bu seçenek **Hayır** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri kalır. Bu girişler silinmez. Bunun yerine, yalnızca o mali yılda son yıl sonu kapanışından bu yana deftere nakledilen değiştirilmiş veya yeni hareketler için yeni bir kapanış bakiyesi ve açılış bakiyesi girişi oluşturulur.  

> [!NOTE]
> Kapanış bakiyesi girişi, kapatılan yıl içinde oluşturulur. Bu durum yalnızca Genel muhasebedeki **Aktarım sırasında kapanış hareketleri oluştur** parametresi **Evet** olarak ayarlandığında oluşur. Açılış bakiyesi girişi her zaman oluşturulur çünkü bu, gelecek yılın başlangıç bakiyesidir. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Genel muhasebe: Yıl sonu işleme performansını artırmak için neler değiştirilebilir? 
Yıl sonu kapanışının performansını artırmak için bir dizi değişiklik yapabilirsiniz. Değişikliğin kuruluşunuz için uygun olup olmadığını değerlendirmek için önerilen bu değişiklikleri dikkate almanızı öneririz.  

### <a name="dimension-sets"></a>Boyut kümeleri
Yıl sonu kapanışını çalıştırırken, her boyut kümesi bakiyesi yeniden oluşturulur ve performans üzerinde doğrudan bir etkisi olur. Bazı kuruluşlar, boyut kümeleri bir noktada kullanıldıkları veya kullanılabilecekleri için gereksiz boyut kümeleri oluşturur.  Bu gereksiz boyut kümeleri, yıl sonu kapanışı sırasında yeniden oluşturulmaya devam eder ve işlemin daha uzun sürmesine neden olur. Boyut kümelerinizi değerlendirmek ve gereksiz boyut kümelerini silmek için zaman ayırın.

Gereksiz boyut kümeleri **BudgetDimensionFocusInitializeBalance** (**Genel muhasebe > Hesap planı > Boyutlar > Mali boyut kümeleri)** toplu işini de etkiler.

[![Mali boyut kümeleri](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Yıl sonu kapanış şablonu yapılandırması
Yıl sonu kapanış şablonu, kuruluşların kar ve zarar bakiyelerini elde tutulan kazançlara aktarırken korunmasını istedikleri mali boyut düzeyini seçmelerine olanak tanır. Ayarlar, kuruluşların bakiyeleri elde tutulan kazançlara taşırken ayrıntılı mali boyutları (**Tümünü kapat**) korumasına veya tutarları tek bir boyut değerine (**Tekli kapat**) özetlemeyi seçmesine olanak tanır. Bu durum, her mali boyut için tanımlanabilir. Bu ayarlar hakkında daha fazla bilgi için [Yıl sonu kapanışı](year-end-close.md) konu başlığına bakın.

Kuruluşunuzun gereksinimlerini değerlendirmenizi ve mümkünse performansı artırmak için **Tekli kapat** yıl sonu kapanışı seçeneğini kullanarak mümkün olduğunca çok boyutu kapatmanızı öneririz. Tek bir boyut değerine (boş bir değer de olabilir) kapatarak sistem, elde tutulan kazanç hesabı girişleri için bakiyeleri belirlerken daha az ayrıntı hesaplar.

### <a name="10013-update-or-later"></a>10.0.13 güncelleştirmesi veya sonrası
Kuruluşunuzun yıl sonu kapanışını son çalıştırmasından bu yana 10.0.13 veya sonraki bir sürüme güncelleştirme yaptıysanız [HashV2 özelliğinin uygulanması](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2) nedeniyle yıl sonu kapanışı daha uzun sürebilir. (*Hash* terimi, diğer dize alanlarından hesaplanan bir alanı ifade eder. Hash GUID değerini hesaplayacak API, güvenliği artırmak için güncelleştirilmiştir.) Yıl sonu kapanış işlemini hızlandırmak için yıl sonu kapanışını çalıştırmadan önce boyut kümelerinin bakiyelerini yeniden oluşturmanızı öneririz. 10.0.13 güncelleştirmesini aldıktan sonra boyut kümesi bakiyelerinin yeniden oluşturulması işlemini gerçekleştirdiyseniz yeniden oluşturma işlemini yeniden çalıştırmanız gerekmez.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Genel muhasebe: Dönem kapanışı - Yıl sonu kapanışı ne işe yarar?
 
[![Dönem kapanışı, yıl sonu kapanışı](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Mali boyut kümelerinin yeniden oluşturulması için performans iyileştirmeleri (yeni özellik)
Sürüm 10.0.16'ya eklenen yeni bir özellik, yıl sonu kapanışı ve konsolidasyonu işlemlerinin performansını artırır. Özellik, Mali boyut kümelerinin yeniden oluşturulması için performans iyileştirmeleri olarak adlandırılmıştır. Bu özellik, boyut kümelerinin yalnızca ilgili bir zaman dilimi için yeniden oluşturulabilmesi için boyut kümelerinin yeniden oluşturulma biçimini değiştirir. Önceki sürümlerde, boyut kümeleri tüm tarihler için yeniden oluşturuluyordu. Örneğin, 2020 yılını kapatıyorsanız sistem yalnızca 2020 mali yılı içindeki hareketlerin bakiyelerini yeniden oluşturur. 1 Kasım 2020 ile 30 Kasım 2020 tarihleri arasında bir konsolidasyon işlemi çalıştırıyorsanız sistem yalnızca o tarih aralığının bakiyelerini yeniden oluşturur.

Bu özellik, hataya neden olan değişiklik olarak kabul edilir; özelliği **Özellik yönetimi** çalışma alanını kullanarak etkinleştirmeniz gerekir.
 
[![Yıl sonu kapanışı](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Borç hesapları: 2020 yılı için 1099 yıl sonu raporlamasını desteklemek üzere ne gibi değişiklikler yapıldı?

2020 yılında 1099 yıl sonu değişiklikleri için iki yeni düzenleyici özellik eklendi. **2020 için 1099-NEC ve 1099-MISC formlarındaki değişiklikleri uygulama** adlı ilk özellik, zorunlu bir özellik olarak yıl ortasında kullanıma sunuldu. Amacı, 2020 yılına ait 1099 işlem verilerinin yeni 1099-NEC formu için izlenebilmesidir. Bu özellikle, yeni 1099-NEC'yi desteklemek için gereken 1099 alanları eklendi ve 1099-MISC alanları güncelleştirildi. Bu güncelleştirmeyle, 1099 kutusu bilgileri için satıcı kayıt verileri de yükseltildi. 

**2020 vergi kanunu için güncelleştirilmiş 1099 beyannameleri** adlı ikinci düzenleyici özellik, aşağıdaki değişiklikleri içerir.

- 1099-OID: IRS, formu sürekli kullanıma dönüştürmüştür.
   - Yazdırıldığında raporlama yılının 3. ve 4. hanesi doldurulmalıdır. **Raporlama yılı** alanının **1099 vergisi yazdırma seçeneklerindeki** 3. ve 4. hanelerini kullanın. 

- 1099-NEC: 2020 için yeni form. Bu form, çalışan dışındaki tazminatları kaydeder. 

-   1099-MISC: 1099-NEC formunun oluşturulması nedeniyle, IRS, 1099-MISC formunu revize etti ve belirli gelirlerin raporlanması için kutu numaralarını yeniden düzenledi.
Gelir bildiriminde ve formun kutu numaralarındaki değişiklikler aşağıda listelenmiştir.
   - Mükellefin 5000 dolar veya üzeri doğrudan satış yapmış olması (onay kutusu) kutu 7'de bildirilir.
   - Ürün sigortası gelirleri kutu 9'da bildirilir.
   - Bir avukatın brüt geliri kutu 10'da bildirilir.
   - Bölüm 409A ertelemeleri, kutu 12'de bildirilir.
   - Niteliksiz ertelenmiş tazminat geliri, kutu 14'te bildirilir.
   - Kutu 15, 16 ve 17 sırasıyla kesilen eyalet vergilerini, eyalet kimlik numarasını ve eyalette kazanılan gelirin miktarını bildirir.

- 2020 yılında 1099-DIV veya 1099-INT için değişiklik yapılmamıştır.

- Elektronik dosyalama: Biçim, yeni NEC formunu barındıracak şekilde değiştirildi ve yukarıda açıklanan MISC kutusu değişiklikleri yapıldı. Elektronik dosyalama gereksinimleri hakkında özel bilgiler için [IRS Yayını 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf)'ye bakın.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Borç hesapları: 1099: Yıl boyunca 1099 bilgilerini takip etmeyen bir satıcının 1099 kutusunu ve değerlerini nasıl değiştirebilirim?
1099 verilerini **Satıcı** sayfasındaki **1099 Vergisi** sekmesindeki ayarlara göre doğru şekilde yeniden atamak amacıyla daha önce ödenen fatura hareketlerine göz atmak için 1099'u Güncelleştir işlevini (**Borç hesapları > Satıcılar > Tüm satıcılar > Satıcı seçin > Şeritteki Satıcı sekmesi > 1099'u güncelleştir**) kullanın.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>1099'u Güncelleştir işlevini tüm satıcılarım için aynı anda çalıştırabilir miyim?
Hayır. 1099'u Güncelleştir yordamı, tek seferde tek bir satıcı için gerçekleştirilir. Kuruluşunuz tarafından bu gereksinim gerekiyorsa lütfen [Satıcının 1099 Verilerinin Güncelleştirilmesi için Toplu İşlem](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8) başlıklı fikre oy verin.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Borç hesapları: 1099: 1099'u Güncelleştir aracında "Mevcut 1099 tutarlarını yeniden hesapla" ve "Tümünü güncelleştir".
**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, **Tümünü güncelleştir** onay kutusuyla birlikte kullanıldığında 1099 tutarını ödenen toplam değerlere sıfırlar. 

[![1099 Vergisi hareketleri: Güncelleştirme yordamını çalıştırmadan önce](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, yalnızca faturada kısmi 1099 değerleri olduğunda veya 1099 Vergisi formunda değiştirildiğinde devreye girer. Örneğin, 1000,00 dolar değerinde bir faturanız olduğunu ancak kullanıcının 1099 tutarına el ile 500,00 dolarlık fatura girdiğini varsayalım.

[![1099 Vergisi hareketleri: Tümünü güncelleştir ve Mevcut 1099 tutarlarını yeniden hesapla](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Bu ödendiğinde, ödenen 1099 tutarı 500,00 dolar olacaktır. Yeniden hesaplama yordamını gerçekleştirirseniz sistem, 1099 tutarını ödenen toplam tutar olan 1000,00 dolar olarak değiştirir.

[![1099 Vergisi hareketleri: 1099 yordamını çalıştırdıktan sonra](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Borç hesapları: 1099: 1099 hareketlerini el ile oluştur
Bir kuruluşun faturayla ilişkili olmayan 1099 hareketlerini el ile oluşturması gerekebilir. **Borç hesapları > Periyodik görevler > 1099 vergisi > 1099 için satıcı kapatma**'ya giderek 1099 hareketlerini el ile ekleyebilirsiniz. **El ile 1099 hareketleri** düğmesini seçin. 

El ile oluşturulan 1099 hareketleri **1099'u Güncelleştir** arasında **Tümünü güncelleştir** işlemi veya **Mevcut 1099 tutarlarını yeniden hesapla** işlemiyle güncelleştirilmez.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Borç hesapları: 1099: Dynamics 365 Finance, 1096 formunu destekler mi? 

Dynamics 365 Finance 1096 Yıllık Özeti'ni ve ABD Bilgi Beyannamelerinin İletimi formunu yazdırmaz.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Borç hesapları: 1099: Kamu sektörü için 1099 raporlamasını destekleyen yeni özellikler var mı? 
Kamu sektörüne yönelik **1099 bilgilerini ana hesaba göre güncelleştir** adlı yeni bir özellik eklenmiştir. Özelliği, **Özellik yönetimi** çalışma alanından etkinleştirebilirsiniz. Bu özellik, satıcının 1099 değerlerini satıcı kaydındaki varsayılan hesap yerine, muhasebe dağılımındaki ana hesaba göre ilişkilendirmenize olanak tanır.

Daha fazla bilgi için bkz. [1099 raporlamasına ilişkin satıcıları ayarlama](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]