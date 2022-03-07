---
title: Sabit kıymet grupları için yenileme maliyetlerini ve sigortalı değerleri yeniden hesaplama
description: Bu makalede, sabit kıymetlerin yenileme maliyetlerini ve sigortalanan değerlerini güncelleştirme işlemi açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c66f51a513524cfad7fb5382efa748197f9b4bac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990526"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Sabit kıymet grupları için yenileme maliyetlerini ve sigortalı değerleri yeniden hesaplama

[!include [banner](../includes/banner.md)]

Bu makalede, sabit kıymetlerin yenileme maliyetlerini ve sigortalanan değerlerini güncelleştirme işlemi açıklanmaktadır.

Düzenli aralıklarla, değiştirme maliyeti veya sigortaya özel sabit kıymetlerin değiştiği size bildirilebilir. Örneğin, yöneticiniz enflasyonun bir önceki yıl yüzde 3 olduğunu, bu nedenle tüm sabit kıymetlerin değiştirme maliyetini yüzde 3 ile arttırmanız gerektiği konusunda sizi bilgilendirebilir. 

**Sabit kıymet** sayfasındaki her bir sabit kıymet için yenileme maliyetini ve sigortalanan değeri düzenleyebilirsiniz, ancak bir grup için bu değerleri aynı anda güncellemek üzere **Yenileme maliyetlerini ve sigortalanan değerleri güncelle** sayfasını kullanabilirsiniz. Bu bilgiler, sabit kıymet grupları veya gruplardaki belirli kıymetler için değerleri nasıl güncelleyeceğinizi açıklamaktadır.

## <a name="how-values-are-updated"></a> Değerler nasıl güncellenir
Sabit kıymet grupları için yenileme maliyetlerini ve sigortalanan değerlerini yeniden hesaplamak için, öncelikle mevcut yenileme maliyetlerinin ve sigortalanan değerlerin değiştirileceği yüzdeyi belirlemeniz ve ardından değerleri gerçekte yeniden hesaplamak için düzenleme güncelleme gerçekleştirmeniz gerekir. **Sabit kıymet grupları** sayfasındaki **Yenileme maliyeti faktörü** ve **Sigortalanan değer faktörü** alanlarındaki yüzdeyi belirleyin. Sabit kıymet grubu için bu faktörleri belirlemenize rağmen **Yenileme maliyetlerini ve sigortalanan değerleri güncelle** sayfasını kullandığınızda sadece bir gruptaki belirli sabit kıymetler için yenileme maliyetini ve sigortalanan değeri yeniden hesaplamayı seçebilirsiniz. 

Kıymetler için yenileme maliyetini ve sigortalanan değeri yeniden hesaplamak için **Yenileme maliyetlerini ve sigortalanan değerleri güncelle** sayfasını kullanırken şu formüllerden yararlanabilirsiniz:

-   \[(Kıymet grubunun yenileme maliyeti faktörü / 100) + 1\]\* Kıymetin varolan yenileme maliyeti
-   \[(Kıymet grubunun sigortalanan değer faktörü / 100) + 1\]\* Kıymetin varolan sigortalanan değeri

> [!NOTE] 
> **Yenileme maliyetlerini ve sigortalanan değerleri güncelle** sayfasını kullandığınızda, seçili kıymetlerin hem yenileme maliyeti hem de sigortalanan değeri güncelleştirilir; yalnızca bir değerin güncelleştirilmesini belirtemezsiniz. Bir değeri aynı bırakmak ve diğer değeri güncelleştirmek için, **Sabit kıymet grubu** sayfasında faktör olarak 0 (sıfır) değerini girin. Sıfır veya boş faktör, güncelleştirmede hesaplamanın atlanmasına neden olur. Sabit kıymetlerin defter değeri ve net defter değeri periyodik güncelleştirmeden etkilenmez. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Hangi maddelerin güncelleştirileceğini seçmek için tarih kullanma
Varsayılan olarak, güncelleştirme işlemi geçerli günde güncelleştirilmemiş ancak önceki günlerde güncelleştirilmiş olabilen seçili kıymetleri güncelleştirir. Örneğin, &lt; geçerli tarih "bugünün tarihinden önce" anlamına gelir. Tarihi **Yenileme maliyetlerini ve sigortalı değerleri güncelleştir** sayfasında **Seç** düğmesine tıklayarak değiştirebilirsiniz. Belirlediğiniz tarih kriteri, kıymet için son düzenli güncelleştirme tarihiyle karşılaştırılır (**Sabit kıymetler** sayfasındaki **Son düzenli değer/maliyet güncelleştirme** alanı). Bir sabit kıymet için yenileme maliyetini veya sigortalanan değeri her güncelleştirdiğinizde **Son düzenli değer/maliyet güncelleştirme** alanı, güncel tarihle otomatik olarak güncelleştirilir. 

