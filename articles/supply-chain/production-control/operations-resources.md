---
title: Operations kaynakları
description: Operasyon kaynakları, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir. Bunlar farklı türlerde, farklı yeteneklere sahip olabilir.
author: sorenva
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifecycleManagementWorkspace, WrkCtrCapability, WrkCtrResourceGroup, WrkCtrResourceAbilityMap, OpResCapacityPlanningWorkspace, WrkCtrCapResGraph, WrkCtrResourceRequirementPart, WrkCtrCapResGraphDialog, WrkCtrResourceCopy, WrkCtrCapResStatistic
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 205906e8c7495df9a60585d0a79d6cbb0a73a49c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439110"
---
# <a name="operations-resources"></a>Operations kaynakları

[!include [banner](../includes/banner.md)]

Operasyon kaynakları, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir. Bunlar farklı türlerde, farklı yeteneklere sahip olabilir. 

<a name="operations-resources"></a>Operations kaynakları
--------------------

Operasyon kaynakları; bir proje veya üretim işleminde faaliyet gösteren makineler, araçlar, çalışanlar, tesisler, fiziksel alanlar veya satıcılardır. Bunlar farklı türlerde, farklı yeteneklere sahip olabilir.

-   **Satıcı** – Proje faaliyetleri veya üretim operasyonları gerçekleştiren harici bir kaynak. Bir örnek olarak alt yüklenici verilebilir. Satıcı kaynaklarını bir satıcı hesabına bağlayarak, ürün reçetesi (BOM) satırlarına veya üretim satırlarına dayalı alt yüklenici satınalmaları oluşturabilirsiniz.
-   **İnsan kaynakları** – Bir faaliyeti tek başına ya da bir araç veya makine operatörü rolüyle gerçekleştiren bir proje veya üretim çalışanı. İnsan kaynakları işlevini kullanıyorsanız, insan kaynaklarını bir çalışana bağlayabilirsiniz. Ardından, planlama altyapısı ilgili çalışan için tanımlanan yetkinliklere dayalı kaynaklar tahsis edebilirsiniz.
-   **Makine** – Üretimde gerekli olan bir makine veya diğer üretim ekipmanları.
-   **Araç** – Bir proje veya üretimde faaliyet gerçekleştirmek için genelde başka bir kaynakla birlikte kullanılan bir araç veya cihaz.
-   **Konum** – Bir faaliyeti gerçekleştirmek için gereken belirli bir büyüklükteki fiziksel bir konum. Örnek olarak bir montaj alanı verilebilir.
-   **Tesis** – Bir faaliyeti gerçekleştirmek için gereken bir bina veya sabit bir yapı.

## <a name="calendars"></a>Takvimler
Operasyon kaynağına bir takvim atanabilir ve bu kaynağın kapasitesini (saat cinsinden) tanımlar. Operasyon kaynağının çalışma süreleri operasyon kaynağının bir parçası olduğu kaynak grubuna atanmış takvime göre belirlenir. Atanan takvim için bir yürürlük tarihi ve bitiş tarihi ayarlayabilirsiniz. Daha sonra bir operasyon kaynağı için birden fazla takvim atayabilirsiniz. Ancak, atanan takvimlerin tarihleri çakışamaz ve operasyon kaynağı bir defada yalnızca tek takvime atanabilir. **Not:** Bir kaynak grubu için artık etkin bir çalışma takvimi yoksa (örneğin, atanan son takvim veya atanmış tek takvimin süresi dolmuşsa), üretim planlaması ve operasyon planlama çizelgeleme için kaynak grubuna atanmış olan operasyon kaynaklarına erişemezsiniz. Hem bir kaynak grubu hem de o kaynak grubuna atanmış olan tüm operasyon kaynakları için çalışma saatlerini belirtmek üzere kaynak grubuna bir takvim atayabilirsiniz. Kaynak grubunun kapasitesi o kaynak grubuna atanmış her bir operasyon kaynağının kapasitelerinin toplamı şeklinde hesaplanır. Bir kaynak grubuna atanmış takvimi zaman içinde değişebilir.

