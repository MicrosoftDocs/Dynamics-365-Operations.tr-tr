---
title: Yıl sonu faaliyetleriyle ilgili SSS
description: Bu makalede, yıl sonunda ortaya çıkabilecek sorular ve yıl sonu kapanışı faaliyetlerine yardımcı olabilecek yanıtlar listelenmektedir.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853055"
---
# <a name="year-end-activities-faq"></a>Yıl sonu faaliyetleriyle ilgili SSS 

[!include [banner](../includes/banner.md)]

Bu makalede, yıl sonunda ortaya çıkabilecek sorular ve yıl sonu kapanışı faaliyetlerine yardımcı olabilecek yanıtlar listelenmektedir. Bu makaledeki bilgiler, öncelikle Genel muhasebe ve Borç hesapları için yıl sonu kapanış faaliyetlerine ilişkin sorulara odaklanmaktadır.

## <a name="general-ledger-year-end-enhancements"></a>Genel muhasebe yıl sonu geliştirmeleri

Microsoft Dynamics 365 Finance 10.0.20 sürümünde, bir yıl sonu kapanışı geliştirmesi kullanıma sunulmuştur. Bu geliştirme, varsayılan olarak 10.0.25 sürümünden itibaren etkinleştirilir ve 10.0.29 sürümünden itibaren zorunludur. Kuruluşunuzda 10.0.25 sürümünden daha eski bir sürüm kullanılıyorsa yıl sonu kapanışı işlemine başlamadan önce bu özelliği etkinleştirmenizi öneririz. Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için **Özellik yönetimi** çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** Genel muhasebe
- **Özellik adı:** Genel muhasebe yıl sonu geliştirmeleri

Yıl sonu kapanışı şablonlarının kurulumu, yeni bir kurulum sayfasına (**Yıl sonu kapanışı şablonu kurulumu**) taşınmıştır. Mevcut yıl sonu kapanışı sayfası, **Genel muhasebe yabancı para birimi yeniden değerleme işlemi** sayfasına benzer olacaktır. Burada, yıl sonu kapanışının çalıştırıldığı veya tersine çevrildiği her işlem liste şeklinde gösterilir. Sayfa, özellik etkinleştirilmeden önce yapılan yıl sonu kapanışlarıyla ilgili geçmiş bilgileri göstermez. Bir muhasebe müdürü, yıl sonu kapanışı işlemini yeni sayfadan başlatabilir.

Yıl sonu kapanışını tersine çevirmek üzere uygun tüzel kişilik için en son mali yılı ve ardından **Yıl sonu kapanışını tersine çevir**'i seçin. Tersine çevirme işlemi, önceki yıl sonu kapanışı işleminin muhasebe girişlerini siler ve işlem otomatik olarak yeniden çalıştırılmaz. **Genel muhasebe yıl sonu geliştirmeleri** özelliğini bir yıl sonu kapanışını tamamladıktan sonra etkinleştirir ve geçmiş yıl sonu sonuçlarını tersine çevirmek isterseniz, **Yılı tekrar kapatırken mevcut yıl sonu kapanışı girişlerini sil** Genel muhasebe parametresini etkinleştirdikten sonra geçmiş yıl sonu kapanışını yeniden çalıştırın.

Mali yıl ve tüzel kişilik için işlemi yeniden başlatarak yıl sonu kapanışını yeniden çalıştırabilirsiniz. İşlem kapsamında, yıl sonu kapanışını yeniden çalıştırma işleminin yalnızca yeni veya değiştirilmiş hareketleri mi dikkate alacağını yoksa önceki kapanış işlemini tamamen tersine çevirerek işlemi tüm hareketler için mi yeniden çalıştıracağını belirlemek için Genel muhasebe parametre ayarı kullanılmaya devam edilir.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Genel muhasebe: Genel muhasebe yıl sonu geliştirmeleri özelliğini etkinleştirdim. Yıl sonu kapanışı sayfasının Geçmiş bölümünde, önceki yıl kapanışlarımı neden görüntüleyemiyorum?

