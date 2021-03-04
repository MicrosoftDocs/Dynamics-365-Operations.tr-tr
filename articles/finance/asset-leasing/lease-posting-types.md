---
title: Kira deftere nakil türleri
description: Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449023"
---
# <a name="lease-posting-types"></a>Kira deftere nakil türleri

[!include [banner](../includes/banner.md)]

Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.

## <a name="lease-asset"></a>Kiralama kıymeti

Hesap, kullanım hakkı (ROU) varlığıyla ilişkilidir. Kiralama; yeni kiralama muhasebe standartları, Muhasabe Standartları Kodlaması Konu 842 (ASC 842) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) kapsamında ilk kez kabul edildiğinde hesap borçlandırılır. Değiştirilmiş bir kiralama için, bu hesap, değişikliğin kira yükümlülüğünü artırmasına veya azaltmasına bağlı olarak borçlandırılabilir veya alacaklandırılabilir.

**Örnek günlük girişleri**: İlk kabul<br>
**Borç**: Kiralama varlığı XXX<br>
**Alacak**: Kiralama yükümlülüğü XXX

## <a name="lease-liability"></a>Kiralama yükümlülüğü

Hesap, yeni IFRS 16 ve ASC 842 standartları kapsamında ödemelere iskonto uygulandığında oluşan kira yükümlülüğüyle ilişkilidir. Bu hesap, bir kiralama yeni standartlar kapsamında ilk kez kabul edildiğinde alacaklandırılır. Kira ödemeleri için borçlandırılır ve faiz tahakkukları için alacaklandırılır.

**Örnek günlük girişleri**: İlk kabul<br>
**Borç**: Kiralama varlığı XXX<br>
**Alacak**: Kiralama yükümlülüğü XXX

**Örnek günlük girişleri**: Faiz tahakkuku<br>
**Borç**: Faiz gideri XXX<br>
**Alacak**: Kiralama yükümlülüğü XXX

**Örnek günlük girişleri**: Kira ödemesi<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Alacak**: Satıcı borç/kira ödemesi XXX

## <a name="short-term-lease-liability"></a>Kısa süreli kiralama yükümlülüğü

Kısa süreli kiralama yükümlülüğü yeniden sınıflandırma günlük girişi deftere nakledildiğinde, hesap kısa süreli kira yükümlülüğüyle ilişkilendirilir. Bu hesap, ayın son günündeki amortisman planında kısa süreli yükümlülük için alacaklandırılır. Ancak, aynı tutar sonraki ayın ilk gününe borç olarak kaydedilir.

**Örnek günlük girişleri**: Kısa süreli kira yükümlülüğü yeniden sınıflandırma<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Alacak**: Kısa süreli kiralama yükümlülüğü XXX<br>
**Borç**: Kısa süreli kiralama yükümlülüğü XXX<br>
**Alacak**: Kiralama yükümlülüğü XXX

## <a name="depreciation-expense"></a>Amortisman gideri

Hesap, IFRS 16, ASC 842 ve IAS 17 ile ASC 840 kapsamındaki finansal kiralamalar kapsamındaki ROU valrığının amortismanıyla ilgili giderle ilişkilidir. Her ay ROU varlığına amortisman uygulandığında bu hesaba borç kaydedilir.

**Örnek günlük girişleri**: Amortisman tahakkuku<br>
**Borç**: Amortisman gideri XXX<br>
**Alacak:** Birikmiş Amortisman XXX

## <a name="gainloss-on-lease-modification"></a>Kiralama değişikliğinde kazanç/kayıp

Hesap, kiralama değişikliklerinden doğan tüm kazanç veya kayıplarla ilişkilidir. Değişiklik, kiralama yükümlülüğünü ROU varlığının defter değerini aşacak bir tutarda azaltırsa kiralama değişikliği sırasında bir kazanç oluşabilir.

Örneğin, bir kiralamanın kiralama yükümlülüğü geçerli defter değerinin 150.000 ABD doları ve ROU varlığının defter değerinin 100.000 ABD doları olduğunu düşünelim. Kira değiştirilir ve bu değişiklik gelecekteki en düşük kira ödemelerinin (PVFMLP) yeni bir şimdiki değerini oluşturur (40.000 ABD doları). Bu nedenle, kiralama yükümlülüğü 110.000 (150.000 – 40.000) (ABD doları) ile borç kaydedilir. ROU varlığı yalnızca 100.000 ABD doları olduğundan, 110.000 ABD doları tutarındaki azalma varlığı 0 (sıfır) değerinin altına düşürür. Bu nedenle, muhasebe kılavuzu kalan kısmın bir kazanç hesabına kaydedilmesi gerektiğini belirtir. Bu durumda, son günlük girişi kiralama yükümlülüğüne 110.000 ABD doları borç, kiralama varlığına 100.000 ABD doları alacak ve kazanç hesabına 10.000 ABD doları alacak olacaktır.

**Örnek günlük girişleri**: Kiralama değişikliği<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Alacak**: Kiralama Varlığı XXX<br>
**Alacak**: Kazanç XXX

## <a name="accumulated-depreciation"></a>Birikmiş amortisman