## <a name="resource-capabilities"></a>Kaynak yetenekleri
Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Bir veya daha fazla yeteneği bir operasyon kaynağına atayabilirsiniz. Zamanlama altyapısı, kaynakları ayırmak için her bir etkinliğin kaynak gereksinimlerini, kullanılabilecek operasyon kaynaklarının yetenekleriyle eşleştirir. Yetenekler tüm operasyon kaynağı türlerine atanabilir (**Araç**, **Satıcı**, **Makine**, **İnsan kaynakları**, **Konum** veya **Tesis**) Yetenekleri sınırlı bir süre için operasyon kaynaklarına atamak için yetenek atamasında bir başlangıç tarihi ve bitiş tarihi tanımlayın. Daha fazla bilgi için, [Kaynak yetenekleri](resource-capabilities.md) bölümüne bakın.

## <a name="resource-groups"></a>Kaynak grupları
Bir kaynak grubu, operasyon planlama çizelgeleme yöntemini kullandığınızda kaynakları planlamak istediğiniz ayrıntı düzeyini temsil eden bir dizi operasyon kaynağıdır. Bu nedenle, kaynak grupları genellikle üretim atölyesinde sarı satırlarla sınırı çizilen fiziki iş hücreleri düzenine karşılık gelir. Kaynak grubu, gruba atanan operasyon kaynaklarının tesis, üretim birimi ve ambar koşullarını tanımlar. Bir kaynak grubuna bir operasyon kaynağı atadığınızda, kaynak, kaynak grubunun bulunduğu tesiste zamanlanabilir. Bir kaynak grubuna oluşturduğunuz operasyon kaynaklarını atamak zorunda değilsinizdir. Ancak, çalışma gerçekleştirmek için zamanlanabilmesi için operasyon kaynaklarının bir kaynak grubuna atanması gerekir. Bir operasyon kaynağı sınırlı bir süre için bir kaynak grubuna atanabilir. Tesisler arasında kaynağı paylaştırabilmek için operasyon kaynağını birden çok kaynak grubuna da atayabilirsiniz. Ancak, yürürlük tarihleri ve bitiş tarihleri çakışamaz. Diğer bir deyişle, operasyon kaynaklarını aynı anda iki kaynak grubuna atayamazsınız. Kaynak grubu atamalarındaki değişiklikler yalnızca yeni kaynak tahsisatları için geçerlidir. İşler, işlemler için kapasite rezervasyonları ve önceden zamanlanmış proje saati tahminleri etkilenmez. **Not:** **Satıcı** türünün operasyon kaynaklarını bir kaynak grubuna atadığınızda, bu kaynak grubuna atanmış olan tüm operasyon kaynakları **Satıcı** türünde olmalı ve aynı satıcı hesabına bağlanmalıdır.

## <a name="production-units"></a>Üretim birimleri
Üretim birimi, kaynak gruplarının koleksiyonu olan bir yönetim birimidir. Üretim birimi birden çok kaynak grup içerebilir, ancak bir kaynak grubu yalnızca bir üretim birimine atanabilir. Üretim birimi, üretim kaynaklarının fiziksel düzenini yansıtır ve hareketler ile hareketlerin işlenme şekli üzerinde hiçbir etkisi yoktur. Bir üretim birimini bir tesisle ilişkilendirmeniz gerekir. Üretim birimine malzeme çekme ambarı ve depolama ambarı da atayabilirsiniz. Üretimle ilgili verileri konsolide etmek ve filtrelemek için üretim birimi kullanabilirsiniz. Örneğin, atölye yöneticisi belirli bir üretim birimine yönelik bekleyen iş yüküne ve kullanılabilir kapasiteye ilişkin bir genel bakış görebilir. Kaynak grubuna atanan üretim birimini değiştirebilirsiniz. Ayrıca üretim birimini silmek de mümkündür. Ancak üretim biriminde yapılan değişiklikler, yalnızca master planlama çalıştırıldıktan sonra oluşturulan yeni siparişiler için etkin olur. Üretim birimi değişikliğinin var olan siparişlere uygulanmasını istiyorsanız, bu değişikliği el ile yapmanız gerekir.