**Genel muhasebe yıl sonu geliştirmeleri** özelliği etkinleştirilmeden önce, son yıl sonu kapanışı işleminin çalıştırıldığı tarih ve saat izlenir. Her yıl sonu kapanışı işlemi için geçmiş izlenmez. Bu nedenle, her yıl sonu kapanışı çalıştırmasının ayrıntılarını göremezsiniz. Özellik etkinleştirildikten sonraki yıl sonu kapanışı işlemine ilişkin bilgiler korunur. Özellik etkinleştirilmeden önce çalıştırılsa bile tüm yıl sonu kapanışı işlemlerindeki fişler, **Fiş hareketleri** sayfasında görüntülenebilir. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Genel muhasebe: Yıl sonu kapanışı işlemi, şu hata nedeniyle başarısız oldu: "Kapatmakta olduğunuz mali yılda deftere nakledilen bir veya daha fazla genel muhasebe hareketi, farklı bir mali yıldaki bir genel muhasebe hareketi için kapatıldığından yıl sonu kapanışı çalıştırılamıyor." Bu hata ne anlama geliyor?

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliği etkinleştirildiği için yalnızca kapatılan mali yıla ait kapatılan genel muhasebe hareketleri açılış bakiyesinden hariç tutulur. Bu davranış, borçların ve alacakların bakiye dışı olmasına neden olur. Daha fazla bilgi için [Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık](awareness-between-ledger-settlement-year-end-close.md) bölümünü inceleyin.

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Genel muhasebe: Yıl sonu kapanışını tersine çevirme işlemi, şu hata nedeniyle başarısız oldu:" 01.01.2023 mali yılı için başlangıç bakiyesi hareketi genel muhasebede kapatıldığından 01.01.2022 mali yılının yıl sonu kapanışı geri alınamaz." Bu hata ne anlama geliyor?

**Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliği etkinleştirildiği için yıl sonu işlemesi, açılış hareketleri yeni mali yılda kapatıldıysa tersine çevrilemez. 1 Ocak 2022 için yıl sonu kapanışını tersine çevirmeden önce yeni 2023 mali yılındaki genel muhasebe kapatma işlemini tersine çevirin. Alternatif olarak 1 Ocak 2022 için yılı yeniden kapatabilirsiniz ancak işlemi yalnızca yeni düzenlenen girişlerde gerçekleştirin. Yılı yalnızca ayarlamalar için tekrar kapatmak istiyorsanız **Yılı tekrar kapatırken mevcut yıl sonu girişlerini sil** Genel muhasebe parametresini devre dışı bırakın.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Genel muhasebe: Genel muhasebe kapatma otomasyonu neden Aralık ayının genel muhasebe kapatma hareketlerini işlemiyor?

**Genel muhasebe kapatma işlemlerini otomatikleştir** özelliği, mali yılın ilk gününden tekrarın çalıştırıldığı geçerli tarihe kadar olan hareketler için otomasyonu çalıştırır. 31 Aralık'ta sona eren mali yıllarda, Aralık'ta çalıştırıldığından emin olmak için tekrarınızın yürütme tarihini ayarlamanız gerekebilir. Örneğin, otomasyon her ayın ilk günü çalıştırılacak şekilde ayarlanır. Bu otomasyon 1 Aralık 2022'de çalıştırılır ve 1 Ocak 2023'te çalıştırılacak şekilde planlanmıştır. 1 Ocak 2023'te çalıştırılacak tekrarı, 31 Aralık 2022'de çalıştırılması için değiştirmenizi öneririz. Bu değişiklik, 2-31 Aralık tarihleri arasında yapılan hareketlerin otomatik kapatmaya dahil edilmesini sağlar.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Genel muhasebe: Yıl sonu kapanışı için "Yıl sonu kapanışını tersine çevir" eylemi ve "Tekrar kapatırken mevcut yıl sonu girişlerini sil" parametresi arasındaki fark nedir?

**Yıl sonu kapanışını tersine çevir** eylemiyle Genel muhasebedeki (**Genel muhasebe \> Muhasebe kurulumu \> Genel muhasebe parametreleri**) **Tekrar kapatırken mevcut yıl sonu girişlerini sil** parametresi arasındaki farklar kafa karıştırıcı olabilir.

