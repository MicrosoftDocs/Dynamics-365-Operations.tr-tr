---
title: "Yükseltme kesin bitiş testi"
description: "Bu konu, AX 2012'yi kapattıktan ve Dynamics 365 for Finance and Operations, Enterprise Edition'ı açmadan önce gerçekleşen görevlerin nasıl test edileceğini açıklar."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: tr-tr
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Yükseltme kesin bitiş testi

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

*Kesin bitiş* yeni bir sistemi kullanıma sunmadan önceki son işlem için kullanılan bir terimdir. Bu kesin bitiş işlemi, AX 2012 kapatıldıktan sonra ve Dynamics 365 for Finance and Operations, Enterprise Edition açılmadan önce gerçekleştirilen görevlerden oluşur. Yükseltme kesin bitiş testinin amacı, kullanıma sunma amacıyla gerçekleştirilen gerçek kesin bitişe dahil olan herkesin sorunsuz bir deneyim yaşamasını sağlamak amacıyla kesin bitiş işlemi için uygulama yapmaktır.

Bir kesin bitiş sırasında iki ana iş akışı vardır:

- **Teknik iş akışı** – Bu iş akışı veri yükseltmeyi yürütme işlemini içerir. İşletmeniz izin verilen kesinti süresi miktarı üzerinde bir sınır uygular. Bu kesinti sırasında, ne AX 2012 ne de Finance and Operations kullanılabilir olmaz. Bu iş akışının, işletmenin kesinti süresi sınırını karşılamak amacıyla veri yükseltme yordamına ayar yapması gerekebilir.
- **İşlevsel iş akışı** – Bu iş akışı, veri yükseltme tamamlandıktan sonra gerçekleştirilen yapılandırma görevlerini içerir. Bu görevlerin tümü belgelenmeli ve sayısal ölçümleri yapılmalıdır, hem işlevsel iş akışının hem de teknik iş akışının iş kesinti süresi sınırı içinde olması gerektiğinden kaynak atanmalıdır.

Aşağıdaki örnekte kullanıma sunmak gerçekleştirilen tüm kesin bitiş işlemi üretim ortamında gerçekleşeceği şekilde gösterilmektedir.

![Kesin bitiş işlemi](./media/cutover_1.png)

Kesin bitiş işlemi korumalı alan ortamında yapılan bir temel veri yükseltme işleminden aşağıdaki şekillerde farklıdır:

- AX 2012 veritabanı kopyalanmaz ancak yalnızca yedeği alınır ve ardından orijinal veritabanı değiştirilir. Bu yaklaşım daha hızlıdır ve geri alma gerekirse yedekleme geri alma olanağı sağlar.
- Finance and Operations için üretim ortamına erişim sınırlı olduğundan, daha önce Uygulama Nesne Sunucusunun (AOS) korumalı alan kurulumunda gerçekleştirilen görevler şimdi Microsoft DSE ekibi tarafından gerçekleştirilir. Bu görevler arasında bacpac dosyasını indirip içe aktarma ve MajorversionDataUpgrade.zip paketini çalıştırma bulunur.
- Aşağıdaki görevleri ekledik:

    - Duman testi gerçekleştirin.
    - Uygulama kurulum görevlerini tamamlayın. Bu adım, kullanılan işlevselliğe bağlı olarak büyük olabilir. Bu adım sırasında, işlev ekibi yeni uygulama işlevlerini yükseltilen sistemde kullanılmaya hazır olacak şekilde yapılandırır.
    - Kullanıların geri gelmelerini sağlayın. Kullanıcılarınızı yükseltmenin tamamlandığı ve sistemi yeniden kullanabilecekleri konusunda bilgilendirin.

## <a name="technical-workstream"></a>Teknik iş akışı

Teknik iş akışı çeşitli teknik ekip üyeleri içerir: veritabanı yöneticisi (DBA), AX 2012 sistem yöneticisi, sunucu yöneticileri ve AX 2012 ve Finance and Operations hakkında bilgi sahibi olan geliştiriciler. Bu konu hangi rollerin hangi görevleri içerdiğini açıklar.

Kesin bitiş testi sırasında teknik ekip iş kesinti süresi sınırına uygun olmasını sağlamak amacıyla veri yükseltme işleminin performansına ve güvenilirliğine odaklanır. Bu işleme çok sayıda donanım ve yazılım öğesi dahil olur. Bu öğelerin bazıları kurum içinde, bazıları ise Microsoft buluttadır. Ayrıca, birçok özel uygulama kodu ve standart kod da bu işlem kapsamındadır. Bu testin sonucu, ortamınız için kesin bitişin güvenilir olduğu olmalıdır.

### <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 AOS kurulumlarını kapatma

Bu görev, AX 2012 sistem yöneticisini ve sunucu yöneticilerini kapsar.

Aşağıdaki alanların değerlendirilmesi gerekir:

