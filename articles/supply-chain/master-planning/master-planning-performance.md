---
title: Master planlama performansını iyileştirme
description: Bu konu, ana planlama ve sorun giderme sorunlarının performansını artırmanıza yardımcı olabilecek çeşitli seçenekleri açıklamaktadır.
author: t-benebo
manager: AnnBe
ms.date: 05/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: f0d075bbcc8a6671054f227a13c75ca7fb1e954f
ms.sourcegitcommit: 432481001b986b54937d423516efd8f2af1511d6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/13/2019
ms.locfileid: "1631555"
---
# <a name="improve-master-planning-performance"></a>Master planlama performansını iyileştirme

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Bu konu, ana planlama ve sorun giderme sorunlarının performansını artırmanıza yardımcı olabilecek çeşitli seçenekleri açıklamaktadır. Parametreler ve ayarlar hakkında bilgiler ve önerilen yapılandırmalar ve eylemler hakkında bilgi içerir. Ayrıca, uzun süre çalışan master planlama işleriniz olduğunda dikkate almanız gereken tüm önemli parametrelerin özeti de bulunur.

Bu konu, sorun giderme yeteneğine sahip olan sistem yöneticileri veya BT kullanıcıları içindir. İşletme planlama gereksinimiyle ilgili parametreler hakkında bilgiler içerdiğinden, üretim veya tedarik planlayıcıları için de hazırlanmıştır. 

## <a name="parameters-that-are-related-to-master-planning-performance"></a>Master planlama performansı ile ilgili parametreler

Çeşitli parametreler, master planlamanın çalışma süresini etkiler ve dikkate alınmalıdır.

### <a name="number-of-threads"></a>İş parçacığı sayısı

**İş parçacığı sayısı** parametresi, belirli veri kümesinde daha iyi çalışmasına yardımcı olacak master planlama sürecini ayarlamanıza olanak sağlar. Master planlamayı çalıştırmak için kullanılacak iş parçacıklarının toplam sayısını belirtir. Master planlama çalıştırmasının paralelleşmesine neden olur ve bu paralelleşme çalışma süresinin azalmasına yardımcı olur. 

**Master planlamayı çalıştır** iletişim kutusunda**İş parçacığı sayısı çalıştır** parametresini ayarlayabilirsiniz. Bu iletişim kutusunu açmak için **Master planlama \> Master planlama \> Çalıştır \> Master planlama**'ya gidin ya da **Master planlama** çalışma alanında **Çalıştır**'ı seçin. Bu parametrenin en iyi değerini belirlemek için bir deneme ve hata işlemine güvenmelidir. Ancak bir başlangıç değeri hesaplamak için aşağıdaki formülleri kullanabilirsiniz:

- **Sektörünüz imalatsa** İş parçacığı sayısı = Planlanan sipariş sayısı ÷ 1,000
- **Aksi takdirde** : İş parçacığı sayısı = Madde sayısı ÷ 1.000

Master planlama sırasında kullanılan yardımcıların sayısı, toplu iş sunucusunda izin verilen iş parçacığı sayısı üst sınırından az veya bu değere eşit olmalıdır. Yardımcıların sayısı toplu iş sunucusundaki iş parçacığı sayısını aşarsa ek iş parçacıkları hiçbir işe yaramayacaktır.

> [!NOTE]
> **İş parçacığı sayısı** parametresi için **0** (sıfır) ayarı master planlama çalışma süresini artırır. Bu nedenle, her zaman 0' dan büyük bir değeri ayarlamanız önerilir.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Yardımcı görev ürün demetindeki görev sayısı

**Ürün demetindeki görevlerin sayısı** ayarlarını değiştirerek (ürün demeti) çalışma süresini azaltabilirsiniz. Bu ayar tek bir yardımcıyla birlikte planlanan madde sayısını kontrol eder.

**Master planı parametreleri** sayfasının  **Genel** sekmesindeki **Performans** bölümündeki **Ürün demetindeki görevlerin sayısı**'nı ayarlayabilirsiniz (**Master planlama \> Kurulum \> Master planlama parametreleri**). Bu parametre için en iyi değer verilerinize bağlıdır. Bu nedenle, **1**değeriyle başlamanız ve sonra kurulumun en iyi değerini belirlemek için bir deneme-hata süreci kullanmanızı öneririz.