Yıl sonu kapanışı hiç çalıştırılmamış gibi, tüm kapanış bakiyesi ve açılış bakiyesi girişlerini silmek için yıl sonu kapanışı işlemini çalıştırırken **Yıl sonu kapanışını terine çevir** eylemini seçin. Bu durumda fişler silinir. Yıl sonu kapanışı otomatik olarak yeniden çalıştırılmaz. Yıl sonu kapanışını çalıştırmak için **Yıl sonu kapanışını çalıştır** eylemini seçin.

Genel muhasebedeki **Yılı tekrar kapatırken mevcut yıl sonu girişlerini sil** parametresi yıl sonu kapanışını tersine çevirirken değil, yalnızca çalıştırırken kullanılır. Bu parametre **Evet** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri silinir ve yıl sonu kapanışı yeniden çalıştırılır. Bu seçenek, bir kuruluş son yıl sonu kapanışından sonraki ayarlamalar dahil tüm hareketlerin, kapanış bakiyesi ve açılış bakiyesi girişleri için tek bir muhasebe girişinde deftere naklini istediğinde kullanılır. Parametre **Hayır** olarak ayarlanırsa tüm kapanış bakiyesi ve açılış bakiyesi girişleri kalır. Bu girişler silinmez. Bunun yerine, yalnızca o mali yılda son yıl sonu kapanışından bu yana deftere nakledilen değiştirilmiş veya yeni hareketler için yeni bir kapanış bakiyesi ve açılış bakiyesi girişi oluşturulur.

> [!NOTE]
> Kapanış bakiyesi girişi, kapatılan yıl içinde oluşturulur. Bu durum yalnızca Genel muhasebedeki **Aktarım sırasında kapanış hareketleri oluştur** parametresi **Evet** olarak ayarlandığında oluşur. Açılış bakiyesi girişi, gelecek yılın başlangıç bakiyesi olduğu için her zaman oluşturulur.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Genel muhasebe: Yıl sonu kapanışı işleminin Kar ve zarar boyutlarını aktar bölümündeki "Tümünü kapat" ve "Tekli kapat" seçenekleri arasındaki fark nedir?

**Tümünü kapat**, deftere nakledilen hareketlerdeki özgün mali boyut değerlerini korur ve bunları yedek akçe hesabında açılış bakiyelerini oluşturmak için kullanır. Ayrı yedek akçe başlangıç bakiyeleri, daha sonra her bir benzersiz mali boyut değer birleşimleri için oluşturulur. **Tekli kapat** seçiliyse bu mali boyuta sahip deftere nakledilmiş tüm hareketler, **Tekli kapat** seçeneğinden sonra görünen alana girilen boyut değeri için yedek akçe başlangıç bakiyesinde özetlenir. 

Örneğin, mali yıl için tüm hareketlerin Ana hesap - Departman hesap yapısıyla deftere nakledilmiş olduğunu varsayalım. Şablondaki Departman mali boyutu için **Tekli kapat** seçilir ve boyut değeri olarak 100 girilir. 200, 300 ve 400 departmanlarında deftere nakledilen tüm hareketleri toplam geliri 100.000 ABD doları ise, Yedek akçe - 100 için bir açılış bakiyesi oluşturulacaktır. **Tekli kapat**'ı seçer fakat mali boyut değerini boş bırakırsanız tüm hareketler bu boyut değeri boş olarak yedek akçede deftere nakledilir.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Genel muhasebe: Yıl sonu kapanışı işleminin Kar ve zarar boyutlarını aktar bölümündeki "Tekli kapat" seçeneğini belirlediğimde ayrıntılı işlem bilgilerimi kaybeder miyim?

**Tümünü kapat** ve **Tekli kapat** seçenekleri, kar ve zarar hesaplarında deftere nakledilen hareketlerdeki hangi mali boyutların yedek akçe ana hesabına aktarılacağını belirmek için kullanılır. Kar ve zarar hesaplarına yapılan eski ve ayrıntılı deftere nakil işlemleri etkilenmez ve ayrıntılar korunur. Bu seçenek, yeni yılda açılış bakiyesi olarak yedek akçe hesaplarına aktarılan ayrıntı düzeyini etkiler. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Genel muhasebe: Yılın raporlama para birimi eşleşmediğinden yıl sonu kapanış işlemi başarısız oluyor. Bu ne anlama geliyor?