- **Kesin bitiş sırasında çalıştırılan toplu işler** – Zaten başlatılmış olan uzun süre çalışan bir toplu iş sistemin durdurulmasını engeller. AOS kurulumlarını istediğiniz zaman durdurabilmek için önceden planlama yapın. Toplu işleri siz AX 2012'yi kapatmadan bir süre önce tamamlanacak şekilde planlayabilirsiniz.
- **Tümleştirilen sistemler** – AX 2012 ortamıyla tümleşik olan başka sistemleriniz olabilir. Bu sistemleri AX 2012'yi devre dışı bırakma planınızda göz önünde bulundurmanız gerekir. Örneğin, tümleştirilen sistemleri AX 2012'yi devre dışı bırakmadan bir süre önce kapatarak kalan yürütülen işlemlerin tamamlanmasını sağlayabilirsiniz. Tümleştirilen sistemlerin gereksinimleri büyük ölçüde işletmeden işletmeye farklılık gösterir. Bu nedenle, uzman ekibiniz bu senaryoyu bağımsız şekilde planlamalıdır.

### <a name="create-a-backup-of-the-ax-2012-database"></a>AX 2012 veritabanının yedeğini oluşturma

Bu görev DBA'ya yöneliktir. Geri alma gerekirse yedek kullanılacaktır. Ayrıca bir dönem saklanacak bir referans noktası olarak kullanılır ve kesin bitiş sırasındaki sistem durumunu gösterir.

Aşağıdaki alanların değerlendirilmesi gerekir:

- Yedekleme işlemi için somut zamanlamalar belirleyin.
- Mümkün olan en hızlı yedeklemeyi garanti etmek için kullanılan yedekleme seçeneklerini (örneğin, sıkıştırma veya sıkıştırmama) ayarlayın.

### <a name="export-the-database-to-bacpac"></a>Veritabanını bacpac'e aktarma

Bu görev DBA'ya yöneliktir. Bu görevin sonucunda yeni sistem için Microsoft Azure'a yüklenecek dışa aktarma dosyası elde edilir.

Aşağıdaki alanların değerlendirilmesi gerekir:

- Yedekleme işlemi için somut zamanlamalar belirleyin.
- En hızlı deneyimi sağlamanıza yardımcı olması için dışa aktarma işlemini en iyi duruma getirin. En iyi duruma getirme aşağıdaki görevleri gerektirebilir:

    - Dışa aktarma sırasında CPU, disk giriş çıkış ve bellek gibi sistem kaynaklarını ölçün.
    - Kaynaklarda darboğaz sorunları varsa, bunları azaltmak için bir plan oluşturun. Genellikle, daha fazla gerekli kaynak atayarak bu sorunları azaltabilirsiniz.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>Azure depolamaya bacpac dosyasını yükleme

Bu görev DBA veya sunucu yöneticileriyle ilgilidir. Bu görev sırasında bacpac dosyası Azure'a taşınır.

Aşağıdaki alanların değerlendirilmesi gerekir:

- Yükleme için kullanılacak makineyi seçin ve Azure Depolama gezgini aracının yapılandırıldığından ve kullanıma hazır olduğundan emin olun.
- Yükleme işlemi için birkaç kez ölçüm yaparak somut zamanlamalar elde edin. Yükleme süreleri İnternet bağlantı hızınıza ve Azure veri merkezinin bulunduğunuz konuma göre coğrafi konumuna bağlı olarak farklılık gösterir.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>bacpac fosyasını Azure SQL veritabanından indirme ve veritabanına aktarma

Bu görev kullanıma sunma zamanında oluştuğunda, Microsoft DSE ekibi tarafından gerçekleştirilir. Bununla birlikte, kesin bitiş testi sırasında DBA'nın görev kapsamındadır. Bu görevin sonucunda yeni sistem için Azure'a yüklenecek dışa aktarma dosyası elde edilir.

Aşağıdaki alanların değerlendirilmesi gerekir:

- İçe aktarma işlemi için somut zamanlamalar belirleyin.
- En hızlı deneyimi sağlamanıza yardımcı olması için dışa aktarma işlemini en iyi duruma getirin. En iyi duruma getirme aşağıdaki görevleri gerektirebilir:

    - Dışa aktarma sırasında sistem kaynaklarını ölçün. Burada bazı örnekler verilmiştir:

        - **AOS makinede:** CPU, disk G/Ç ve bellek
        - **Azure SQL Veritabanı kurulumunda:** SQL veritabanı işlem hacmi (DTU). AOS makinesindeki Microsoft SQL Server Management Studio'dan ilk Azure SQL DTU'yu sys.dm_resource_stats sistem görünümüne bakarak izleyebilirsiniz.

    - Kaynaklarda darboğaz sorunları varsa, bunları azaltmak için bir plan oluşturun. Genellikle, daha fazla gerekli kaynak atayarak bu sorunları azaltabilirsiniz. Bu makine Microsoft tarafından barındırıldığından, bir darboğaz olduğunu belirlerseniz kaynakları artırması için Microsoft'a bir istek göndermeniz gerekir.