Genel olarak, öğe sayısı çok büyükse (yüzbinlerce) görev sayısını artırmanız önerilir. Aksi durumda, görev sayısını azaltmanız gerekir. Aşağıdaki belirli sektörler için şu noktaları göz önünde bulundurun:

- Birçok bağımsız maddenin bulunduğu perakende ve dağıtım sektörlerinde, maddeler arasında bağımlılık olmadığı için birçok yardımcı kullanın. 
- Birçok ürün reçetesi (BOM) ve paylaşılan alt bileşenlerin bulunduğu üretim sektöründe, maddeler arasındaki bağımlılıklar bekleme sürelerine neden olabileceğinden, daha az sayıda yardımcı kullanın.

> [!TIP]
> Performans sorunlarınız varsa **Görev ürün demeti yardımcı sayısı**ayarındaki yardımcıların sayısını **1**'e azaltmanız önerilir. Daha sonra kurulumunuz için en iyi değeri bulmak üzere deneme ve hata sürecini başlatabilirsiniz. Genel olarak, performans sorunları, bir öğenin kalan öğelerden daha uzun sürdüğü zaman ortaya çıkar. Bu durumda, master planlama çalışmasında **Karşılama** durumunda olan iki sonraki görevin çalışması önemli ölçüde farklı olacaktır. Olağanüstü durumlarda, bu fark 30 dakika kadar olabilir. Görevlerin çalışmaya tamamlanması için gereken süreyi, her bir görevin süresine bakarak belirtebilirsiniz.

### <a name="use-of-cache"></a>Önbellek kullanımı

**Önbellek kullanımı** parametresi, belirli veri kümesinde daha iyi çalışmasına yardımcı olacak master planlama sürecini ayarlamanıza olanak sağlar. Örneğin, aşağıdaki sonuçları elde etmek için ayarlayabilirsiniz:

- Daha fazla önbelleğe alma işlemi yapıldıysa veri belleğinde daha fazla veri toplanır. Veriler daha sonra yeniden kullanılacaktır. Veri bellekte ise bazı veritabanı isteklerini kaydedebilirsiniz. Ancak, daha fazla önbelleğe alma işlemi yapıldıysa bellek gereksinimleri artar.
- Daha az önbelleğe alma işlemi yapıldıysa aynı verilerin veritabanından daha sık getirilmesi gerekebilir. Ek olarak, Uygulama Nesne Sunucusu (AOS) süreç boyunca küçük verileri bellekte depolar.

Hangi seçeneğin daha iyi olacağını tahmin etmek zordur, çünkü her durum yalnızca verilere değil, donanıma da bağlıdır. Örneğin, daha az sayıda önbelleğe alma veritabanı sunucusunda ek yüklemeye neden oluyorsa, veritabanı sunucunuz zaten aşırı yüklenmiş ise, büyük olasılıkla bu seçeneği kullanmak iyi bir fikir değildir.

**Master plan parametreleri** sayfasının **Genel** sekmesindeki **Performans** bölümündeki **Önbellek kullanımı**'nı ayarlayabilirsiniz (**Master planlama \> Kurulum \> Master planlama parametreleri**). Önbelleğe almanın verimliliği, müşteri verilerine bağlıdır. Örneğin, önbelleğe alınmış verilere hiçbir zaman ihtiyaç duyulmazsa zamanlama işleminin sonuna kadar veri depolarsanız ve yalnızca belleği boşa harcamış olursunuz. Bu durumda, daha az önbelleğe almayı yapılandırırsanız, AOS daha az bellek gerektirdiğinden ve diğer görevler için sunucu kaynakları serbest bırakıldığından performans artırılabilir.

> [!TIP]
> Genel olarak parametre, performans genişletme özelliği olarak düşünülebileceğinden, **Önbellek kullanımı**'nı **Maksimum** olarak ayarlayamanızı tavsiye ediyoruz. Parametreyi şirket içinde çalıştırırsanız ve sınırlı belleğiniz varsa parametreyi **Minimum** olarak ayarlamanızı tavsiye ediyoruz. (yaklaşık olarak 2 gigabayt\[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Kesinleşen ürün demetindeki siparişlerin sayısı