Bu hata, **Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliği (Duyarlılık özelliği) etkinleştirildikten sonra yaşanabilir. Özellik etkinleştirildiğinde, kapatılan genel muhasebe hareketleri, genel muhasebe yıl sonu kapanışı çalıştırılırken bir sonraki mali yılın açılış bakiyesine dahil edilmez. Muhasebe bir raporlama para birimiyle tanımlanmışsa kapatılan genel muhasebe hareketleri hariç tutulduğunda, yıl sonu kapanışında müşteriler bir sorunla karşılaşabilir.   
Genel muhasebe kapatma işlemi yalnızca muhasebe para birimi için gerçekleştirilir.  Genel muhasebe hareketleri kapatıldığında, doğrulama yalnızca muhasebe para birimi borçlarının, muhasebe para birimi alacaklarına eşit olmasını sağlar. Bu genel muhasebe hareketlerinin raporlama para birimi tutarları doğrulanmaz ve borçlar alacaklara eşit olmayabilir.  Bununla birlikte genel muhasebe kapatma, raporlama para biriminde bir kazancı/kaybı otomatik olarak hesaplamaz ve deftere nakletmez.  Bu sınırlamalar nedeniyle, genel muhasebe kapatma işlemi yapılırken raporlama para biriminde bir kazanç/kayıp hareketi bulunmalıdır.  Kazanç/kayıp hareketi genel muhasebe kapanışına dahil edilmezse, yıl sonu kapanışı bir bakiye dışında iletisiyle sonuçlanır.  Daha fazla bilgi için [Genel muhasebe kapatma özelliği ve raporlama para birimi arasındaki duyarlılık bakiye dışı](reporting-currency-yec.md) bölümüne bakın.

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Genel muhasebe: Yıl sonu işleme performansını artırmaya yardımcı olmak için neler değiştirilebilir?

Yıl sonu kapanışının performansını artırmak için birkaç değişiklik yapabilirsiniz. Değişikliklerin kuruluşunuz için uygun olup olmadığına karar vermek için önerilen bu değişiklikleri değerlendirmenizi öneririz.

### <a name="optimize-year-end-close-service"></a>Yıl sonu kapanışını optimize etme hizmeti

**Yıl sonu kapanışını optimize etme** hizmeti, Microsoft Dynamics 365 Finance müşterilerinin büyük ölçekli yıl sonu işlemelerini bir mikro hizmete taşıyarak yıl sonu kapanışlarını hızlandırmasına olanak tanır. Verimli bir yıl sonu kapanışıyla kazanılan zaman, her Finance takımının finansal raporlar oluşturulurken gerekli ayarlamaları zamanında yapmasını sağlar. Yıl sonu kapanışı bir mikro hizmette işlendiğinde değerli kaynaklar serbest bırakılmış olur. İşlem yüksekliği SQL Server'daki yükü en aza indirir ve müşterilere yıl sonu kapanışı işlemini hızlandırmaları için bir fırsat sunar.

Daha fazla müşterinin yeni hizmeti 2022 yıl sonu döneminde kullanabilmesi için **Yıl sonu kapanışını optimize etme** hizmeti, 10.0.31 sürümünde kullanıma sunulmuştur. Hizmet 10.0.30 ve 10.0.29 sürümlerine de taşınmıştır. Daha fazla bilgi için [Yıl sonu kapanışını optimize etme](optimize-year-end-close.md) bölümüne bakın.

### <a name="dimension-sets"></a>Boyut kümeleri

Yıl sonu kapanışını çalıştırdığınızda, her boyut kümesi bakiyesi yeniden oluşturulur. Bu davranış, performansı doğrudan etkiler. Bazı kuruluşlar, boyut kümeleri bir noktada kullanıldıkları veya kullanılabilecekleri için gereksiz boyut kümeleri oluşturur. Bu gereksiz boyut kümeleri, yıl sonu kapanışı sırasında yeniden oluşturulmaya devam eder ve bu da işlemin daha uzun sürmesine neden olur. Boyut kümelerinizi değerlendirmek ve gereksiz olanları silmek için zaman ayırın.

