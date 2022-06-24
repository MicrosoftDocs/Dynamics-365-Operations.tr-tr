---
title: Üretim planlama
description: Bu makalede üretim planlaması açıklanır ve Planlamayı En İyi Duruma Getirme kullanılarak planlı üretim emirlerinin nasıl değiştirileceği anlatılır.
author: t-benebo
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 151aa3688c570ea6ec282c297ed18288dd886131
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873796"
---
# <a name="production-planning"></a>Üretim planlama

[!include [banner](../../includes/banner.md)]

Planlamayı En İyi Duruma Getirme, birçok üretim senaryosunu destekler. Mevcut, yerleşik master planlama altyapısından geçiş yapıyorsanız değiştirilen bazı davranışları öğrenmeniz gerekir.

Aşağıdaki video, bu makalede ele alınan bazı kavramlara kısa bir giriş sağlar: [Dynamics 365 Supply Chain Management: Planlamayı İyileştirme'deki geliştirmeler](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-on-this-feature-for-your-system"></a>Sisteminiz için bu özelliği etkinleştirme

Sisteminiz bu makalede açıklanan özellikleri zaten içermiyorsa [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Planlama Optimizasyonu için planlı üretim emirleri* özelliğini açın.

## <a name="planned-production-orders"></a>Planlı üretim emirleri

Master planlama gereksinimleri karşılamak üzere planlı siparişler oluşturduğunda, sipariş türü **Planlı sipariş türü** alanındaki değere göre belirlenir. **Planlı sipariş türü** alanı *Üretim* olarak ayarlanmışsa, planlanan üretim emirleri oluşturulur. Bu planlı üretim emirleri, etkin ürün reçeteleri (BOM) ve ilgili üretim kurulumundaki rota kodu hakkında bilgiler içerir.

## <a name="requirements-from-boms"></a>Ürün reçetelerindeki gereksinimler

Master planlama sırasında ürün reçetesi bilgileri dikkate alınır. Plan çıktısı, üretim için ilgili malzeme talebini kapsayacak malzeme tedarikini içerir.

Master planlama sırasında geçerli, etkin ürün reçetesi üretim için gerekli olan malzemeleri belirlemek için kullanılır. Bu adım, gerekli üretim emriyle ilişkili ürün reçetesi yapısının tüm düzeylerinde gerçekleştirilir. Malzeme gereksinimi, kullanılabilir eldeki stok, siparişteki mevcut tedarik ve onaylanmış planlı siparişler kullanılarak yerine getirilir. Herhangi bir yerde ek malzeme gerekiyorsa talebi kapsayacak şekilde planlı bir sipariş oluşturulur.

## <a name="scheduling-during-firming"></a>Kesinleştirme sırasında planlama

Planlı üretim emirleri, üretim planlaması için gerekli rota kodunu içerir. Ancak, planlı siparişler için planlama çalıştırması sırasında destek zamanlama işlemi bekler. Rota kodu, kesinleştirme sırasında planlanan üretim emirlerini zamanlamak için kullanılır. Bu nedenle, planlanan üretim emirlerindeki sağlama süresi, burada açıklandığı gibi, bunlar temel alınarak oluşturulan ilgili zamanlanmış, kesinleştirilmiş üretim emirlerindeki sağlama süresinden farklı olabilir.

- **Planlı üretim emri**: Sağlama süresi, serbest bırakılan ürünün statik sağlama süresini temel alan bir görevdir.
- **Kesinleştirilmiş üretim emri**: Sağlama süresi rota bilgilerini ve ilgili kaynak kısıtlamalarını kullanan zamanlamaya dayanır.

Beklenen özellik kullanılabilirliği hakkında daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).

Henüz Planlamayı En İyi Duruma Getirme için sunulmayan üretim işlevini kullanıyorsanız yerleşik master planlama altyapısını kullanmaya devam edebilirsiniz. Özel durum gerekli değildir.

## <a name="delays"></a>Gecikmeler

Gerekli malzemenin sağlama süresi bugünün tarihi ile malzeme gereksinim tarihi arasındaki dönemden uzunsa, gerekli malzeme ve ilgili üretim emri için planlanan emir geciktirilir. Planlı emirler için, gün cinsinden gecikme serbest bırakılan ürünün sağlama süresine göre hesaplanır. Sonra, gecikme bilgileri ürün reçetesi yapısının tüm düzeylerinde uygulanır. Bu nedenle, gecikmiş ham maddenin etkisini müşterinin satış siparişine göre takip edebilirsiniz.

## <a name="modifying-planned-orders"></a>Planlı siparişleri değiştirme

Planlı sipariş ile ilgili bilgileri değiştirdiğinizde şu iletiyi alırsınız: "Planlı siparişlerde el ile yapılan değişikliklerin etkisi, bir sonraki master planlamayı çalıştırma işlemine kadar planın geri kalanına yansıtılmaz."

Planlı bir siparişte yer alan bilgileri değiştirmek ve ilgili malzeme gereksinimleri üzerindeki etkiyi görmek istiyorsanız aşağıdaki adımları izleyin.

1. Planlı siparişi güncelleyin.
2. Planlı siparişi onaylayın.
3. Master planlamayı çalıştırın.

Master planlamayı çalıştırdığınızda, planlanan üretim emirleri dahilse filtre kullanmamalısınız. Daha fazla bilgi için bu makalenin sonraki kısımlarında yer alan [Filtreler](#filters) bölümüne bakın.

> [!NOTE]
> Planlı siparişin teslimat tarihi sonraki bir tarihe değiştirilirse talep yeni bir planlı siparişle ilişkilendirilebilir. Bu davranış, yeni tedarik tarihi ilişkilendirilmiş talep için gecikmeye neden olduğunda ancak sağlama süresi ayarlarına göre gecikme önlenebileceğinde gerçekleşir.

## <a name="explosion-page"></a>Açılım sayfası

Belirli bir üretim emri veya planlı üretim emri için gerekli talebi, ilgili kapsamı ve ilişkilendirme bilgilerini analiz etmek için **Açılım** sayfasını kullanabilirsiniz. **Açılım** sayfasındaki bilgiler master planlama sırasında güncelleştirilir. Bilgileri, doğrudan **Açılım** sayfasından güncelleştiremezsiniz.

## <a name="filters"></a><a name="filters"></a>Filtreler

Planlamayı En İyi Duruma Getirme işlevinin doğru sonucu hesaplamak için gerekli bilgilere sahip olmasını sağlamak için planlı siparişin tüm ürün reçetesi yapısındaki ürünlerle ilişkisi olan tüm ürünleri dahil etmelisiniz. Üretim içeren planlama senaryoları için bu yüzden filtre uygulanmış master planlama çalıştırmaların kullanmamanızı öneririz.

Yerleşik master planlama altyapısı kullanıldığında bağımlı alt öğeler otomatik olarak tespit edilip master planlama çalışmalarına dahil edilse de Planlamayı En İyi Duruma Getirme şu anda bu eylemi gerçekleştirmez.

Örneğin, A ürününün ürün reçetesi yapısından yapılan tek bir cıvata, B ürününü üretmek için de kullanılırsa A ve B ürünlerinin ürün reçetesi yapısındaki tüm ürünler filtreye dahil edilmelidir. Tüm ürünlerin filtrenin parçası olduğundan emin olmak karmaşık olabileceğinden, üretim emirleri söz konusu olduğunda filtre uygulanmış master planlama çalıştırmalarını kullanmamanızı öneririz. Aksi durumda, master planlama istenmeyen sonuçlar sağlar.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Filtre uygulanmış master planlama çalıştırmalarını gerçekleştirmemek için nedenler

Bir ürün için filtrelenmiş master planlama çalıştırdığınızda, Planlamayı En İyi Duruma Getirme (yerleşik master planlama alt yapısının aksine), söz konusu ürünün ürün reçetesi yapısındaki tüm alt ürünleri ve hammaddeleri algılamaz ve bu nedenle bunları master planlama çalıştırmasına bunları dahil etmez. Planlamayı En İyi Duruma Getirme, ürünün ürün reçetesi yapısındaki ilk düzeyi tanımladığı halde, veritabanındaki herhangi bir ürün ayarını (varsayılan sipariş türü veya madde kapsamı gibi) yüklemez.

Planlamayı En İyi Duruma Getirme sırasında, çalıştırmaya ilişkin veriler önceden yüklenir ve filtreler uygular. Bu, belirli bir ürüne dahil edilen bir alt ürün veya ham malzeme filtrenin parçası değilse, çalıştırma için bu ilgili bilgilerin yakalanmayacağı anlamına gelir. Ek olarak, alt ürün veya hammadde başka bir ürüne dahil edildiğinde, yalnızca orijinal ürün ve bileşenleri içeren filtre uygulanmış bir çalıştırma, o diğer ürün için oluşturulmuş varolan planlı talebi kaldırır.

Bu mantık, filtre uygulanmış master planlama çalışmalarının beklenmeyen sonuçlar üretmesine neden olabilir. Aşağıdaki bölümlerde, oluşabilecek beklenmedik sonuçları gösteren örnekler verilmiştir.

### <a name="example-1"></a>Örnek 1

Tamamlanan *FG* malı, aşağıdaki bileşenlerden oluşur:

- Hammadde *R*
- *S2* alt ürününden oluşan alt ürün *S1*

*R* hammadesi için eldeki stok mevcutken *S1* alt ürünü stokta mevcut değildir.

Tamamlanmış *FG* malı için filtre uygulanmış bir master planlama gerçekleştirdiğinizde, tamamlanan *FG* malı için planlı bir üretim emri, *R* ham malzemesi için planlı bir satınalma siparişi ve *S1* alt ürünü için planlı bir satınalma siparişi elde edebilirsiniz. Bu istenmeyen bir sonuçtur çünkü Planlamayı En İyi Duruma Getirme, *R* hammadesi için varolan tedariği yok saydı ve *S1* altmaddesinin doğrudan sipariş yerine *S2* kullanılarak üretilmesi gerekir. Bunun nedeni, Planlamayı En İyi Duruma Getirmenin, mevcut bileşen kaynağı veya bunların varsayılan sipariş ayarları gibi ilgili bilgileri içermeyen, yalnızca tamamlanan *FG* malı bileşenler listesine sahip olmasıdır.

### <a name="example-2"></a>Örnek 2

Önceki örnekten devam edersek, ek bir tamamlanan *FG2* malı da *S1* alt ürününü kullanmaktadır. Tamamlanan *FG2* malı için bir planlı sipariş bulunur ve *S1* dahil olmak üzere tüm bileşenler için planlı bir talep vardır.

Tamamlanan *FG* malı ürün reçetesi yapısından tüm alt ürünleri ve ham malzemeleri filtreye ekleyerek ve sonra eksiksiz yeniden oluşturma işlemi çalıştırarak önceki örnekteki filtre uygulanmış master planlama çalıştırmasının istenmeyen sonuçlarının üstesinden gelmeye karar verirsiniz.

Eksiksiz yeniden oluşturmayı çalıştırdığınızda, sistem dahil edilen tüm ürünlerle ilgili varolan tüm sonuçları siler ve sonra yeni hesaplamaları temel alarak sonuçları yeniden oluşturur. Bu, *S1* ürünü için varolan planlı talebin silindiği ve daha sonra hesaba yalnızca tamamlanan *FG* malının gereksinimlerini kattığını, *FG2* gereksinimlerini yok saydığı anlamına gelir. Bunun nedeni, Planlamayı En İyi Duruma Getirmeyi çalıştırdığınızda, planlanan diğer üretim emirlerinin planlı talebini dahil etmemesidir&mdash;yalnızca çalıştırma sırasında oluşturulan planlı talep kullanılır.

> [!NOTE]
> Tamamlanan *FG2* malının varolan planlı siparişin durumu *Onaylandı* ise, üst ürün filtreye eklenmemiş olsa bile onaylanan planlı talep dahil edilir.

Bu nedenle, tamamlanan *FG* malı, tamamlanan *FG2* malı ve bu bileşenlerin parçası olan tüm diğer ürünler (bileşenleriyle birlikte) eklenmedikçe, filtre uygulanan master planlama çalışması istenmeyen sonuçlara neden olur.

Tüm ürünlerin filtrenin parçası olduğundan emin olmak karmaşık olabileceğinden, üretim emirleri söz konusu olduğunda filtre uygulanmış master planlama çalıştırmalarını kullanmamanızı öneririz.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
