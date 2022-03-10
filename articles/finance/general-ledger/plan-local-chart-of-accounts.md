---
title: Yerel hesap planınızı planlama
description: Bu konu, kuruluşunuza ait yasal/yerel gereksinimlerle ilgili gereksinimleriniz olduğunda hesap planını planlamanıza yardımcı olacak bilgiler sağlar.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798308"
---
# <a name="plan-your-local-chart-of-accounts"></a>Yerel hesap planınızı planlama

[!include [banner](../includes/banner.md)]

Bu konu, organizasyonunuz, iş amaçlı belirli yerelleştirmeleri için gereksinimleri karşılaması gereken yasal varlıklar içeriyorsa, hesap planını planlamanıza yardımcı olacak bilgiler sağlar. Bu konu, hesap grafiklerini açıklamak için aşağıdaki terimleri kullanır:

- **Global** – Organizasyonun global olarak kullandığı hesap planı. Çoğu durumda bu hesap planını birleştirmezsiniz.
- **Yerel** – Belirli bir ülke veya bölgedeki yasal varlıkların kullandığı hesap planı.
- **Paylaşılan** – Birden fazla yasal varlığın kullanabileceği bir hesap planı. Hem global hesap planı hem de hesapların yerel grafikleri paylaşılabilir.

Birden çok hesap grafiği oluşturabilir ve paylaşabilirsiniz. Paylaşılan hesap planı birden fazla yasal varlık tarafından kullanılabilir, ancak her yasal varlığa yalnızca bir hesap planı atanabilir. Tüzel kişilik tarafından kullanılan hesap planı **Genel muhasebe** sayfasında tanımlanır.

Hesap planını tasarlarken, birçok kuruluş genel bir hesap planı için hedeflenir. Paylaşılan hesap planı özelliği, global hesap planı oluşturulmasına olanak tanır. Tek bir hesap planı oluşturmanın ve kullanmanın yararları vardır. Örneğin, idare ve denetim, bakım ve raporlama daha kolaydır.

Çoğu kuruluşlar genel bir hesap planı tercih eder ve bu en kolay türdür. Bununla birlikte, bazı yasal varlıkların aşağıdaki nedenlerden dolayı yerel bir hesap planı ihtiyacı olur:

- Yerel yasal gereksinimler
- Yerel muhasebe standartları gereksinimleri
- Sektör gereksinimleri
- Şirkete özgü raporlama ve analiz gereksinimleri

Organizasyonunuz, yasal bir varlığın yerel bir hesap planı kullanmasını gerektiriyorsa, bunu uygulamak için iki seçenek vardır:

- Genel hesap planını atayın ve yerel gereksinimleri karşılamak için diğer araçları tanımlayın.
- Yasal varlığa yerel bir hesap planı atayın ve genel hesap planıyla ilgili ilişkileri tanımlayın.

Organizasyon yapısı ve raporlama yapısı, kullanılan seçeneği belirler.