### <a name="run-the-majorversiondataupgradezip-package"></a>MajorVersiondataUpgrade.zip paketini çalıştırma

Bu görev kullanıma sunma zamanında oluştuğunda, Microsoft DSE ekibi tarafından gerçekleştirilir. Bununla birlikte, kesin bitiş testi sırasında, geliştiricilerin görev kapsamındadır. Bu görev sırasında, eski veritabanı yapısı yeni sistemin yapısına dönüştürülür.

Veritabanı eşitleme işlemi bu görevin bir parçası olarak çalıştırılır. Veritabanı eşitleme bir tablodaki kümelenmiş dizininin değiştirimesi gibi bazı durumlarda önemli bir süre alabilir çünkü bu işlem SQL'de maliyetli bir işlemdir.

Öncelikle geliştirme ortamında analiz ve hata ayıklama işlemi yapmanızı öneririz. Korumalı alan ortamında, analiz ve hata ayıklama seçenekleri daha kısıtlıdır. Hedef kesin bitiş testini yaparken, giderilmesi gereken az sorun veya hiç sorun olmamasıdır.

Aşağıdaki alanların değerlendirilmesi gerekir:

- İçe aktarma işlemi için somut zamanlamalar belirleyin.
- Hızlı bir deneyim sağlamanıza yardımcı olması için işlemi en iyi duruma getirin. En iyi duruma getirme aşağıdaki görevleri gerektirebilir:

    - ReleaseUpdateScriptsExecution tablosu aracılığıyla ayrı yükseltme komut dosyalarının performansını izleyin.
    - Performansı en iyi duruma getirmek için komut dosyalarını düzenleyin. Bu görev, veri kümeniz için bir komut dosyasının X++ kodunu en iyi duruma getirmenizi gerektirebilir.
    - Microsoft Dynamics Lifecycle Services (LCS) izleme özelliğini veya Management Studio'daki sys.dm_resources_stats sistem görünümünü kullanarak Azure SQL DTU'yu izleyin. Kaynaklar en üst düzeye getirilmişse, Microsoft DSE ekibinde daha yüksek bir veritabanı düzeyi isteyebilirsiniz.

### <a name="roll-back-to-ax-2012"></a>AX 2012'ye geri dönme

Bu görevin amacı AX 2012 devre dışı bırakılırken yapılan yedeklemeyi kullanarak veritabanını geri yüklemek ve AX 2012'yi yeniden etkinleştirmektir. Tümleştirilmiş sistemlerin durumu da geri yüklenmelidir. Ancak, tümleştirilmiş sistemler kurumdan kuruma farklılık gösterdiğinden, bu senaryoyu kendi özel koşullarınıza göre bağımsız olarak planlamanız gerekir. Geri dönme olasılığınız düşük olmasına karşın, bunun gerekli olması durumu için test edilmiş bir işleminiz olması çok önemlidir.

## <a name="functional-workstream"></a>İşlevsel iş akışı

Veri yükseltmeden sonra yeni ortamda birçok yapılandırma görevi gerekli olacaktır. Bu iş akışının amacı tüm yapılandırma görevlerini belgelemek ve sayılarını belirlemek ve her göreve bu görevlerin kesinti süresi döneminde teknik iş akışıyla birlikte yapılabilmesini sağlamak için bir kaynak atamaktır.

Genellikle, işlevsel görevler belirli sistem parametreleri değerlerinin veya diğer yapılandırma verilerinin değiştirilmesini içerir. Bu görevler, kesin bitiş testinden ayrı bir işlem olan tam işlevsel test geçişiyle tanımlanır. Bu türde bir görev tanımlandığında, bu görevin işlevsel kaynakla ve geliştiricinizle birlikte gözden geçirilmesi gerekir.

Daha büyük değişiklikler, veri yükseltme işlemi sırasında verilerin güncelleştirilmesi için yeni bir özel yükseltme komut dosyası yazılmasını gerektirebilir. Bununla birlikte, işlevsel kaynak veri yükseltme sonrasında yeni sistem üzerinde el ile daha küçük değişiklikleri çalıştırabilir.

Yeni veri yükseltme komut dosyaları olan daha büyük değişikliklerin test edilmesi gerekir. Bu nedenle, MajorVersionDataUpgrade.zip paketinin bir veya daha fazla ek yinelemesi çalıştırılmalıdır. Paketi yeniden çalıştırmanın maliyeti ile el ile veri girişi maliyetini karşılaştırarak değerlendirmeniz önemlidir.

El ile yapılacak her değişiklik için kesin bitiş planı belgesine bir görev eklenmelidir. Bu görev aşağıdaki ayrıntıları göstermelidir:

-   Görev nedir ve ne yapılmalıdır?
-   Kimin yapması gerekir?
-   Ne kadar sürer?

