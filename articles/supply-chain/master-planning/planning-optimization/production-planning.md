---
title: Üretim planlama
description: Bu konuda üretim planlaması açıklanır ve Planlamayı En İyi Duruma Getirme kullanılarak planlı üretim emirlerinin nasıl değiştirileceği anlatılır.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992407"
---
# <a name="production-planning"></a>Üretim planlama

Planlamayı En İyi Duruma Getirme, birçok üretim senaryosunu destekler. Mevcut, yerleşik master planlama altyapısından geçiş yapıyorsanız değiştirilen bazı davranışları öğrenmeniz gerekir.

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

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

Master planlamayı çalıştırdığınızda, planlanan üretim emirleri dahilse filtre kullanmamalısınız. Daha fazla bilgi için bu konunun sonraki kısımlarında yer alan [Filtreler](#filters) bölümüne bakın.

> [!NOTE]
> Planlı siparişin teslimat tarihi sonraki bir tarihe değiştirilirse talep yeni bir planlı siparişle ilişkilendirilebilir. Bu davranış, yeni tedarik tarihi ilişkilendirilmiş talep için gecikmeye neden olduğunda ancak sağlama süresi ayarlarına göre gecikme önlenebileceğinde gerçekleşir.

## <a name="explosion-page"></a>Açılım sayfası

Belirli bir üretim emri veya planlı üretim emri için gerekli talebi, ilgili kapsamı ve ilişkilendirme bilgilerini analiz etmek için **Açılım** sayfasını kullanabilirsiniz. **Açılım** sayfasındaki bilgiler master planlama sırasında güncelleştirilir. Bilgileri, doğrudan **Açılım** sayfasından güncelleştiremezsiniz.

## <a name="filters"></a><a name="filters"></a>Filtreler

Üretim içeren planlama senaryoları için filtre uygulanmış master planlama çalıştırmaların kullanmamanızı öneririz. Planlamayı En İyi Duruma Getirme işlevinin doğru sonucu hesaplamak için gerekli bilgilere sahip olmasını sağlamak için planlı siparişin tüm ürün reçetesi yapısındaki ürünlerle ilişkisi olan tüm ürünleri dahil etmelisiniz.

Yerleşik master planlama altyapısı kullanıldığında bağımlı alt öğeler otomatik olarak tespit edilip master planlama çalışmalarına dahil edilse de Planlamayı En İyi Duruma Getirme bu eylemi gerçekleştirmez.

Örneğin, A ürününün ürün reçetesi yapısından yapılan tek bir cıvata, B ürününü üretmek için de kullanılırsa A ve B ürünlerinin ürün reçetesi yapısındaki tüm ürünler filtreye dahil edilmelidir. Tüm ürünlerin filtrenin parçası olduğundan emin olmak çok karmaşık olabileceğinden, üretim emirleri söz konusu olduğunda filtre uygulanmış master planlama çalıştırmalarını kullanmamanızı öneririz.
