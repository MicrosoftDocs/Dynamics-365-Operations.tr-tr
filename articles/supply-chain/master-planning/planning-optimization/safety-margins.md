---
title: Emniyet marjları
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management güvenlik boşluklarının uygulamasında Planlamayı En İyi Duruma Getirme Eklentisi ile nasıl kullanılabileceği açıklanmaktadır.
author: ChristianRytt
ms.date: 09/14/2020
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
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9dc305f46dad6b372721805669529bbc9ac554e8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908305"
---
# <a name="safety-margins"></a>Emniyet marjları

[!include [banner](../../includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management güvenlik boşluklarının uygulamasında Planlamayı En İyi Duruma Getirme Eklentisi ile nasıl kullanılabileceği açıklanmaktadır.

## <a name="safety-margins-overview"></a>Emniyet marjlarına genel bakış

Emniyet marjlarının amacı, normal sağlama süresinin ötesinde bazı tampon zaman sağlayan bir kurulumu etkinleştirmeyi sağlamaktır. Örneğin, satıcıdan alındıktan sonra malzemenin paketinden çıkarılarak incelenmesi gerektiğinde, yalnızca satınalma sağlama süresine ek süre ekleyemezsiniz, çünkü bu yaklaşım tedarikçiye ek tampon süre verir. Bu örnekte, tedarikçinin daha erken teslim ettiğinden emin olmak için giriş marjı kullanılabilir. Bu yaklaşım, malların içeride işlenebilmesi için tampon zaman sağlar.

Üç tip emniyet marjı vardır:

- **Sipariş yenileme sınırı**: tedarik emrinin oluşturulması için tampon süre
- **Giriş marjı**: gelen tedariki işlemek için tampon süre
- **Çıkış marjı**: sevkiyatların işlenmesi için tampon süre

Aşağıdaki şekilde, bu emniyet marjlarının zamanla nasıl uygulanacağını gösterilir.

![Emniyet marjları](media/safety-margins-1.png)

Tüm marjlar gün olarak tanımlanır. Varsayılan değer olan *0* (sıfır) hiçbir marjın uygulanmadığını belirtir. Birden fazla marj ayarlarsanız, bunların tümü tedarik *emri tarihinden* talep *gereksinim tarihine* kadar olan toplam zamana eklenir. Örneğin, bir kurulum sağlama süresine sahip değildir ve üç marj türünün tümü bir güne ayarlanır. Bu durumda, tedarik emri tarihi ile talep gereksinim tarihi arasında üç gün olacaktır, bu nedenle sipariş tarihi 1 Temmuz ise, gereksinim tarihi 4 Temmuz olur.

### <a name="receipt-margin"></a>Giriş marjı

Giriş marjı büyük olasılıkla üç emniyet marjının en çok kullanılanıdır. *Teslimat tarihine* ve *gereksinim tarihinden* geriye doğru uygulanır. Başka bir deyişle, ürünler, gerek duyuldukları günden önceki belirtilen sayıda giriş marjı günü kadar önce alınması gerekir.

Aşağıdaki çizimde giriş marjları vurgulanır.

![Giriş marjı](media/safety-margins-2.png)

Giriş marjı genellikle, ambar kaydı veya sistemdeki genel sağlama süresinin bir parçası olarak hesaba katılmayan başka zaman alan süreçler için zaman sağlamak amacıyla tampon olarak kullanılır. Satınalmalar için, bir avantajı ise satınalma emrine ait *teslimat tarihinin* uygun şekilde ileriye doğru hareket ettirilebilmesidir. Bir emniyet marjı kullanmak yerine sağlama süresini artırdığınızda, satıcıdan son dakikada teslim etmesi istenecektir.

Giriş marjının, tedarikin *gereksinim tarihini* değiştirmediğini unutmayın. Bu nedenle, talep ve tedarik için gereksinim tarihleri karşılaştırıldığı zaman, giriş marjı doğrudan görünmez (örneğin, **Net gereksinimler** sayfasında). Örneğin giriş marjı 4 gün olarak belirlenir ve bir satınalma siparişi satırının ayın 15'inde alınması planlanırsa, master planlama ayarlanan giriş tarihini ayın 19'u olarak hesaplar.

Eldeki stok tedarik olarak kullanıldığında bir giriş marjının uygulanmadığını unutmayın. Eldeki tüm stokların, gerçekten ne zaman teslim alındığında bağımsız olarak hemen kullanılabilir olduğu varsayılır.

### <a name="reorder-margin"></a>Sipariş yenileme sınırı

> [!NOTE]
> **Çok yakında:** Bu özellik henüz Planlama Optimizasyonu için desteklenmiyor. Desteklenene kadar, **Madde sağlama süresine eklenen sipariş yenileme sınırı** için girilen tüm değerler *0* (sıfır) olarak kabul edilir.

Aşağıdaki çizimde sipariş yenileme sınırı vurgulanır.

![Sipariş yenileme sınırı](media/safety-margins-3.png)

Sipariş yenileme sınırı, master planlama sırasında planlanan tüm siparişler için malzeme sağlama zamanının önüne eklenir. Bu nedenle, bir tedarik emrinin oluşturulması için ek süre sağlar. Bu marj genellikle, tedarik emirlerinin oluşturulması sırasında gerekli olan onay işlemleri veya diğer iç işlemlere zaman sağlamak amacıyla tampon olarak kullanılır. Yeniden sipariş sınırı tedarik *emri tarihi* ile *başlangıç tarihi* arasına konur.

### <a name="issue-margin"></a>Çıkış marjı

> [!NOTE]
> **Çok yakında:** Bu özellik henüz Planlama Optimizasyonu için desteklenmiyor. Desteklenene kadar, **Gereksinim tarihinden kesilen çıkış marjı** için girilen tüm değerler *0* (sıfır) olarak kabul edilir.

Aşağıdaki çizimde çıkış marjı vurgulanır.

![Çıkış marjı](media/safety-margins-4.png)

Master planlama sırasında çıkış marjı talep gereksinim tarihinden düşülür. Gelen talep emirlerine cevap vermek ve sevk etmek için zaman kazanmanıza yardımcı olur. Bu marj, genellikle sevkiyat ve ilgili ambar çıkış işlemlerine zaman sağlamak amacıyla tampon olarak kullanılır.

Bir çıkış marjı uygulandığında, ilgili tedarik ve talep gereksinim tarihlerinin eşleşmediğini unutmayın. Bunun yerine, çıkış marjı tedarik *gereksinim tarihi* ve talep *gereksinim tarihi* arasına eklendiği için çıkış marjına göre farklılık gösterir.

## <a name="set-up-safety-margins"></a>Emniyet marjlarını ayarlama

### <a name="turn-on-safety-margins-in-feature-management"></a>Özellik yönetiminde Emniyet marjlarını açma

Bu özelliği Planlama Optimizasyonu ile kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** _Master planlama_
- **Özellik adı:** _Planlama Optimizasyonu_ için Marjlar

### <a name="define-safety-margins"></a>Emniyet marjlarını tanımlama

Emniyet marjlarının esnek bir ayarı vardır. Bunlar hem *karşılama grubunda*, hem de *master planda* ayarlanabilir. Marjların birbirlerinin üzerine eklendiğinin bilinmesi önemlidir. Örneğin, karşılama grubunda iki günlük giriş marjı ve master plandaki üç gün, beş günlük etkin giriş marjı oluşturacaktır.

Master planda marj ayarlama yeteneği, belirli bir plan için günlük planlamayı etkilemeden daha uzun bir sağlama süresi veya belirsizlik senaryosunu canlandırmak istediğinizde yararlı olabilir.

#### <a name="coverage-group-safety-margins"></a>Karşılama grubu emniyet marjları

Bir karşılama grubuna emniyet marjı uygulamak için, aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Karşılama grupları**'na gidin.
1. Liste bölmesinde, istediğiniz karşılama grubunu seçin.
1. **Diğer** hızlı sekmesinde, **Gün cinsinden emniyet marjları** bölümünde, gerekli emniyet marjlarını (gün cinsinden) ayarlamak için aşağıdaki alanları kullanın:

    - Gereksinim tarihine eklenen giriş marjı
    - Gereksinim tarihinden kesilen çıkış marjı
    - Madde sağlama süresine eklenen sipariş yenileme sınırı

#### <a name="master-plan-safety-margins"></a>Master plan emniyet marjları

Bir master plana emniyet marjı uygulamak için, aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesinde, istediğiniz master planı seçin.
1. **Gün cinsinden emniyet marjları** hızlı sekmesinde, gerekli emniyet marjlarını (gün cinsinden) ayarlamak için aşağıdaki alanları kullanın:

    - Gereksinim tarihine eklenen giriş marjı
    - Gereksinim tarihinden kesilen çıkış marjı
    - Madde sağlama süresine eklenen sipariş yenileme sınırı

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Hesaplamaların takvim günlerini mi yoksa iş günlerini mi temel alacağını tanımlama

Tüm Emniyet marjlarını, takvim günleri veya iş günleri temel alınarak hesaplanacak şekilde ayarlayabilirsiniz.

1. **Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin.
1. **Genel** sekmesinde, **Gün cinsinden emniyet marjları** bölümünde, çalışma günlerini temel alarak marjları hesaplamak için **Çalışma günleri** seçeneğini *Evet* olarak ayarlayın. Takvim günlerini temel alarak marjları hesaplamak için bu seçeneği *Hayır* olarak ayarlayın.

Örneğin, bir takvim Pazartesi'den Cuma gününe kadar açık ve Cumartesi'den Pazar'a kapalıdır. Bir günlük giriş marjı varsa, Pazartesi günündeki gereksinim tarihi önceki Cuma günü teslim tarihi oluşturur, çünkü Cumartesi ve Pazar günleri çalışma günleri değildir.

Çalışma günlerini belirlemek için kullanılan takvim, kuruluma ve tedarik türüne bağlıdır. Karşılama grubu, ambar ve satıcı takvimleri tarafından denetlenebilir.

> [!NOTE]
> *Ambar* kapsam boyutunun bir parçası değilse (başka bir deyişle, planlama yalnızca *tesis*'i temel alır), ambar takvimi kullanılmaz.

Sistem, bir veya daha fazla takvim tanımlandığı bir kurulumu kullanabilir. Aşağıdaki alt kısımlar sonucu kontrol etmek için kullanılabilen olası birleşimleri açıklar.

#### <a name="calendar-that-is-used-for-the-duration"></a>Süre için kullanılan takvim

Tanımlanan takvimler, tedarik emri tarihinden talep gereksinim tarihine kadar olan gerçek toplam sağlama süresini takvim günlerinde kontrol eder. Aşağıdaki takvim öncelik belirlemesi kullanılır:

- **Satınalma sağlama süresi**: Yalnızca karşılama grubu takvimi dikkate alınır.
- **Giriş marjı**: Tanımlanmışsa, karşılama grubu takvimi kullanılır. Aksi halde, ambar takvimi kullanılır.
- **Çıkış marjı**: Tanımlanmışsa, karşılama grubu takvimi kullanılır. Aksi halde, ambar takvimi kullanılır.
- **Sipariş sınırı**: Yalnızca karşılama grubu takvimi dikkate alınır.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Son tarih için kullanılan takvim

Planlama altyapısının belirli bir tarih türü için belirli bir tarihi kullanıp kullanamayacağını belirlemek için aşağıdaki kurallar uygulanır:

- **Satınalma giriş tarihi**: Tanımlanmışsa, satıcı takvimi kullanılır. Aksi takdirde tanımlanmışsa, karşılama grubu takvimi kullanılır. Bu takvimlerden hiçbiri tanımlanmadıysa, ambar takvimi kullanılır.
- **Transfer giriş tarihi**: Tanımlanmışsa, karşılama grubu takvimi kullanılır. Aksi halde, ambar takvimi kullanılır.
- **Üretim giriş tarihi**: Tanımlanmışsa, karşılama grubu takvimi kullanılır. Aksi halde, ambar takvimi kullanılır.
- **Talep çıkış açık günü**: Tanımlanmışsa, karşılama grubu takvimi kullanılır. Aksi takdirde karşılama grubu takvimi kullanılır.
- **Sipariş açık günü**: Karşılama grubu takviminin ve satıcı takviminin bir birleşimi (kesişim) kullanılır. Tarihi kullanmak için iki takvim de açık olmalıdır. Bu takvimlerden yalnızca biri tanımlandıysa, söz konusu takvimi tek başına kullanılır.

#### <a name="calendar-setup-overview-matrix"></a>Takvim kurulumu genel görünüm matrisi

Aşağıdaki şekilde, emniyet marjları hesaplanırken hangi takvimlerin uygulanacağını özetleyen bir matris gösterilir. (Yüksek çözünürlüklü bir sürümü açılacak görüntüyü seçin.) Aşağıdaki kısaltmalar ve renkler, her bir takvim türünün belirtildiği yeri göstermek için kullanılır:

- **Karşılama grubu (CG):** yeşil
- **Ambar (WH):** sarı
- **(V) satıcı:** mavi

[![Takvim kurulumu genel görünüm matrisi](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Gecikmeleri hesaplama

Sistem bir siparişin geciktirilip gecikmediğini belirlediğinde, üç güvenlik marjı türünün tümü de eklenir.

Örneğin, bir maddenin bir günlük sağlama süresi ve üç günlük giriş marjı vardır. Bu madde için bir satış siparişi bugün gerekli olarak ayarlandı. Bu durumda, gecikme, *sağlama süresi* + *girişi marjı* = dört gün olarak hesaplanır. Bu nedenle, bugün 14 Ağustos ise, dört günlük gecikme 18 Ağustos'ta bir teslimat oluşturur. Aşağıdaki şekilde bu örnek gösterilmiştir.

![Gecikme hesaplama örneği](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama](get-started.md)

[Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]