---
title: Master planlama kurulum sihirbazı (video içerir)
description: Bu konuda, master planlamayı ayarlamak için master planlama kurulum sihirbazının nasıl çalıştırılacağı açıklanmaktadır.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: a5914f63de654acd076048240c6e37d5b67f4ffa
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470219"
---
# <a name="master-planning-setup-wizard"></a>Master planlama kurulum sihirbazı

[!include [banner](../includes/banner.md)]

Bu konu, **Master planlama kurulum sihirbazı** için bir kılavuz sağlar. Bu, parametre önerilerinin nasıl hesaplanacağını açıklar ve aynı zamanda farklı şirketlerin iş gereksinimlerine göre master planlamanın nasıl ayarladığını gösteren örnekler de sağlar.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

[Dynamics 365 Supply Chain Management'ta master planlama kurulum sihirbazı](https://youtu.be/c-e6n-8rZb4) videosu (yukarıda gösterilen), YouTube'da bulunan [Finance and Operations oynatma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) bulunmaktadır.


## <a name="specific-requirements-of-your-company"></a>Şirketinizin özel gereksinimleri

Sihirbazın ilk sayfası, şirketinizin belirli gereksinimlerini sorar. Bu sorulara verdiğiniz cevaplar kesin olmak zorunda değildir, ancak madde sayısı ve planlanan emirlere tüzel kişilik için kabaca bir tahmin sağlamak mümkün olmalıdır. Yanıtlarınız, yalnızca seçtiğiniz master plana değil, tüzel kişilik için geçerli olan parametreleri yapılandırmak için kullanılır. Aşağıdaki bölümlerde, hesaplanan parametreler ve kullanılan formüller açıklanmaktadır.

### <a name="number-of-threads"></a>İş parçacığı sayısı

- **Bu maddelerin herhangi birini üretiyorsanız** İş parçacığı sayısı = Planlanan sipariş sayısı ÷ 1.000
- **Bu maddelerin herhangi birini üretmiyorsanız** İş parçacığı sayısı = Madde sayısı ÷ 1.000

Hesaplanan iş parçacıklarının sayısı mevcut iplik sayısının yüzde 75'ini aşıyorsa her müşteri için mevcut iş parçacıklarının sayılarının yüzde 75'i ile sınırlandırılır. (Her müşteri için kullanılabilir iş parçacığı sayısı belirlenir.)

Daha fazla bilgi için bkz: [İş parçacığı sayısı](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Paket boyutu

Ürün demeti boyutu **1** olarak ayarlanacaktır. Bu değer genellikle en iyi değerdir, çünkü master planlamanın performansını artırmaya yardımcı olur.

Daha fazla bilgi için bkz [: Yardımcı görev ürün demetinde görevler sayısı](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Toplu iş grubu kesinleştirme

- **Öğelerden herhangi birini üretiyorsanız:** Kesinleşen ürün demeti boyutu bu iki değerin büyük olması için ayarlanır: **10** ve ürün demeti hesaplama
- **Öğelerden herhangi birini üretmiyorsanız:** Kesinleşen ürün demeti boyutu bu iki değerin büyük olması için ayarlanır: **50** ve ürün demeti hesaplama

Ürün demeti hesaplaması = (Ğlanlanan siparişlerin sayısı × (Kesinleşen zaman dilimi ÷ Kapsam zaman dilimi) ÷ İş parçacığı sayısı) ÷ 10

### <a name="cache-size"></a>Önbellek boyutu

Önbellek boyutu **Maksimum** olarak ayarlanacaktır. Bu değer genellikle en iyi değerdir, çünkü master planlamanın performansını artırmaya yardımcı olur.

Daha fazla bilgi için bkz: [İş ürün demetindeki işlere zaman tahsis etme](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Üretim kurulumu

Öğe üretiyorsanız sihirbazda daha sonra bir **Üretim kurulumu** sayfası görünecektir.

## <a name="scope-of-the-current-plan"></a>Geçerli planın kapsamı

Sihirbazın **Geçerli plan kapsamı** sayfasının üzerinde, gelecekteki çeşitli gereksinimlerin master planlamada ne kadar uzun zaman içinde değerlendirileceği ve hesaplanacağı ile ilgili sorulara yanıt bulabilirsiniz. Her soru, bir özelliği kullanmak isteyip istemediğinizi ve bunu nasıl yapılandırmak istediğinizi sorar.

Örneğin, tahmin planı özelliği için, sihirbaz "Öngörülen talebi yerine getirmek üzere planlanan siparişlerin önerilmesi için master planlamada bir tahmin planı kullanmak ister misiniz?" diye sorar.

Aşağıdaki seçenekler bulunur:

- **Hayır** -Master planlama bir tahmini yerine getirmek için planlanan siparişler önermez. **Master planlar** sayfasının **Zaman dilimleri** sekmesinde (**Master planlama \> Kurulum \> Planlar \> Master planlar**), sihirbaz **Tahmin planı (zaman dilimi)** seçeneğini **Evet** olarak ve günleri **0** (sıfır) olarak ayarlayacak. Bu kurulum, kapsam grubunda belirtilen zaman dilimini geçersiz kılacaktır. Gün sayısı **0** (sıfır) olarak ayarladığından, özellik kullanılmaz.
- **Evet, bu master planda tanımlandığı gibi**, – Master planlamanın, öngörülen talebi yerine getirmek için planlı siparişler önereceği gün sayısını girebileceğiniz bir alan kullanılabilir. Sihirbaz **Tahmin planı (zaman dilimi)** seçeneğini **Evet** ve **Master planlar** sayfasının **Zaman dilimleri** sekmesinde **Tahmin planı** alanını girilen gün sayısını gün sayısı olarak ayarlayacak. Bu kurulum, kapsam grubunda ayarlanan değerleri geçersiz kılacaktır.
- **Evet, kapsamda tanımlandığı gibi** – Sihirbaz **Tahmin planı (zaman dilimi)** seçeneğini **Hayır** olarak ayarlayacak. Kapsam grubunda belirtilen zaman planı, tahmin için ne kadar zaman planlayacağınızı belirlemek için kullanılacaktır.

Bu sayfada kalan sorular ve cevapları aynı şemayı takip ediyor:

- **Hayır** – **Tahmin planı (zaman dilimi)** seçeneği **Evet** olarak ve gün sayısı **0** (sıfır) olarak ayarlanır.
- **Evet, master planı tanımlandığı gibi** – Sihirbaz **Tahmin planı (zaman dilimi)** seçeneğini **Evet** olarak ayarlayacak. Girdiğiniz gün sayısı kullanılacaktır ve kapsam gruplarında ayarlanan değerleri geçersiz kılacaktır.
- **Evet, grupta tanımlandığı gibi** – Sihirbaz **Tahmin planı (zaman dilimi)** seçeneğini **Hayır** olarak ayarlayacak.

Daha fazla bilgi için bkz. [İş planlama](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Planlama seçenekleri

**Zamanlama seçenekleri** sayfası, yalnızca sihirbasın ilk sayfasındaki "Planlanmış öğelerden herhangi birini üretiyor musunuz?" sorusunu **Evet** olarak yanıtladığınız takdirde görünür.

Bu sayfadaki ilk soruya cevabınız (Bireysel işlere bölünmüş işlemleri zamanlamanız gerekiyor mu?) **Master planlar** sayfasındaki **Genel** sekmesindeki zamanlama yöntemini belirler.

- **Evet** -İş planlaması kullanılacaktır.
- **Hayır** – İşlem planlaması kullanılacaktır.

Daha fazla bilgi için bkz. [İşlem planlaması](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) ve [İş planlaması](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Talep ve tedarik güncelleştirmeleri

**Talep ve tedarik güncelleştirmeleri** sayfasındaki sorular kesinleştirme, eylem mesajları ve gecikmelerle ilgilidir.

Master planlama kurulumu, önceki bölümde açıklanan aynı şemaya göre yanıtlarınızı temel alarak güncelleştirilir:

- **Hayır** – **Master planlar** sayfasındaki **Zaman dilimi** seçeneği **Evet** olarak ayarlanır ve gğn sayısı **0** (sıfır) olarak ayarlanır.
- **Evet, master planı tanımlandığı gibi** – Sihirbaz **Zaman dilimi** seçeneğini **Evet** olarak ayarlayacak. Girdiğiniz gün sayısı kullanılacaktır ve kapsam gruplarında ayarlanan değerleri geçersiz kılacaktır.
- **Evet, grupta tanımlandığı gibi** – Sihirbaz **Zaman dilimi** seçeneğini **Hayır** olarak ayarlayacak.

Hesaplanan gecikmeler için, sihirbazdaki sorulara yanıtlarınız,**Master planlar** sayfasının **Hesaplanan gecikmeler** sekmesindeki ilgili parametreleri güncelleyecektir.

## <a name="summary-of-your-changes"></a>Yaptığınız değişikliklerin özeti

Sihirbazın son sayfası, yanıtlarınızı temel alarak önerilen değişiklikleri gösterir. Her iki değer, kurulumunuzu (**Geçerli kurulum**) ve sihirbazın önerdiği değeri (**Yeni yapılandırma**) gösterir.

Yeni yapılandırmada parametreleri de değiştirebilirsiniz. Parametreler, tüzel kişiliğinize ve yalnızca seçtiğiniz master plana uygulanan parametreler için geçerli olan parametrelere ayrılır. Sihirbaz kullanılarak değiştirilebilir tüm kurulum parametrelerini görüntülemek için sayfanın altındaki **Tüm parametreleri göster**'i seçin. Daha sonra parametreleri değiştirebilirsiniz.

Son olarak, **Bitir**'i seçtiğiniz zaman yeni yapılandırma uygulanır. **İptal**'i seçerseniz değişikliklerden hiçbiri uygulanmaz.

## <a name="examples"></a>Örnekler

Bu bölümde, kurulumun her işletmenin ihtiyaçlarına göre nasıl değişeceğini göstermek için iki kurgusal şirketin kurulumu açıklanmaktadır.

### <a name="example-1-contoso-manufacturer"></a>Örnek 1: Contoso Manufacturer

Contoso Manufacturer, hoparlör üreten bir üretim şirketidir. Çeşitli tedarikçilerden son hoparlörler için kullanılan çeşitli hammadde ve bileşenleri satın alır. Tedarik ve imalatının bazı özellikleri şunlardır:

- Şirketin ürettiği son öğeler bir ürün reçetesi (BOM) yapısına sahiptir.
- Tüm son öğeler ve bileşenler master planlama tarafından planlanmıştır. El ile planlama yapılmamıştır.
- Her son maddenin üretimi için bir işlem rotası tanımlanır.
- Üretim tesisi son öğeleri üretir. Bileşenleri işlemek için kullanılan freze ve delme makineleri için tanımlanmış bir sayı vardır. Çeşitli bileşenlerin bu makineler tarafından işlenmesi gerekir.
- Birçok tedarikçi vardır. Maddelerin ortalama sağlama süresi bir haftadır. Aynı tedarikçiden gelen bir grup öğenin sağlama süresi yedi hafta olacaktır.

Sihirbazda, Contoso Manufacturer için aşağıdaki değerler girilir:

- **Kapsam:**

    - **Soru:** "Planlama ufkunun gün sayısını belirtmek istiyor musunuz?"
    - **Cevap:** "Evet, kapsam grubunda tanımlandığı gibi."

    Maddelerin sağlama süresi çok farklı olduğundan, Contoso gelecekte aynı dönem için tüm öğeleri planlamak zorunda değildir. Maddelerin kapsam grupları oluşturulur. Benzer bir sağlama süresi olan öğeler aynı kapsam grubuna atanır. Her bir kapsama grub için planlama ufku (yani, kapsam zaman dilimi) yaklaşık teslim süresi artı bir hafta marjıdır. Daha sonra master planlama, maddelerin teslim süresini temel alarak önceden planlanmış olduğundan emin olur.

    Bu nedenle, bu örnek için iki kapsam grubu oluşturulacaktır. Bir kapsam grubunun iki haftalık bir kapsam zaman dilimi, diğerinin sekiz haftalık bir kapsam zaman dilimi olacaktır.

    Cevap olarak **Evet, bu master planda tanımlandığı gibi** seçiliyse girilen gün sayısı tüm öğelerin en uzun teslim süresini aşmalıdır. Ancak, birçok öğe şimdiye kadar önceden planlanmamış olması nedeniyle, birçok planlanan sipariş hesaplanır ama asla kullanılmaz. Bu nedenle, master planlamanın çalışma süresi artar.

- **Planlama:**

    - **Soru:** "Bireysel işlere bölünmüş işlemleri zamanlamanız gerekiyor mu?"
    - **Cevap:** "Evet."

    Contoso Manufacturing, atölye üzerinde gerçekleştirilecek bireysel işleri planlamak ve zamanlamak zorundadır. Bu nedenle, iş planlaması kullanacak.

- **Kapasite:**

    - **Soru:** "Kaynakların kapasitesini kullanarak zamanlama yapmak istiyor musunuz?"
    - **Cevap:** "Evet, bu master planda tanımlandığı gibi." **10 gün** girilir.

    Freze ve delme makineleri sayısı sınırlıdır. Üretim planlaması bu sınırlama dikkate almalı ve kaynakların kapasitesine göre zamanında işlerini düzenlemelidir. Diğer bir deyişle, zamanlanan işler kaynakların sınırlamalarına bağlı olarak yeniden planlanacaktır. Planlama, tanımlanan döneme ek olarak sağlama süresini kullanır. (Planlı üretim emri çakışabilir.) Maddelerin üretim sağlama süresi yedi gün olduğundan, master planlama kaynaklarının kapasitesi 10 gün olarak değerlendirilir.

- **Sıralama:**

    - **Soru:** "Planlanan siparişleri ürünün sıra değerlerini kullanarak sıralamak istiyor musunuz?"
    - **Cevap:** "Evet, kapsam grubunda tanımlandığı gibi."

    Her son maddenin üretimi için bir rota tanımlanır. Bu nedenle, master planlama, belirlenen rotalara göre siparişleri zamanında planlayacaktır.

- **Açılım:**

    - **Soru:** "Bir ürün reçetesindeki tüm öğelerin siparişini planlamak istiyor musunuz (tüm ana ve alt öğeler için plan)?"
    - **Cevap:** "Evet, kapsam grubunda tanımlandığı gibi."

    Üretim için kullanılan tüm öğeler planlanmalıdır. Öğelerin çok farklı sağlama süreleri olduğundan, master planlama kapsam grupları kullandığında daha iyi performans gösterecektir. Yine, bir haftalık bir marj girilebilir ve kapsam alanıyla aynı anda açılım yapılabilir.

### <a name="example-2-contoso-retailer"></a>Örnek 2: Contoso Retailer

Contoso Retailer, moda endüstrisinde bir dağıtım şirketidir. Satınalma siparişlerinin ne zaman yerleştirileceğini, tahmin edilen satışlara göre hesaplamak için master planlama kullanır. Bazı özellikleri şunlardır:

- Contoso Retailer, satışları tahmin etmek için bir talep tahmini kullanır. Satın alma siparişleri tahmin uyarınca planlanır.
- Mağazaları, stok yenileme için talepleri kullanır.
- Ana ambardan her mağazaya teslim süresi, tüm öğeler için yaklaşık iki haftadır.

Sihirbazda, Contoso Retailer için aşağıdaki değerler girilir:

- **Talep tahmini:**

    - **Soru:** "Master planlamada planlanan siparişler tahmin edilen talebi yerine getirmek için önerilecek bir tahmin planı kullanmak istiyor musunuz?"
    - **Cevap:** "Evet, bu master planda tanımlandığı gibi."

    Contoso satış tahmin etmek için bir talep tahmini dahil etti. Bu nedenle, master planlama tahmini yerine getirmek için planlanan siparişleri tavsiye etmelidir.

- **Kesinleştirme:**

    - **Soru:** "Master planlamanın, planlanan siparişleri otomatik olarak sipariş belgelerine, örneğin üretim veya satınalma siparişlerine göre düzenlemesini mi istiyorsunuz?"
    - **Cevap:** "Evet, bu master planda tanımlandığı gibi." **1 gün** girilir.

    Contoso Retailer, doğrudan planlanan satınalma siparişlerinden satınalma siparişleri oluşturduğundan, planlanan satınalma siparişleri otomatik olarak kesinleştiriliyorsa yararlıdır. Şirket her gün master planlama yaptığından, bir günün kesinleştirici bir zaman dilimi ertesi gün için gereken tüm siparişleri otomatik olarak yerine getirecektir.

- **Onaylanan talepler:**

    - **Soru:** "Perakende mağazalarının yenilenmesi için onaylı talepten talep dahil etmek istiyor musunuz?"
    - **Cevap:** "Evet, bu master planda tanımlandığı gibi." **1 gün** girilir.

    Contoso, bu mağazaları yenilemek için planlanan satınalma siparişleri oluşturmak üzere mağazalardan onaylanan talepleri kullanır. Master planlama her gün çalıştırıldığından, son günden gelen talepler planlamaya dahil edilecektir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]