Gereksiz boyut kümeleri **BudgetDimensionFocusInitializeBalance** (**Genel muhasebe \> Hesap planı \> Boyutlar \> Mali boyut kümeleri)** toplu işini de etkiler.

[![Mali boyut kümeleri.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Yıl sonu kapanış şablonu yapılandırması

Yıl sonu kapanış şablonu, kuruluşların kar ve zarar bakiyelerini yedek akçeye aktarırken korunmasını istedikleri mali boyut düzeyini seçmelerine olanak tanır. Ayarlar, kuruluşların bakiyeleri yedek akçeye taşırken ayrıntılı mali boyutları (**Tümünü kapat**) korumasına veya tutarları tek bir boyut değerine (**Tekli kapat**) özetlemeyi seçmesine olanak tanır. Bu durum, her mali boyut için tanımlanabilir. Bu ayarlar hakkında daha fazla bilgi için [Yıl sonu kapanışı](year-end-close.md) makalesine bakın.

Kuruluşunuzun gereksinimlerini değerlendirmenizi ve mümkünse performansı artırmak için **Tekli kapat** yıl sonu kapanışı seçeneğini kullanarak mümkün olduğunca çok boyutu kapatmanızı öneririz. Tek bir boyut değerine (boş bir değer de olabilir) kapatarak sistem, yedek akçe hesabı girişleri için bakiyeleri belirlerken daha az ayrıntı hesaplar.

### <a name="degenerate-dimensions"></a>Bozuk boyutlar

Bozuk boyutlar, kendi başına ve diğer boyutlarla birlikte yeniden kullanım için az imkân sağlar veya hiç imkân sağlamaz. İki tür bozuk boyut bulunur. İlk tür, ayrı olarak bozulan bir boyuttur. Genellikle bu bozuk boyut türü, yalnızca tek bir harekette veya küçük hareket kümelerinde görünür. İkinci tür, üretilebilecek olası permütasyonlara göre aynı potansiyeli gösteren bir veya daha fazla ek boyutla birlikte bozuk hâle gelen bir boyuttur. Bozuk bir boyut, yıl sonu kapanışı işleminin performansı üzerinde önemli bir etkiye sahip olabilir. Performans sorunlarını en aza indirmek için önceki bölümde açıklandığı üzere, yıl sonu kapanışı kurulumunda tüm bozuk boyutları **Tekli kapat** olarak tanımlayın.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Borç hesapları: 2022 yılı için 1099 yıl sonu raporlamasını desteklemek üzere ne gibi değişiklikler yapıldı?

#### <a name="update-to-all-1099-forms"></a>Tüm 1099 formlarına yönelik güncelleştirme

2022 vergi yılı için tüm 1099 formlarında aşağıdaki değişiklikler yapılmıştır:

- 2021'de yıl, 1099 formlarında sabitti. 2022'den itibaren yıl, rapor tarafından doldurulmaktadır.

#### <a name="1099-misc"></a>1099-ÇEŞİTLİ

2022 vergi yılı için Form 1099-ÇEŞİTLİ kapsamında aşağıdaki güncelleştirmeler yapılmıştır:

- Kutu 13: Yabancı Hesaplar Vergi Uyum Yasası (FATCA) dosyalama gereksinimini gösterir.
- Kutu 14: Artık aşırı yüklü tazminat ödemelerini raporlamak için kullanılır.
- Kutu 15: Artık niteliksiz ertelenmiş tazminat (NQDC) planları kapsamındaki ödemeyi raporlamak için kullanılır.
- Kutu 16: Artık devlette tutulan vergileri raporlamak için kullanılır.
- Kutu 17: Artık mükellefin eyalet numarasını raporlamak için kullanılır.
- Kutu 18: Artık eyalet gelirini raporlamak için kullanılır.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Borç hesapları: 1099: Yıl boyunca 1099 bilgilerini takip etmeyen bir satıcının 1099 kutusunu ve değerlerini nasıl değiştirebilirim?

Daha önce ödenen fatura hareketlerini incelemek ve 1099 verilerini, **Satıcı** sayfasının **1099 Vergisi** sekmesindeki ayarlara göre doğru şekilde yeniden atamak için **1099'u Güncelleştir** işlevini kullanın. **1099'u Güncelleştir** işlevini kullanmak için **Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin, bir satıcı seçin ve ardından Eylem Bölmesi'nde **Satıcı** sekmesine giderek **1099'u Güncelleştir**'i seçin.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>1099'u Güncelleştir işlevini tüm satıcılarım için aynı anda çalıştırabilir miyim?

**Birden çok satıcı için 1099 bilgilerini güncelleştir** sayfasını, satıcı kaydındaki 1099 kutusunu ve 1099 kutusundaki bilgileri kullanarak hareketleri güncelleştirmek için kullanabilirsiniz. Bu sayfayı açmak için **Borç hesapları \> Periyodik görev \> 1099 Vergisi**'ne gidin. Sayfaya erişmek için **Birden çok satıcı için 1099 kutusunu ve hareketlerini güncelleştir** güvenlik ayrıcalığına atanmış olmanız gerekir.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Borç hesapları: 1099: 1099'u Güncelleştir aracında "Mevcut 1099 tutarlarını yeniden hesapla" ve "Tümünü güncelleştir"

**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, **Tümünü güncelleştir** onay kutusuyla birlikte kullanıldığında 1099 tutarını ödenen toplam değerlere sıfırlar.

[![1099 Vergisi hareketleri: Güncelleştirme yordamını çalıştırmadan önce.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

**Mevcut 1099 tutarlarını yeniden hesapla** onay kutusu, yalnızca faturada kısmi 1099 değerleri olduğunda veya fatura 1099 Vergisi formunda değiştirildiğinde devreye girer. Örneğin, 1000,00 ABD doları değerinde bir faturanız olduğunu ancak kullanıcının faturaya 500,00 ABD doları değerinde bir 1099 tutarı girdiğini varsayalım.

[![1099 Vergisi hareketleri: Tümünü güncelleştir ve Mevcut 1099 tutarlarını yeniden hesapla seçeneklerini işaretleme.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Bu fatura ödendiğinde, ödenen 1099 tutarı 500,00 ABD doları olacaktır. Yeniden hesaplama yordamını gerçekleştirirseniz, 1099 tutarı ödenen toplam tutar olan 1000,00 ABD doları olarak değiştirilir.

[![1099 Vergisi hareketleri: 1099 yordamını çalıştırdıktan sonra.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Borç hesapları: 1099: 1099 hareketlerini el ile oluştur

Bir kuruluşun faturayla ilişkili olmayan 1099 hareketlerini el ile oluşturması gerekebilir. **Borç hesapları \> Periyodik görevler \> 1099 vergisi \> 1099 için satıcı kapatma**'ya giderek 1099 hareketlerini el ile ekleyebilirsiniz. **El ile 1099 hareketleri** düğmesini seçin.

El ile oluşturulan 1099 hareketleri, **1099'u Güncelleştir** işlevindeki **Tümünü güncelleştir** veya **Mevcut 1099 tutarlarını yeniden hesapla** işlemiyle güncelleştirilmez.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Borç hesapları: 1099: Dynamics 365 Finance, 1096 formunu destekler mi?

Dynamics 365 Finance, 1096 Yıllık Özeti'ni ve ABD Bilgi Beyannamelerinin İletimi formunu yazdırmaz.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Borç hesapları: 1099: Kamu sektörü için 1099 raporlamasını destekleyen yeni özellikler var mı?

Kamu sektörüne yönelik **1099 bilgilerini ana hesaba göre güncelleştir** adlı yeni bir özellik eklenmiştir. Özelliği, **Özellik yönetimi** çalışma alanından etkinleştirebilirsiniz. Bu özellik, satıcının 1099 değerlerini satıcı kaydındaki varsayılan hesap yerine, muhasebe dağıtımındaki ana hesaba göre ilişkilendirmenize olanak tanır.

Daha fazla bilgi için bkz. [1099 raporlamasına ilişkin satıcıları ayarlama](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