**Kesinleşen ürün demetindeki siparişlerin sayısı** parametresindeki sayı veya siparişler her bir iş parçacığı/toplu iş tarafından bir seferde işlenecek siparişlerin toplam sayısını belirtir. Otomatik kesinleştirme sürecinin paralelleşmesine neden olur.

**Master planı parametreleri** sayfasının  **Genel** sekmesindeki **Performans** bölümündeki **Kesinleşen ürün demetindeki siparişlerin sayısı**'nı ayarlayabilirsiniz (**Master planlama \> Ayarlama \> Master planlama parametreleri**). Otomatik kesinleştirme sürecinin paralelleştirmesi, birlikte işlenmesi gereken siparişlere dayanır. Bu nedenle, örneğin, bu parametre **50**olarak ayarlanırsa her iş parçacığı veya toplu görev, her seferinde 50 sipariş alır ve bunları birlikte işler. En iyi değeri bulmak için bir deneme ve hata işlemi kullanmanızı öneririz. Ancak bir başlangıç değeri hesaplamak için aşağıdaki formülü kullanabilirsiniz:

Paket başına sipariş sayısı = Talep öğelerinin sayısı ÷ İş parçacığı sayısı

> [!NOTE]
> **Kesinleşen ürün demetindeki siparişlerin sayısı** parametresi içindeki siparişlerin sayısını **0**'a (sıfır) ayarlarsanız otomatik kesinleşme sürecini herhangi bir paralel hale getirme işlemi gerçekleşmez. Tüm işlem tek bir toplu iş görevi üzerinde çalışacak ve toplu çalışma süresine sahip olacaktır. Bu nedenle, master planlamanın çalışma süresi artar. Bu nedenle, bu parametreyi **0**'dan (sıfır) büyük bir değere ayarlamanız önerilir.

### <a name="time-fences"></a>Zaman dilimleri

Zaman dilimleri, hesaplamaların ve diğer gereksinimlerin master planlama tarafından ne kadar ileride hesaplanacağını belirtir. Zaman dilimi ne kadar büyük olursa o kadar uzun bir süre için master planlama yapılır. Bu nedenle, zaman dilimlerini iş gereksinimlerinize göre ayarlayın. Zaman dilimleri hakkında daha fazla bilgi için bkz [Master planlamayı ayarlama](master-planning-setup.md).

### <a name="actions"></a>Eylemler

Zaman dilimleri arasında, **Eylem iletisi** parametresini de bulabilirsiniz. Eylem iletilerinin hesaplanması master planlama için daha uzun süre çalışma süresine neden olur. Eylem iletileri düzenli olarak analiz edilmez ve uygulanmazsa (günlük, haftalık, vb.), master planlama çalıştırması sırasında hesaplamayı kapatmayı düşünebilirsiniz. Hesaplamayı kapatmak için **Master planlar** sayfasından (**Master planlama \> Kurulum \> Planlar \> Master planlar**), **Eylem iletisi** zaman dilimini çalıştırdığınız master planınız için **0** (sıfır) olarak ayarlayın. Ayrıca, tüm kapsam grupları için **Êylem iletisi** ayarının kapatılmış olduğundan da emin olun.

### <a name="futures"></a>Vadeli işlemler

Vadeli işlemler hesaplanması master planlama için daha uzun süre çalışma süresine neden olur. BOM'ları planlamıyorsanız veya gecikmeler planlama sırasında tedarikten talebe sunulmak zorunda değilse master planlama sırasında vadeli işlem hesaplamalarını kapatmayı düşünün. Hesaplamaları kapatmak için çalıştırdığınız master planına ilişkin **Vadeli işlemler** zaman dilimini **0** (sıfır) olarak ayarlayın. Ayrıca, tüm kapsam grupları için **Vadeli işlemler** ayarının kapatılmış olduğundan da emin olun.

## <a name="one-heavy-routine-at-a-time"></a>Bir seferde tek bir yordam

Master planlama çizelgeleyebilirsiniz, aynı anda başka bir toplu iş planlanmayın. Özellikle, aynı anda stok kapanışı gibi diğer ağır yordamların planlanmamasına dikkat edin.

## <a name="review-the-session-log"></a>Kullanıcı oturumu günlüğünü inceleme