Hesap, ROU varlığının karşı varlık hesabıyla ilişkilidir. Bu hesap, bir amortisman gideri deftere nakledildiğinde alacaklandırılır.

**Örnek günlük girişleri**: Amortisman tahakkuku<br>
**Borç**: Amortisman gideri XXX<br>
**Alacak:** Birikmiş amortisman XXX

## <a name="retained-earnings"></a>Yedek akçe

Bu hesap, dağıtılmamış kazançlarla ilişkilidir. Bu hesap, tam geriye dönük yöntem veya kümülatif yakalama seçeneği A yöntemi kullanılarak bir geçiş düzeltme günlüğü girişinde borçlandırılabilir veya alacaklandırılabilir. İlk ROU varlığı ile kiralama yükümlülüğü arasındaki fark, dağıtılmamış kazançlara kaydedilir. Nadiren de olsa, ROU varlığının kiralama yükümlülüğüne eşit olması için değerinin artırılması veya azaltılması amacıyla kiralama sınıflandırmasının finansaldan işletmeye geçmesi durumunda kalan kazançlar da kiralama değişikliğinden etkilenebilir.

**Örnek günlük girişleri**: Geçiş düzeltmesi (tam geriye dönük veya kümülatif yakalama seçeneği A yöntemi)<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Alacak**: Kiralama varlığı XXX<br>
**Alacak**: Dağıtılmamış kazançlar xxx

## <a name="variable-payment"></a>Değişken ödeme

Hesap, ASC 842, ASC 840 ve IAS 17 kiralamaları kapsamında endeks yeniden değerleme tarafından oluşturulan değişken kira ödemeleriyle ilişkilidir. Kira ödemesi planında değişken ödemeler **Değişken ödeme** sütununa dahil edilir. Değişken ödeme içeren bir ödeme planı satırı için fatura oluşturulduğunda, bu hesaba borç kaydedilir.

**Örnek günlük girişleri**: Kira ödemesi<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Borç**: Değişken ödeme XXX<br>
**Alacak**: Satıcı borç/kira ödemesi XXX

## <a name="deferred-rent-asset-liability"></a>Ertelenmiş kira varlığı (yükümlülüğü)

Bu hesap, ertelenmiş kira işlemi kiralaması tarafından oluşturulan ertelenmiş kira varlığı veya yükümlülüğü ile ilişkilidir. Kira ödemesi tutarı dönemin sabit esaslı kira giderinden fazlaysa ertelenmiş kira işlem kiralaması için fatura oluşturulduğunda bu hesaba borç kaydedilir. Kira ödemesi dönemin sabit esaslı kira giderinden azsa alacak kaydedilir.

**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)<br>
**Borç**: Kiralama gideri XXX<br>
**Alacak**: Ertelenmiş kira yükümlülüğü XXX<br>
**Alacak**: Satıcı borç/kira ödemesi XXX

## <a name="lease-expense"></a>Kiralama gideri

Kiralama ertelenmiş kira işlem kiralaması olarak sınıflandırılırsa hesap kiralama gideriyle ilişkilendirilir. Ertelenmiş kira işlem kiralaması için bir fatura oluşturulduğunda bu hesaba borç kaydedilir.

**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)<br>
**Borç**: Kiralama gideri XXX<br>
**Alacak**: Ertelenmiş kira yükümlülüğü XXX<br>
**Alacak**: Satıcı borç/kira ödemesi XXX

## <a name="impairment-expense"></a>Değer düşüşü gideri

Bir kiralamanın değeri düşürüldüğünde hesap deftere nakledilir. Bu hesap borçlandırılır ancak ROU varlığı hesabı doğrudan alacaklandırılır.

**Örnek günlük girişleri**: Kira ödemesi<br>
**Borç:** Değer düşüşü gideri XXX<br>
**Alacak**: ROU varlığı XXX

## <a name="lease-payment"></a>Kira ödemesi

**Satıcıya Öde** parametresi kapalıysa hesap deftere nakledilir. Parametre kapatılmışsa satıcı borcu yerine bu hesap alacaklandırılır.

**Örnek günlük girişleri**: Kira ödemesi<br>
**Borç**: Kiralama yükümlülüğü XXX<br>
**Alacak**: Kira ödemesi XXX

## <a name="expense-type-postings"></a>Gider türü deftere nakiller

Her gider türü için seçilen hesap, ilgili gider türü için bir ödeme oluşturulduğunda borçlandırılır. Örneğin, **Sigorta** gider türü için belirtilen bir hesap, sigorta gideri için icra maliyeti planından bir fatura veya ödeme günlük giriş oluşturulduğunda borçlandırılır.

**Örnek günlük girişleri**: Sigorta ödemesi<br>
**Borç**: Sigorta gideri türü hesabı XXX<br>
**Alacak**: Mahsup hesap XXX

> [!NOTE]
> Mahsup hesap, icra maliyeti ödeme planı için satırlardaki kiralama düzeyinde seçilir. Bu mahsup hesap, satıcıyla veya bir genel muhasebe hesabıyla ilişkilendirilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]