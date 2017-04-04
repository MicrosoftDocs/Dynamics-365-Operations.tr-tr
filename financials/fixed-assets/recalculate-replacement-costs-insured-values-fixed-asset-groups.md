---
title: "Sabit kıymet grupları için yenileme maliyetlerini ve Sigortalı değerleri yeniden hesapla"
description: "Bu makalede, sabit kıymetlerin yenileme maliyetlerini ve sigortalanan değerlerini güncelleştirme işlemi açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 38f779274da370d436509e021cabf5b90ab08475
ms.lasthandoff: 03/31/2017


---

# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Sabit kıymet grupları için yenileme maliyetlerini ve Sigortalı değerleri yeniden hesapla

Bu makalede, sabit kıymetlerin yenileme maliyetlerini ve sigortalanan değerlerini güncelleştirme işlemi açıklanmaktadır.

Düzenli aralıklarla, değiştirme maliyeti veya sigortaya özel sabit kıymetlerin değiştiği size bildirilebilir. Örneğin, yöneticiniz enflasyonun bir önceki yıl yüzde 3 olduğunu, bu nedenle tüm sabit kıymetlerin değiştirme maliyetini yüzde 3 ile arttırmanız gerektiği konusunda sizi bilgilendirebilir. 

Sabit kıymet formundaki her bir sabit kıymet için yenileme maliyetini ve sigortalanan değerini düzenleyebilirsiniz, ancak bir grup için bu değerleri aynı anda güncellemek üzere Yenileme maliyetlerini ve sigortalanan değerleri güncelleme formunu kullanabilirsiniz. Bu bilgiler, sabit kıymet grupları veya gruplardaki belirli kıymetler için değerleri nasıl güncelleyeceğinizi açıklamaktadır.

## <a name="how-values-are-updated"></a> Değerler nasıl güncellenir
Sabit kıymet grupları için yenileme maliyetlerini ve sigortalanan değerlerini yeniden hesaplamak için, öncelikle mevcut yenileme maliyetlerinin ve sigortalanan değerlerin değiştirileceği yüzdeyi belirlemeniz ve ardından değerleri gerçekte yeniden hesaplamak için düzenleme güncelleme gerçekleştirmeniz gerekir. Sabit kıymet grupları formundaki Yenileme maliyeti faktörü ve Sigortalanan değer faktörü alanlarındaki yüzdeyi belirliyorsunuz. Sabit kıymet grubu için bu faktörleri belirlemenize rağmen Yenileme maliyetlerini ve sigortalanan değerleri güncelle formunu kullandığınızda sadece bir gruptaki belirli sabit kıymetler için yenileme maliyetini ve sigortalanan değeri yeniden hesaplamayı seçebilirsiniz. 

Kıymetler için yenileme maliyetini ve sigortalanan değeri yeniden hesaplamak için yenileme maliyetlerini ve sigortalanan değerleri güncelleme formunu kullanırken şu formüllerden yararlanabilirsiniz:

-   \[(Yenileme maliyeti faktörü kıymet grup / 100) + 1\]\* kıymet varolan yenileme maliyeti
-   \[(Sigortalanan Değer faktörü kıymet grubu / 100) + 1\]\* kıymetin varolan Sigortalanan Değer

> [!NOTE] 
> Yenileme maliyetlerini ve sigortalanan değerleri güncelleme formunu kullandığınızda, seçili kıymetlerin hem yenileme maliyeti hem de sigortalanan değeri güncelleştirilir; yalnızca bir değerin güncelleştirilmesini belirtemezsiniz. Bir değeri aynı bırakmak ve diğer değeri güncelleştirmek için, Sabit kıymet grubu formunda faktör olarak 0 (sıfır) değerini girin. Sıfır veya boş faktör, güncelleştirmede hesaplamanın atlanmasına neden olur. Sabit kıymetlerin defter değeri ve net defter değeri periyodik güncelleştirmeden etkilenmez. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Hangi maddelerin güncelleştirileceğini seçmek için tarih kullanma
Varsayılan olarak, güncelleştirme işlemi geçerli günde güncelleştirilmemiş ancak önceki günlerde güncelleştirilmiş olabilen seçili kıymetleri güncelleştirir. Örneğin, &lt;geçerli tarih anlamına gelir "bugünün tarihinden önce." Güncelleştirme değiştirme maliyetlerini ve Sigortalı değerler formunda Tarih Seç düğmesini tıklatarak değiştirebilirsiniz. Belirlediğiniz tarih kriteri, kıymet için son düzenli güncelleştirme tarihiyle karşılaştırılır (Sabit kıymetler formundaki Son düzenli değer/maliyet güncelleştirme alanı). Bir sabit kıymet için yenileme maliyetini veya sigortalanan değeri her güncelleştirdiğinizde Son düzenli değer/maliyet güncelleştirme alanı, güncel tarihle otomatik olarak güncelleştirilir. 