Sistem, master planlama sırasında çalışan görevlerle ilgili daha fazla bilgi toplayabilir. Sistemin bu bilgileri toplayabilmesi için **Master plan çalışması** iletişim kutusundaki **İşleme izleme saati**'ni açın. Toplanan bilgileri çalıştırmak tıkanmaları bulmanıza yardımcı olabilir. Örneğin **Yardımcı görev ürün demetindeki görev sayısı** parametresi **1** olarak ayarlandığında en uzun çalışma süresine sahip maddeyi tanımlayabilirsiniz. Ayrıca, **Karşılama** durumunda olan çeşitli iş parçacıklarının çalışma sürelerini ve her görevin süresini karşılaştırabilirsiniz.

Sisteminizin master planlama çalışmalarını gözden geçirmek için aşağıdaki adımlardan birini izleyin.

- **Master planlama** çalışma alanında, açılan alanda bir master plan seçin ve sonra **Master planlama** kutucuğunda **Geçmiş**'i seçin. Bir iş seçin, hızlı sekmede **Sorgulamalar**'ı seçin ve **İşleme görevi süresi**'ni seçin.
- **Master planlar** sayfasında, sol bölmeden bir plan seçin ve hızlı sekmede **Geçmiş**'i seçin. Bir iş seçin, hızlı sekmede **Sorgulamalar**'ı seçin ve **İşleme görevi süresi**'ni seçin.

Oturum günlüğünü gözden geçirdikten sonra aşağıdaki noktaları dikkate alın:

- **Güncelleştirme** uzun sürmez (genel olarak 30 dakikaya kadar sürer). Ancak, tek iş parçacıklı olur.
- **Kopya planı** uzun sürmez (yaklaşık bir dakika sürer).
- **Otomatik kesinleştirme** genellikle yaklaşık 30 dakika sürer. Ancak, siparişlerin sayısına ve maddelerin karmaşıklığına bağlı olarak birkaç saat sürebilir.
- **Otomatik kesinleştirme**, **Kapsam**'dan daha kısa sürer.
- **Kapsam**, geri kalanıyla karşılaştırıldığında en uzun sürendir.
- **Eylem** ve **Gelecek iletiler**, verilerin ve BOM'ların sayısına bağlı olarak uzun sürebilir.

## <a name="filtering-of-items"></a>Maddelere filtre uygulama

**Master planlama çalışması** iletişim kutusunda uygulanan filtreler, master planlamanın çalışmasının süresini etkiler. **Master planlama \> Master planlama \> Çalıştır \> Master planlama**'ya gidin ya da **Master planlama** çalışma alanında **Çalıştır**'ı seçin. Öğeleri çalıştırmadan hariç tutmak için öğenin yaşam döngüsü durumuna göre filtremenizi öneririz (madde numaralarına göre değil). Yaşam döngüsü durumuna filtre uyguladığınızda, güncelleştirme işlemi, madde numaralarına göre filtrelediğiniz zamana göre daha az zaman alır.

## <a name="performance-checklist-summary"></a>Performans yapılacaklar listesi özeti

- **İş parçacığı sayısı**'nı **0**'dan (sıfır) büyük bir değere ayarlayın.
- **Yardımcı görev ürün demetindeki görev sayısı**'nı **0**'dan (sıfır) büyük bir değere ayarlayın. (Bu konunun önceki bölümlerinde verilen formülleri kullanın.)
- **Önbellek kullanımı**, sisteminizin belleği azalmadıkça **Maksimum** olarak ayarlanır.
- **Kesinleşen ürün demetindeki siparişlerin sayısı**'nı **0**'dan (sıfır) büyük bir değere ayarlayın. (Bu konunun önceki bölümlerinde verilen formülü kullanın.)
- **Zaman dilimleri** – İş gereksinimlerinize göre ayarlayın.
- **Eylemler ve vadeli işlemler** – Eylemleri ve vadeli işlemleri kullanmıyorsanız devre dışı bırakın.
- **Bir seferde tek bir yordam** – Master planlamayı başka herhangi bir yordamla birlikte çalıştırmayın.
- **Kullanıcı oturumu günlüğünü inceleme.**
- **Maddelere filtre uygulama** – Yaşam döngüsü durumunu, maddeleri Master planlama çalıştırmasında hariç bırakmak için kullanın. (Madde numaralarını kullanmayın.)