## <a name="resource-scheduling"></a>Kaynak zamanlama
Bir proje ve üretim zamanlandığında operasyon kaynakları faaliyetlere atanır. Kullanılabilir iki planlama yöntemi vardır: Operasyon planlama çizelgeleme ve iş planlama çizelgeleme. Operasyon planlama çizelgelemeyi kullandığınızda, operasyon için belirtilen kaynak gereksinimleriyle uyumlu operasyon kaynaklarını içeren kaynak grubundaki her operasyon veya proje faaliyeti zamanlanır. Operayon için belirli bir operasyon kaynağı gerekiyorsa, planlama gruptaki yalnızca belirli bir operasyon kaynağında kapasite rezerve eder. İş planlama çizelgeleme, operasyon planlama çizelgelemeden daha ayrıntılı bir biçimdir. Her operasyonun tek tek görevlerinin veya işlerinin dökümünü verir. Bu işler daha sonra bunları gerçekleştirecek operasyon kaynaklarına atanır. İş planlama çizelgeleme, kaynak gruplarındaki kapasiteyi üretim rotasında veya proje faaliyetlerinde tanımlanan işlem sürelerini temel alarak rezerve eder. Sınırlı kapasite ile çalışıyorsanız, planlama, faaliyetin tamamlanması için gereken operasyon kaynaklarının kullanılabilirliğine bağlıdır. Operasyon planlama çizelgeleme için, kaynak grubunun kapasitesi o grubun parçası olan operasyon kaynaklarının kullanılabilir kapasitenin toplamıdır. Operasyon kaynakları için zaten mevcut olan kapasite rezervasyonları, kullanılamayan kapasite olarak kabul edilir. Üretim için yeterli kullanılabilir kapasite yoksa, üretim emirleri gecikebilir ve hatta durdurulabilir. **Kaynaklar** sayfasında, kapasite rezervasyonlarının nasıl yapılacağını denetleyen çeşitli özellikler tanımlayabilirsiniz:

-   **Kapasite** – Kapasite ölçü birimi olarak operasyon kaynağının saatlik kapasitesini belirtin.
-   **Toplu kapasite** – Operasyon kaynağının çalışma başına işleyebileceği maksimum parça sayısını belirtin.
-   **Verimlilik yüzdesi** – Operasyon kaynağından beklediğiniz verimliliği belirtin. Verimlilik yüzdesi, operasyon kaynağının iş çıkarma yeteneğini ayarlar ve kaynağa ayrılan zamanı etkiler. Operasyon kaynağını kullanan operasyonların sağlama süreleri de buna göre ayarlanır. Hesaplama için kullanılan formül şudur: Planlama zamanı = Zaman × 100 ÷ Verimlilik yüzdesi. *Zaman* hem çalıştırma süresini, hem de kurulum süresini içerir.
-   **Operasyon planlama çizelgeleme yüzdesi** – Operasyon planlamasında kullanmak istediğiniz operasyon kaynağı kapasitesinin maksimum yüzdesini belirtin. İş planlaması yapılırken kapasitede esneklik sağlaması için bu değeri yüzde 100'den az olacak şekilde ayarlamalısınız.
-   **Sınırlı kapasite** – Operasyon kaynağı, mevcut kullanılabilir kapasiteye göre planlanacaksa ve mevcut kapasite rezervasyonları değerlendirilecekse bu seçeneği **Evet** yapın. Bu seçenek **Hayır** yapılırsa, operasyon kaynağının sonsuz kapasiteye sahip olduğu varsayılır ve dolayısıyla kaynak kapasitesinin üzerinde rezerve edilebilir.
-   **Sınırlı kaynak** – Operasyon kaynağının gerekli çalışma zamanı planlama özellikleriyle ilgili kullanılabilir fiili kapasiteye dayalı olarak zamanlanmasını istiyorsanız bu seçeneği **Evet** olarak ayarlayın.
-   **Özel** – Operasyon kaynağının geçerli üretim tamamlanana kadar başka bir iş veya operasyon için kullanılabilir olmasını istemiyorsanız, bu seçeneği **Evet** olarak ayarlayın. Bu durumda,operasyon kaynağı kaynakların çalışma zamanında boşluklar olsa bile kullanılamaz.
-   **Darboğazdaki kaynak** – Operasyon kaynağını darboğazdaki kaynak olarak tanımlayın. **Master planlar** sayfasında **Sınırlı kapasite** ve **Darboğaz çizelgelemesi** seçenekleri belirlendiğinde, darboğazdaki kaynak sınırlı kapasite kullanılarak zamanlanır.