Örnek 

Taşıtlar, ofis mobilyası ve bina grupları yenileme maliyetini yüzde 5 dün güncelleştirildi ve artık doğru şekilde güncelleştirilmesini bu varlıkları düşünün. Son tarih girdiğiniz tüm diğer sabit kıymetler bugün güncelleştirdiğinizde bu varlıkları dışlamak için Dönemsel değer/maliyet güncelleştirme alanı olan dün önce (&lt; dünün tarihiyle), son güncelleştirme taşıtlar, ofis mobilyası ve bina grupları için girdiğiniz tarih ölçütü dışında oluştu.

## <a name="cumulative-effect-of-each-update"></a> Her güncelleştirmenin toplam etkisi
Her güncelleştirme bir toplam etkiye sahiptir. Bu nedenle, güncelleştirmelerinizi dikkatle planlamalısınız. Örneğin, Salı günü tüm kıymetleri yüzde 3 oranında yükseltir ve ardından Cuma günü ofis mobilyalarını yüzde 4 oranında arttırırsanız, ofis mobilyalarını toplamda yüzde 7,12 oranında artar.

## <a name="scenario"></a>Senaryo
Yöneticiniz size aşağıdaki sabit kıymet değişikliklerini bildiriyor:
-   Bilgisayarlar dışındaki tüm sabit kıymetlerin değiştirme maliyetini yüzde 3,25 ile arttırın.
-   Tüm ofis mobilyalarının değiştirme maliyetini ek yüzde 1 ile arttırın.
-   Tüm bilgisayarların değiştirme maliyetini ve sigortalanan değerini yüzde 10 ile azaltın.

Şu değişiklikleri yaparsınız:
1.  Sabit kıymet grupları formunda, Ofis Mobilyaları grubu ve Bilgisayarlar grubu dışındaki tüm sabit kıymet grupları için, Yenileme maliyeti faktörü alanına 3.25 değerini ve Sigortalanan değer faktörü alanına 0 değerini girersiniz.
2.  Ofis Mobilyaları grubu için, Yenileme maliyeti faktörü alanına 4.25 değerini ve Sigortalanan değer faktörü alanına 0 değerini girersiniz.
3.  Bilgisayarlar grubu için, Yenileme maliyeti faktörü alanına -10 değerini ve Sigortalanan değer faktörü alanına -10 değerini girersiniz.
4.  Yenileme maliyetlerini ve sigortalanan değerleri güncelleştirme formunda, tüm sabit kıymetler için yeniden hesaplama gerçekleştirmek için Tamam düğmesini tıklarsınız.

Ertesi gün yöneticiniz bilgisayarlarınızın yüzde 10 yerine yüzde 8 oranında azaldığı bilgisini verir, bu nedenle yenileme maliyetlerini ve sigortalanan değerleri düzeltmeniz gerekir. Hatayı düzeltmek için aşağıdaki iki yöntemden birini kullanabilirsiniz:
-   Bilgisayarlar sabit kıymet grubunda her bir sabit kıymet için Sabit kıymetler formundaki Sigortalanan değer ve Yenileme maliyeti alanlarını manuel olarak değiştirin. Değerleri, orijinal tutarı yüzde 8 ile azaltmışsınız gibi hesaplayın ve el ile girin. Bu yöntemi kullanarak, Yenileme maliyetlerini ve sigortalanan değerleri güncelleştirme formunu kullanmayın.
-   Sabit kıymet grupları formundaki Yenileme maliyeti faktörü ve Sigortalanan değer faktörü alanlarındaki Bilgisayar grubu için yenileme maliyeti ve sigortalanan değer faktörlerini girin. Bu hem kıymetleri orijinal değerlerine sıfırlar (yüzde 10'luk azalıştan önceki) hem de orijinal değere yüzde 8 azalma uygular. Ardından, girdiğiniz faktörlere dayalı olarak değerleri yeniden hesaplamak için Yenileme maliyetlerini ve sigortalanan değerleri güncelleştirme formunu kullanın.

> [!NOTE]  
> Tutarlar amaçladığınız gibi hesaplanmayacağından, –10 faktörünü tersine çevirmek için pozitif 10 faktörü giremezsiniz (veya –10 ile –8 arasındaki fark için 2 faktörü). 