[![Kuruluş yapısının genel mi yoksa yerel hesap planı mı kullanılacağını belirleyen diyagram](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Global hesap planı yasal varlığa atanmışsa, yerel raporlama gereksinimleri toplantı için aşağıdaki seçenekler kullanılabilir:

- Yerel konsolidasyon gerçekleştirin.
- Yerel hesap planını izlemek için bir mali boyut kullanın.
- Genel hesap planında yerel ana hesaplar oluşturun.
- Yerel hesap planıyla harici eşleme yapın.

Yerel hesap planı yasal varlığa atanmışsa, global raporlama gereksinimlerini karşılamanın şu andaki tek seçeneği, global konsolidasyondur.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Yasal bir varlığa atanan genel hesap planı

Global hesap planını yasal bir varlığa atamanız gerekiyorsa, daha önce açıklandığı gibi, sistemi konfigüre etmek için dört seçenek kullanılabilir. Dört seçeneğin tümü için, tek bir hesap planı yapılandırılır ve **Genel muhasebe** sayfasındaki her bir tüzel kişiliği bağlıdır. Her seçenek, yerelleştirme gereksinimlerini karşılamak için farklı bir yaklaşım kullanır. Aşağıdaki bölümlerde, sistemi yerelleştirme gereksinimleri için konfigüre eden üst düzey adımların ana hatları verilmiştir. Ayrıca, her seçeneğin avantajları ve dezavantajları da açıklanır.

### <a name="do-local-consolidation"></a>Yerel konsolidasyon gerçekleştirin

Yerel konsolidasyon, yerel hesap gereksinimleri ve bu amaçla tasarlanmış sistem işlevselliğinin yararı için önerilen yaklaşımdır.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Yerel bir hesap planı için konsolidasyon kurulumu

1. Gerekli tüm ana firmaları içeren tek bir global hesap planı oluşturun.
2. Her yasal varlıkta, genel hesap planını **Genel muhasebe** sayfasına atayın.
3. Gerekli olan her yerelleştirme için bir konsolidasyon yasal varlığı oluşturun.
4. Şu adımlardan birini izleyin:

    - Yalnızca bir yerelleştirme gerekiyorsa, **Ana hesap** sayfasında konsolidasyon hesabını konfigüre edin veya **Konsolidasyon gruplarını** ve **Ek konsolidasyon hesapları** sayfalarını kullanın.
    - Birden fazla yerelleştirme gerekiyorsa veya hem hesap numarası hem de hesap adı çeviri gerektiriyorsa, yerelleştirme gruplarını temsil etmek için **Konsolidasyon gruplarını** ve **Ek konsolidasyon hesaplarını** kullanın.

5. Global hesap planını kullanan kaynak tüzel kişiliğinden, yerel hesap planını kullanan konsolidasyon şirketine değeri dönüştürmek için konsolidasyon işlemini çalıştırın.

#### <a name="advantages"></a>Avantajlar

- Bu yaklaşım, kuruluş içinde çalışmak için tutarlı bir yol sağlar.
- Yerel pozisyonun bir çevirisi yapılır.
- Bu yaklaşım, hem ana hesap kimliğinin hem de her bir ana hesabın adının çevirisini destekler.
- Çoklu yerelleştirmeleri destekler.

#### <a name="disadvantages"></a>Dezavantajlar

- Ek bir konsolidasyon şirketi oluşturulur.
- Ek bir konsolidasyon süreci tamamlanır.
- Bu yaklaşım, yalnızca konsolidasyon işlemi tamamlandıktan sonra yerelleştirilmiş grafik üzerinde rapor verebilir.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Yerel hesap planını izlemek için bir mali boyut kullanın

Bu yaklaşım, mali boyut değerlerinin yerelleştirme için gereken yerel ana firmaları temsil ettiği bir finansal boyut kullanır. Yalnızca tek bir yerelleştirme gerekliyse bu işlem iyi çalışır. Ancak, daha fazla yerelleştirmeler ve mali boyut eklediğinizde daha az kullanılabilir hale gelir.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Yerel hesap planını için mali boyut kurulumu

1. Gerekli tüm ana firmaları içeren tek bir global hesap planı oluşturun.
2. Her yasal varlıkta, genel hesap planını **Genel muhasebe** sayfasına atayın.
3. Yerel hesap planını temsil eden bir mali boyut oluşturun.
4. Yerel hesap planlarındaki ana hesapları temsil eden mali boyut değerleri oluşturun.
5. "Yerel hesap planı" mali boyutunu içermesi için hesap yapısını güncelleştirin.
6. "Yerel hesap planı" mali boyutunun her zaman bir değere sahip olduğundan ve boş bir değere izin vermediğinden emin olun. Türetilmiş boyutları veya sabit boyutları kullanmayı düşünebilirsiniz.
7. "Yerel hesap planı" mali boyutunun, ilk seçilen mali boyut olduğu bir mali boyut kümesi oluşturun. Mali boyut kümesi, mizan oluşturulurken kullanılabilir.

#### <a name="advantages"></a>Avantajlar

- Hesapların hem global hem yerel grafiklerinin ana hesapları hareket düzeyinde mevcuttur. Ana hesap geneldir ve mali boyut değeri yereldir.
- Bu yaklaşım hem global finans konumu hem de yerel finans konumu için gerçek zamanlı raporlama ve görünümler sağlar.

#### <a name="disadvantages"></a>Dezavantajlar

- Genel muhasebe parametrelerinde, **Özet hesap alanında kullanılan değerler** **Hesap dağıtımları** olarak ayarlanmışsa, gider/kıymet/gelir için ana hesabı temsil eden mali boyutlar alacak hesapları ve borç hesapları özet hesabı için hatalı olarak kullanılacaktır. Doğru mali boyut değerlerinin kullanıldığından emin olmak için, bunun yerine alanı bir kaynak belge olarak ayarlamanız tavsiye ediyoruz.
- Hesapların birçok yerel grafiği gerekliyse ve tümü için bir mali boyut kullanılıyorsa, kullanılan finansal boyut değerleri listesi uzun ve bunlarla çalışılması zor olabilir.
- Hesapların birçok yerel grafiği gerekliyse ve her birini temsil eden ayrı bir mali boyut kullanılıyorsa, mali boyutlar ve finansal boyut kümeleri eklendiğinde sistemin kullanılabilirliği ve performansı etkilenebilir.
- Tüm bu etmenler sistem performansını etkileyebileceğinden, gereksinim duyduğunuz finansal boyut sayısını, her birindeki değerlerin sayısını ve finansal boyut kümelerinin sayısını dikkatle düşünmeniz önerilir.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Genel hesap planında yerel ana hesaplar oluşturun

*Kopya düzenleyicisinin sorduğu sorular hakkında:* Bu yaklaşımda, global hesap planında bulunan yerel ana hesaplar, genel hesap planındaki yerel hesap planındaki ana firmaları içerir.

*Özgün sürüm:* Genel CoA'daki yerel ana hesaplar yaklaşımı, yerel CoA ana hesaplarının genel CoA'ya dahil edilmesidir.

*Bunu mu söylesin:* Bu yaklaşımda, yerel hesap planındaki yerel ana hesaplar, genel hesap planında yer alır.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Genel hesap planında yerel ana hesaplar kurulumu

1. Global hesap planı ve yerel hesap planı için ana hesaplar içeren tek bir hesap planı oluşturun.
2. Her yasal varlıkta, hesap planını **Genel muhasebe** sayfasına atayın.
3. Aynı amacı temsil eden ana firmaları toplamak için hesap planında toplam hesapları oluşturun.
4. Yerel hesabın tasarlanmamış olduğu diğer tüzel kişilikler arasında işlem yapılmasını önlemek için her yerel hesapta yasal varlık geçersiz kılmaları oluşturun.
5. Yerelleştirme hukuk varlıklarından hareketleri önlemek için her genel hesapta yasal varlık geçersiz kılmaları oluşturun.

#### <a name="advantages"></a>Avantajlar

- Global finans ve yerel finans konumlarından her ikisinin de gerçek zamanlı görünümü belirli raporlarda ve sistemdeki belirli görünümlerde (örneğin, bilanço finansal raporları) kullanılabilir. Ayrıca toplam hesapta **Dönem** düğmesini kullanarak da erişilebilir olabilir.
- Genel muhasebe hesabında ek bir segmentiniz yok.

#### <a name="disadvantages"></a>Dezavantajlar

- Toplam hesap kullanımı ve görünürlüğü sınırlıdır. Örneğin, tüm **Mizan** listesi sayfasında toplam hesaplar görünmez.
- Bakım için ek çaba gereklidir.
- Mali raporların oluşturulması ek el ile çaba gerektirir.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Yerel hesap planıyla harici eşleme yapın

Genel bir hesap planını benimsemenin sistemin dışındaki eşleme ve yerelleştirmeleri yönettiğiniz varsayılır. Bu yaklaşımda, Microsoft Dynamics 365 Finance'te tek bir global hesap planı oluşturmanız ve gereksinimleri sistem dışında işlemeniz yeterlidir.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Yerel hesap planıyla harici eşleme kurulumu

1. Gerekli tüm ana firmaları içeren tek bir global hesap planı oluşturun.
2. Her yasal varlıkta, genel hesap planını **Genel muhasebe** sayfasına atayın.
3. Finans dışında Yerel hesap planıyla eşleme yapın.

#### <a name="advantages"></a>Avantajlar

- Bu yaklaşım, kuruluş içinde çalışmak için birleşik yollar sağlar.

#### <a name="disadvantages"></a>Dezavantajlar

- Sistemde kullanılabilir yerel raporlama yok.
- Mali raporlar oluşturulurken bu yaklaşım hataya açıktır.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Yasal bir varlığa atanan yerel hesap planı

Organizasyonunuz, yasal varlıklarda genel hesap planını kullanmayacağına karar verirse, benzersiz her yerel hesap planı için ayrı bir hesap planı oluşturulur. Böylece, her yasal varlık **Genel muhasebe** sayfasındaki ilgili hesap planına bağlanır.

### <a name="do-global-consolidation"></a>Genel konsolidasyon gerçekleştirin

Bu yaklaşımda, bir konsolidasyon şirketi her kaynak yerel şirketten alınan bakiyeleri konsolidasyon şirketindeki birleştirilmiş global hesap planıyla birleştirmek ve bu şirketin bakiyelerini birleştirebilmek için kullanılır. Bu yaklaşım, her bir yerel hesap planının, konsolidasyon şirketindeki global hesap planında eşlenmesini sürdürmenize gerek duyar.

#### <a name="set-up-global-consolidation"></a>Genel konsolidasyon kurulumu

1. Farklı bir yerel hesap planına sahip olan her yasal varlık için ayrı bir hesap planı oluşturun. Tüzel kişilikler aynı yerel hesap planına sahipse, yalnızca bir yerel hesap planı gereklidir ve bu paylaşılabilir.
2. Her yasal varlıkta, uygun hesap planını **Genel muhasebe** sayfasına atayın.
3. İsteğe bağlı: Global bir hesap planı farklı olan her bir konsolidasyon şirketinin genel hesap planı için bir hesap planı oluşturun.
4. Gerekli olan her konsolidasyon düzeyi için bir konsolidasyon yasal varlığı oluşturun ve ilgili hesap planını **Genel muhasebe** sayfasında atayın.
5. Şu adımlardan birini izleyin:

    - Yalnızca tek bir konsolidasyon gerekiyorsa, **Ana hesap** sayfasında konsolidasyon hesabını konfigüre edin.
    - Birden fazla konsolidasyon gerekiyorsa veya hem hesap numarası hem de hesap adı çeviri gerektiriyorsa, genel hesap planı gereksinimlerini temsil etmek için **Konsolidasyon gruplarını** ve **Ek konsolidasyon hesaplarını** kullanın.

6. Yerel yasal varlıklardaki bakiyeleri konsolide yasal varlığa transfer etmek için konsolidasyon işlemini çalıştırın. Bu konsolide yasal varlığı adım 5'te tanımladığınız konsolidasyon hesaplarını kullanır.

#### <a name="advantages"></a>Avantajlar

- Yerel muhasebe standartları biçimi özgün olarak uygulanır.
- Bu yaklaşım, yerel finans ekibinin çalışmasını daha kolay bir şekilde sağlar.

#### <a name="disadvantages"></a>Dezavantajlar

- Global pozisyonun gerçek zamanlı görünümü yok.
- Konsolidasyon işlemi daha sık çalışabilir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Hesap planınızı planlama](plan-chart-of-accounts.md)
- [Genel muhasebe defterlerini yapılandırma](configure-ledger.md)
- [Mali boyutlar ve deftere nakletme](Default-dimensions.md#balancing-dimension)
- [Mali boyut kümeleri](financial-dimension-sets.md)
- [Konsolidasyon ve elemeye genel bakış](../budgeting/consolidation-elimination-overview.md)
- [Konsolidasyon hesabı grupları ve ek konsolidasyon hesapları](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