Örnek 

Dün Araçlar, Ofis Mobilyaları ve Binaların gruplarının yenileme maliyetini yüzde 5 güncelleştirdiniz ve şimdi bu kıymetlerin doğru bir şekilde güncelleştirilmesini düşünüyorsunuz. Diğer tüm sabit kıymetleri bugün güncelleştirdiğinizde bu kıymetleri dışarıda bırakmak için, **Son dönemsel değer/maliyet güncelleştirme** alanına dünden önce olan bir tarih girersiniz (&lt; dünün tarihi); çünkü **Araçlar**, **Ofis Mobilyaları** ve **Binalar** grupları için son güncelleştirme girdiğiniz tarih kriterleri dışında gerçekleşmiştir.

## <a name="cumulative-effect-of-each-update"></a> Her güncelleştirmenin toplam etkisi
Her güncelleştirme bir toplam etkiye sahiptir. Bu nedenle, güncelleştirmelerinizi dikkatle planlamalısınız. Örneğin, Salı günü tüm kıymetleri yüzde 3 oranında yükseltir ve ardından Cuma günü ofis mobilyalarını yüzde 4 oranında arttırırsanız, ofis mobilyalarını toplamda yüzde 7,12 oranında artar.

## <a name="scenario"></a>Senaryo
Yöneticiniz size aşağıdaki sabit kıymet değişikliklerini bildiriyor:
-   Bilgisayarlar dışındaki tüm sabit kıymetlerin değiştirme maliyetini yüzde 3,25 ile arttırın.
-   Tüm ofis mobilyalarının değiştirme maliyetini ek yüzde 1 ile arttırın.
-   Tüm bilgisayarların değiştirme maliyetini ve sigortalanan değerini yüzde 10 ile azaltın.

Şu değişiklikleri yaparsınız:
1.  **Sabit kıymet grupları** sayfasında, **Ofis Mobilyaları** grubu ve **Bilgisayarlar** grubu dışındaki tüm sabit kıymet grupları için, **Yenileme maliyeti faktörü** alanına 3,25 değerini ve **Sigortalanan değer faktörü** alanına 0 değerini girersiniz.
2.  **Ofis Mobilyaları** grubu için, **Yenileme maliyeti faktörü** alanına 4,25 değerini ve **Sigortalanan değer faktörü** alanına 0 değerini girersiniz.
3.  **Bilgisayarlar** grubu için, **Yenileme maliyeti faktörü** alanına -10 değerini ve **Sigortalanan değer faktörü** alanına -10 değerini girersiniz.
4.  **Yenileme maliyetlerini ve sigortalanan değerleri güncelleştir** sayfasında, tüm sabit kıymetler için yeniden hesaplama gerçekleştirmek için **Tamam** düğmesine tıklarsınız.

Ertesi gün yöneticiniz bilgisayarlarınızın yüzde 10 yerine yüzde 8 oranında azaldığı bilgisini verir, bu nedenle yenileme maliyetlerini ve sigortalanan değerleri düzeltmeniz gerekir. Hatayı düzeltmek için aşağıdaki iki yöntemden birini kullanabilirsiniz:
-   **Bilgisayarlar** sabit kıymet grubunda her bir sabit kıymet için **Sabit kıymetler** sayfasındaki **Sigortalanan değer** ve **Yenileme maliyeti** alanlarını manuel olarak değiştirin. Değerleri, orijinal tutarı yüzde 8 ile azaltmışsınız gibi hesaplayın ve el ile girin. Bu yöntemi kullanarak, **Yenileme maliyetlerini ve sigortalanan değerleri güncelleştir** sayfasını kullanmayın.
-   **Sabit kıymet grupları** sayfasındaki **Yenileme maliyeti faktörü** ve **Sigortalanan değer faktörü** alanlarındaki **Bilgisayar** grubu için yenileme maliyeti ve sigortalanan değer faktörlerini girin. Bu hem kıymetleri orijinal değerlerine sıfırlar (yüzde 10'luk azalıştan önceki) hem de orijinal değere yüzde 8 azalma uygular. Ardından, girdiğiniz faktörlere dayalı olarak değerleri yeniden hesaplamak için **Yenileme maliyetlerini ve sigortalanan değerleri güncelleştir** sayfasını kullanın.

> [!NOTE]  
> Tutarlar amaçladığınız gibi hesaplanmayacağından, –10 faktörünü tersine çevirmek için pozitif 10 faktörü giremezsiniz (veya –10 ile –8 arasındaki fark için 2 faktörü). 





