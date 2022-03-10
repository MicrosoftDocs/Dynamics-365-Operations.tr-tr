---
title: Yıl sonu faaliyetleriyle ilgili SSS
description: Bu konuda, yıl sonunda ortaya çıkabilecek sorular ve yıl sonu kapanışı faaliyetlerine yardımcı olabilecek yanıtlar listelenmektedir.
author: moaamer
ms.date: 12/21/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b0560024d87ad72c7ab77eaff52a305a4ab5a089
ms.sourcegitcommit: cd0ba5f0ac7c44d36559a3e6e0fffb6ed18f9a20
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/28/2021
ms.locfileid: "7947274"
---
# <a name="year-end-activities-faq"></a>Yıl sonu faaliyetleriyle ilgili SSS 

[!include [banner](../includes/banner.md)]

Bu konuda, yıl sonunda ortaya çıkabilecek sorular ve yıl sonu kapanışı faaliyetlerine yardımcı olabilecek yanıtlar listelenmektedir. Bu konu başlığındaki bilgiler öncelikle Genel muhasebe ve Borç hesapları için yıl sonu kapanış faaliyetlerine ilişkin sorulara odaklanmaktadır.

## <a name="general-ledger-year-end-enhancements"></a>Genel muhasebe yıl sonu geliştirmeleri 
10.0.20 sürümünde, bir yıl sonu kapanışı geliştirmesi kullanıma sunulmuştur ve bu geliştirme, 10.0.25 sürümünden itibaren varsayılan olarak etkindir. Kuruluşunuzda 10.0.25 sürümünden daha eski bir sürüm kullanılıyorsa yıl sonu kapanışı işlemine başlamadan önce bu özelliği etkinleştirmenizi öneririz. Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için Özellik yönetimi çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

 - Modül: Genel muhasebe
 - Özellik adı: Genel muhasebe yıl sonu geliştirmeleri

Yıl sonu kapanışı şablonlarının kurulumu, yeni bir kurulum sayfasına (**Yıl sonu kapanışı şablonu kurulumu**) taşınmıştır. Mevcut yıl sonu kapanışı sayfası, Genel muhasebe yabancı para birimi yeniden değerleme işlemine benzer şekilde değiştirilecektir. Burada, yıl sonu kapanışı işlemi her çalıştırıldığında veya tersine çevrildiğinde bir liste görüntülenir. Bir muhasebe müdürü, yıl sonu kapanışı işlemini yeni sayfadan başlatabilir. 

Yıl sonu kapanışı işlemini tersine çevirmek için uygun tüzel kişilik için en son mali yılı seçin ve **Yıl sonu kapanışını tersine çevir** düğmesini seçin. Tersine çevirme işlemi, önceki yıl sonu kapanışı işleminin muhasebe girişlerini siler ve yıl sonu kapanışı işlemi otomatik olarak yeniden çalıştırılmaz. 

Mali yıl ve tüzel kişilik için işlemi yeniden başlatarak yıl sonu kapanışını yeniden çalıştırabilirsiniz. İşlem kapsamında, yıl sonu kapanışı yeniden çalıştırma işleminin yalnızca yeni veya değiştirilmiş hareketleri mi dikkate alacağını yoksa önceki kapatma işlemini tamamen tersine çevirerek işlemi tüm hareketler için mi yeniden çalıştıracağını belirlemek için Genel muhasebe parametre ayarı kullanılmaya devam edilir.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Genel muhasebe: Yıl sonu kapanışını çalıştırdığımızı ve geri almadığımızı nasıl anlarım?
Kuruluşların yıl sonu kapanışını yürütmeye çalışıp bunun yerine yıl sonu kapanışını geri almaya çalıştıklarını tespit ettik. Yıl sonu kapanışı gerçekten hızlı bir şekilde sonlanıyorsa veya yıl sonu kapanışı açılış bakiyeleri oluşturmuyorsa **Yıl sonu kapanışı**'ndaki (**Genel muhasebe > Dönem kapanışı > Yıl sonu kapanışı > Mali kapanışı çalıştır**) **Önceki kapanışı geri al** ayarını doğrulayın. 