Örneğin, üretimde bir operasyon gerçekleştirmek için aynı anda birden çok operasyon kaynağını zamanlamak için birincil ve ikincil operasyonları kullanarak çeşitli kaynaklara yönelik gereksinimleri belirtmeniz gerekir. Ardından, farklı kapasiteye sahip birden çok operasyon kaynağı da rezerve edebilirsiniz. Birincil operasyon için planlanan operasyon kaynağı faaliyet süresini belirler.

## <a name="lean-work-cells"></a>Yalın iş hücreleri
Bir kaynak grubunun yalın iş hücresi olduğunu belirtebilirsiniz. Kaynak grubu, bir üretim akışının parçası olabilir. Bir kaynak grubunu yalın bir iş hücresi olarak belirtilmesi, kaynak grubunun ve atanan operasyon kaynaklarının bir üretim emri veya proje saat tahmini operasyonlarına tahsis edilmesini önler. Yalın bir iş hücresi olarak işleyen her bir kaynak grubu için aşağıdaki bilgileri belirtmeniz gerekir:

-   **Takvim** – Standart bir iş gününün özelliğine sahip olması gereken iş hücresinin çalışma takvimi.
-   **Giriş ambarı ve konum** – Bir faaliyet için malzeme çekmek için kullanılan varsayılan konum.
-   **Çıkış ambarı ve konum** – İş hücresinin tüm çıkışlarının konduğu varsayılan konum.
-   **Çalışma zamanı maliyet kategorisi** – Maliyetlendirmede doğrudan işgücü izleniyorsa bu kategorinin iş hücresi için tanımlanması gerekir.

Kaynak grubu yalın bir iş hücresinde kullanıldığında, iş hücresinin kapasitesi doğrudan kaynak grubunda belirtilir. Bu nedenle, kaynak grubuna operasyon kaynaklarını atamanız gerekmez. Yalnızca iş hücresi bir alt yüklenici tarafından yönetildiğinde **Satıcı** türünün operasyon kaynakları iş hücresine atanmalıdır. İş hücresi olarak işaretlenmiş bir kaynak grubuna operasyon kaynağı atarsanız, iş hücresinin kapasitesi etkilenmez.

## <a name="costing-resources"></a>Maliyetlendirme kaynakları
Rota operasyonu veya bir proje saat tahmini gibi bir faaliyet tanımladığınızda, belirli operasyon kaynakları veya kaynak grubu için gereksinimleri belirtebilirsiniz. Ancak, belirli bir türdeki operasyon kaynağı gereksinimini veya belirli bir yeteneğe ya da uzmanlığa sahip operasyon kaynağını belirtebilirsiniz. Bu nedenle, faaliyet zamanlanana ve kapasite rezerve edilene kadar fiili kaynak ataması yapılmaz. Bu nedenle, bir rota operasyonunda tahmin ve ürün reçetesi hesaplamasının belirli bir operasyon kaynağına dayalı olduğunu belirtebilirsiniz. Bu operasyon kaynağı, maliyetlendirme kaynağı olarak adlandırılır. Ayrıca, maliyet kategorilerini ve operasyon sürelerini maliyetlendirme kaynağından ilgili faaliyete aktarabilirsiniz. Operasyon planlandığında, tahmin ve ürün reçetesi hesaplaması fiili olarak zamanlanmış operasyon kaynağı kullanılarak yapılır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]