[![Yıl sonu kapanışını çalıştırma ve yıl sonu kapanışını geri alma.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

**Önceki kapanışı geri al** seçimi **Evet** olarak ayarlanırsa önceki yıl sonu kapanışı tersine çevrilir. Geri alma işlemi çalıştırılırken, yıl sonu kapanışı hiç çalıştırılmamış gibi tüm kapanış bakiyesi ve açılış bakiyesi girişleri silinir. Fişler silinir. Yıl sonu kapanışı otomatik olarak yeniden çalıştırılmaz. İşlemi yeniden başlatmanız gerekir, bu kez **Önceki kapanışı geri al** seçeneğini **Hayır** olarak değiştirin. 

> [!NOTE]
> Kapanış bakiyesi girişi isteğe bağlı olarak kapatılan yıl içinde oluşturulur. Bu durum yalnızca **Aktarım sırasında kapanış hareketleri oluştur** adlı Genel muhasebe parametresi **Evet** olarak ayarlanırsa oluşur. Açılış bakiyesi girişi her zaman oluşturulur çünkü bu, gelecek yılın başlangıç bakiyesidir.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Genel muhasebe: Yıl sonu kapanışı için Geri Al ve Sil GL parametresi arasındaki fark nedir?
**Yıl sonu kapanışı** iletişim kutusunda bulunan **Önceki kapanışı geri al** parametresi ile Genel muhasebede (**Genel muhasebe > Dönem kapanışı > Yıl sonu kapanışı > Mali kapanışı çalıştır**) yer alan **Aktarım sırasında yıl sonu kapanışı hareketlerini sil** parametresi arasındaki farkla ilgili bir karışıklık söz konusu olabilir.  

[![Yıl sonu kapanışı için Geri Al ile Sil GL parametresi arasındaki fark.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Yıl sonu kapanışı hiç çalıştırılmamış gibi, tüm kapanış ve açılış bakiyesi girişlerini silmek için yıl sonu kapatma işlemi çalıştırılırken açılan iletişim menüsünde **Önceki kapanışı geri al**'ı seçin. Fişler silinir. Yıl sonu kapanışı otomatik olarak yeniden çalıştırılmaz. Yıl sonu kapanışını çalıştırmak için bu işlemi yeniden başlatmanız gerekir. Bu kez, **Önceki kapanışı geri al** seçeneğini **Hayır** olarak ayarlayın (**Genel muhasebe > Genel muhasebe kurulumu > Genel muhasebe parametreleri**). 

[![Genel muhasebe parametresi ayarı.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

Genel muhasebedeki **Aktarım sırasında yıl sonu hareketlerini sil** parametresi, yalnızca yıl sonu kapanışını çalıştırırken (geri alırken değil) kullanılır (**Önceki kapanışı geri al** seçimi **Hayır** olarak ayarlanmıştır). Bu parametre **Evet** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri silinir ve yıl sonu kapanışı yeniden çalıştırılır. Bu işlem, kuruluş son yıl sonu kapanışından sonraki ayarlamalar da dahil olmak üzere tüm hareketlerin kapanış bakiyesi ve açılış bakiyesi girişleri için tek bir muhasebe girişinde deftere naklini istediğinde kullanılır. 

Bu seçenek **Hayır** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri kalır. Bu girişler silinmez. Bunun yerine, yalnızca o mali yılda son yıl sonu kapanışından bu yana deftere nakledilen değiştirilmiş veya yeni hareketler için yeni bir kapanış bakiyesi ve açılış bakiyesi girişi oluşturulur.  

> [!NOTE]
> Kapanış bakiyesi girişi, kapatılan yıl içinde oluşturulur. Bu durum yalnızca Genel muhasebedeki **Aktarım sırasında kapanış hareketleri oluştur** parametresi **Evet** olarak ayarlandığında oluşur. Açılış bakiyesi girişi her zaman oluşturulur çünkü bu, gelecek yılın başlangıç bakiyesidir. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Genel muhasebe: Yıl sonu işleme performansını artırmak için neler değiştirilebilir? 
Yıl sonu kapanışının performansını artırmak için bir dizi değişiklik yapabilirsiniz. Değişikliğin kuruluşunuz için uygun olup olmadığını değerlendirmek için önerilen bu değişiklikleri dikkate almanızı öneririz.  

### <a name="dimension-sets"></a>Boyut kümeleri
Yıl sonu kapanışını çalıştırırken, her boyut kümesi bakiyesi yeniden oluşturulur ve performans üzerinde doğrudan bir etkisi olur. Bazı kuruluşlar, boyut kümeleri bir noktada kullanıldıkları veya kullanılabilecekleri için gereksiz boyut kümeleri oluşturur.  Bu gereksiz boyut kümeleri, yıl sonu kapanışı sırasında yeniden oluşturulmaya devam eder ve işlemin daha uzun sürmesine neden olur. Boyut kümelerinizi değerlendirmek ve gereksiz boyut kümelerini silmek için zaman ayırın.

Gereksiz boyut kümeleri **BudgetDimensionFocusInitializeBalance** (**Genel muhasebe > Hesap planı > Boyutlar > Mali boyut kümeleri)** toplu işini de etkiler.

[![Mali boyut kümeleri.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Yıl sonu kapanış şablonu yapılandırması
Yıl sonu kapanış şablonu, kuruluşların kar ve zarar bakiyelerini yedek akçeye aktarırken korunmasını istedikleri mali boyut düzeyini seçmelerine olanak tanır. Ayarlar, kuruluşların bakiyeleri yedek akçeye taşırken ayrıntılı mali boyutları (**Tümünü kapat**) korumasına veya tutarları tek bir boyut değerine (**Tekli kapat**) özetlemeyi seçmesine olanak tanır. Bu durum, her mali boyut için tanımlanabilir. Bu ayarlar hakkında daha fazla bilgi için [Yıl sonu kapanışı](year-end-close.md) konu başlığına bakın.

Kuruluşunuzun gereksinimlerini değerlendirmenizi ve mümkünse performansı artırmak için **Tekli kapat** yıl sonu kapanışı seçeneğini kullanarak mümkün olduğunca çok boyutu kapatmanızı öneririz. Tek bir boyut değerine (boş bir değer de olabilir) kapatarak sistem, yedek akçe hesabı girişleri için bakiyeleri belirlerken daha az ayrıntı hesaplar.

## <a name="degenerate-dimensions"></a>Bozuk boyutlar

Bozuk boyutlar, kendi başına ve diğer boyutlarla birlikte yeniden kullanım için az imkân sağlar veya hiç imkân sağlamaz. İki tür bozuk boyut bulunur. İlk tür, ayrı olarak bozulan bir boyuttur. Genellikle bu bozuk boyut türü, yalnızca tek bir harekette veya küçük hareket kümelerinde görünür. İkinci tür, üretilebilecek olası permütasyonlara göre aynı potansiyeli gösteren bir veya daha fazla ek boyutla birlikte bozuk hâle gelen bir boyuttur. Bozuk bir boyut, yıl sonu kapanışı işleminin performansı üzerinde önemli bir etkiye sahip olabilir. Performans sorunlarını en aza indirmek için önceki bölümde açıklandığı üzere, yıl sonu kapanışı kurulumunda tüm bozuk boyutları **Tekli kapat** olarak tanımlayın.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Genel muhasebe: Dönem kapanışı, yıl sonu kapanışı ne işe yarar?
 
[![Dönem kapanışı, yıl sonu kapanışı.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Mali boyut kümelerini yeniden oluşturmaya yönelik performans iyileştirmeleri
10.0.16 sürümüne eklenen yeni bir özellik, yıl sonu kapanışı ve konsolidasyon işlemlerinin performansını artırır. Özellik, Mali boyut kümelerinin yeniden oluşturulması için performans iyileştirmeleri olarak adlandırılmıştır. Bu özellik, boyut kümelerinin yalnızca ilgili bir zaman dilimi için yeniden oluşturulabilmesi için boyut kümelerinin yeniden oluşturulma biçimini değiştirir. Önceki sürümlerde, boyut kümeleri tüm tarihler için yeniden oluşturuluyordu. Örneğin, 2020 yılını kapatıyorsanız sistem yalnızca 2020 mali yılı içindeki hareketlerin bakiyelerini yeniden oluşturur. 1 Kasım 2020 ile 30 Kasım 2020 tarihleri arasında bir konsolidasyon işlemi çalıştırıyorsanız sistem yalnızca o tarih aralığının bakiyelerini yeniden oluşturur.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için Özellik yönetimi çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:
 
- Modül: Genel muhasebe
- Özellik adı: Mali boyut kümelerinin yeniden oluşturulması için performans iyileştirmeleri

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Borç hesapları: 2021 yılı için 1099 yıl sonu raporlamasını desteklemek üzere ne gibi değişiklikler yapıldı?

2021'de, DIV, NEC ve MISC formları biraz değiştirildi ve bazı ek kutular eklendi.

#### <a name="div-new-box2e-2f"></a>DIV: yeni kutu 2e, 2f
 
- Kutu 2e. Kutu 1a'daki tutarın ABD gayrimenkul hakları (USRPI) satışıyla ilişkilendirilebilen bölüm 897 bölümünü gösterir.  
- Kutu 2F. Kutu 2a'daki tutarın USRPI satışıyla ilişkilendirilebilen bölüm 897 bölümünü gösterir. 2e ve 2F kutularının, aktarıldığında veya dağıtıldığında gelirleri kendi karakterlerini koruyan yabancı kişiler ve tüzel kişilikler ya da doğrudan veya dolaylı yabancı sahiplere veya hak sahipleri için geçerli olduğunu unutmayın. Genellikle Amerika Birleşik Devletleri'ndeki bir ticari kuruluş veya işletmeye doğru şekilde bağlı olarak kabul edilir. Vergi iadeniz için yönergelere bakın. 
 
#### <a name="nec-new-box-2"></a>NEC: yeni kutu 2 
 
Kutu 2 işaretlendiğinde size yeniden satış, satın alıp satma, depozito komisyonu veya diğer temelde satılan, toplamı 5.000 ABD doları veya daha fazla olan tüketici ürünlerini bildirin. Genel olarak, bu ürünlerin satışından elde edilen tüm gelirleri Çizelge C'de (Form 1040) bildirin. 
 
Bu arada, NEC formunun boyutu değiştirilmiştir. Yazdırma sırasında, her sayfada üç form bulunur. 
 
#### <a name="misc-new-box-11"></a>MISC: yeni kutu 11 
 
Kutu 11, balıkçılık ticareti veya işletmesiyle ilgilenen herkesten alınan, yeniden satış amaçlı balık satın alımı için ödenen tutarı gösterir. Bu geliri bildirmek için vergi iadesi yönergelerine bakın. 
 
#### <a name="electronic-filing"></a>Elektronik dosyalama 
Elektronik dosyalama hakkında bilgi için bkz. [Elektronik dosyalama için yayımlama gereksinimleri](https://www.irs.gov/pub/irs-pdf/p1220.pdf).

2021 e-raporu için Biçim Teknik Özelliklerini ve Kayıt Düzenlerini Güncelleştirme 
- Bölüm 2 Veren "A" Kaydı. 
- Tutar Kodları: Alan Pozisyonu 28-45, Uzunluk 18 olarak artırıldı. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Bölüm 2 Veren "A" Kaydı, 1099-DIV Formunda Ödemeleri Bildirmek İçin: 
- Tutar Türü: Bölüm 897 Normal Kar Payları ve Tutar Kodu H eklendi. 
- Tutar Türü: Bölüm 897 Sermaye Kazançları ve Tutar Kodu J eklendi. 
 
#### <a name="sec-3-payee-b-record"></a>Bölüm 3 Alacaklı "B" Kaydı 
- Genel Bilgi Kayıtları: 16-18 Ödeme Tutarı Alanlarının üçüncü madde işareti güncelleştirildi. 
- Alan Başlığı Ödemesi H: Alan Pozisyonu 247-258, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Alan Başlığı Ödemesi J: Alan Pozisyonu 259-270, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Boş alan, Alan Pozisyonu 271-286 olarak güncelleştirildi. 
- Yabancı Ülke Göstergesi, Alan Pozisyonu 287 olarak güncelleştirildi. 
- Alacaklı Adı alanı, Alan Pozisyonu 288-327 olarak güncelleştirildi. 
- Alacaklı İkinci Adı alanı, Alan Pozisyonu 328-367 olarak güncelleştirildi. 
- Kayıt Düzeni Pozisyonları, Form 1099-MISC: Alan Pozisyonu 548 ve Alan Başlığı FATCA Dosyalama Gereksinimi Göstergesi silindi. 
- Kayıt Düzeni Pozisyonları, Form 1099-NEC: 545-546 Boş olarak güncelleştirildi, 547 alanı Doğrudan Satış Göstergesi, Uzunluk ve Açıklama ve Açıklamalar olarak güncelleştirildi, 548-722 alanı Boş olarak güncelleştirildi. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Bölüm 4 Veren Sonu "C" Kaydı 
- Alan Başlığı Ödemesi H: Alan Pozisyonu 304-321, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Alan Başlığı Ödemesi J: Alan Pozisyonu 322-339, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Alan Başlığı 340-499: Uzunluk 160 olarak güncelleştirildi. 
 
#### <a name="sec-5-state-totals-k-record"></a>Bölüm 5 Eyalet Toplamları "K" Kaydı 
- Alan Başlığı Ödemesi H: Alan Pozisyonu 304-321, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Alan Başlığı Ödemesi J: Alan Pozisyonu 322-339, Alan Başlığı, Uzunluk ve Genel Alan Açıklaması güncelleştirildi. 
- Alan Başlığı 340-499: Uzunluk 160 olarak güncelleştirildi.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Borç hesapları: 1099: Yıl boyunca 1099 bilgilerini takip etmeyen bir satıcının 1099 kutusunu ve değerlerini nasıl değiştirebilirim?
1099 verilerini **Satıcı** sayfasındaki **1099 Vergisi** sekmesindeki ayarlara göre doğru şekilde yeniden atamak amacıyla daha önce ödenen fatura hareketlerine göz atmak için 1099'u Güncelleştir işlevini (**Borç hesapları > Satıcılar > Tüm satıcılar > Satıcı seçin > Şeritteki Satıcı sekmesi > 1099'u güncelleştir**) kullanın.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>1099'u Güncelleştir işlevini tüm satıcılarım için aynı anda çalıştırabilir miyim?
Hayır. 1099'u Güncelleştir yordamı, tek seferde tek bir satıcı için gerçekleştirilir. Kuruluşunuz tarafından bu gereksinim gerekiyorsa lütfen [Satıcının 1099 Verilerinin Güncelleştirilmesi için Toplu İşlem](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8) başlıklı fikre oy verin.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Borç hesapları: 1099: 1099'u Güncelleştir aracında "Mevcut 1099 tutarlarını yeniden hesapla" ve "Tümünü güncelleştir"
**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, **Tümünü güncelleştir** onay kutusuyla birlikte kullanıldığında 1099 tutarını ödenen toplam değerlere sıfırlar. 

[![1099 Vergisi hareketleri: Güncelleştirme yordamını çalıştırmadan önce.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, yalnızca faturada kısmi 1099 değerleri olduğunda veya 1099 Vergisi formunda değiştirildiğinde devreye girer. Örneğin, 1000,00 dolar değerinde bir faturanız olduğunu ancak kullanıcının 1099 tutarına el ile 500,00 dolarlık fatura girdiğini varsayalım.

[![1099 Vergisi hareketleri: Tümünü güncelleştir ve Mevcut 1099 tutarlarını yeniden hesapla seçeneklerini işaretleme.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Bu ödendiğinde, ödenen 1099 tutarı 500,00 dolar olacaktır. Yeniden hesaplama yordamını gerçekleştirirseniz sistem, 1099 tutarını ödenen toplam tutar olan 1000,00 dolar olarak değiştirir.

[![1099 Vergisi hareketleri: 1099 yordamını çalıştırdıktan sonra.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Borç hesapları: 1099: 1099 hareketlerini el ile oluştur
Bir kuruluşun faturayla ilişkili olmayan 1099 hareketlerini el ile oluşturması gerekebilir. **Borç hesapları > Periyodik görevler > 1099 vergisi > 1099 için satıcı kapatma**'ya giderek 1099 hareketlerini el ile ekleyebilirsiniz. **El ile 1099 hareketleri** düğmesini seçin. 

El ile oluşturulan 1099 hareketleri **1099'u Güncelleştir** arasında **Tümünü güncelleştir** işlemi veya **Mevcut 1099 tutarlarını yeniden hesapla** işlemiyle güncelleştirilmez.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Borç hesapları: 1099: Dynamics 365 Finance, 1096 formunu destekler mi? 

Dynamics 365 Finance 1096 Yıllık Özeti'ni ve ABD Bilgi Beyannamelerinin İletimi formunu yazdırmaz.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Borç hesapları: 1099: Kamu sektörü için 1099 raporlamasını destekleyen yeni özellikler var mı? 
Kamu sektörüne yönelik **1099 bilgilerini ana hesaba göre güncelleştir** adlı yeni bir özellik eklenmiştir. Özelliği, **Özellik yönetimi** çalışma alanından etkinleştirebilirsiniz. Bu özellik, satıcının 1099 değerlerini satıcı kaydındaki varsayılan hesap yerine, muhasebe dağılımındaki ana hesaba göre ilişkilendirmenize olanak tanır.

Daha fazla bilgi için bkz. [1099 raporlamasına ilişkin satıcıları ayarlama](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
