---
title: "Ürün yapılandırma modeli için hesaplamalar SSS"
description: "Bu makale ürün yapılandırma modelleriyle ilgili hesaplamaları açıklar ve hesaplamalar kısıtlamaları ile birlikte kullanılmasını açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f13d03e5d1a26a5c87d71732b692537be94bdfb8
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Ürün yapılandırma modeli için hesaplamalar SSS

[!include[banner](../includes/banner.md)]


Bu makale ürün yapılandırma modelleriyle ilgili hesaplamaları açıklar ve hesaplamalar kısıtlamaları ile birlikte kullanılmasını açıklar.

Hesaplamalar aritmetik veya mantıksal işlemler için kullanılabilir. Ürün yapılandırma modellerindeki ifade kısıtlamalarını tamamlar. **Kısıtlamaya dayalı ürün yapılandırma modeli ayrıntıları** sayfasında hesaplamaları tanımlayabilir ve ardından ifade düzenleyicideki hesaplamalar için ifadeler oluşturabilirsiniz. Daha fazla bilgi için, Hesaplamalar oluşturma bölümüne bakın.

## <a name="what-is-a-calculation"></a>Hesaplama nedir?
Hesaplama, ürün yapılandırma modelinde kullanabileceğiniz bir öğedir. Hesaplamalar bir ürün yapılandırırken değerleri hesaplamak için ondalık sayılar kullanmanıza izin vererek kısıtlamaları tamamlar. Ayrıca, hesaplamalar, kısıtlamalardan daha geniş bir operatör setine sahiptir.  

Bir kısıtlama gibi, bir hesaplama da ürün yapılandırma modelindeki belirli bir bileşenle ilişkilidir ve başka bir bileşen tarafından veya başka bir bileşenle paylaşımlı olarak kullanılabilir. Hesaplamalar ile kısıtlamalar arasındaki önemli bir fark, hesaplamaların zorunlu (tek yönlü), kısıtlamaların ise tanımlayıcı (çift yönlü) olmasıdır. Kısıtlamalar hakkında daha fazla bilgi için bkz. [İfade kısıtlamaları ve tablo kısıtlamaları](expression-constraints-table-constraints-product-configuration-models.md).  

Bir hesaplama bir hedef özelliği ve bir hesaplama ifadesinden meydana gelir.

## <a name="what-is-a-target-attribute"></a>Hedef öznitelik nedir?
Hedef öznitelik, hesaplama ifadesinin sonucunu alan özniteliktir.  

Aşağıdaki ifadede, hedef öznitelik bir masa örtüsünün ölçümüdür:  

**Deyim:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** masa uzunluğudur ve **decimalAttribute2** masa örtüsü uzunluğudur. **decimalAttribute2** değeri, **decimalAttribute1** değerine eşitse veya daha yüksekse ifade, hedef özniteliğe **Doğru** değerini iletir. Aksi takdirde, ifade **Yanlış** değerini üretir. Bu nedenle, tablecloth uzunluğu tablo uzunluğuyla aynı veya daha yüksek ise tablecloth ölçümü kabul edilebilir.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Hedef özniteliklere hangi öznitelik türleri ayarlanabilir?
Sabit bir listeye sahip olmayan metinler hariç, hedef özniteliklere ürün yapılandırıcının desteklediği tüm öznitelik tipleri ayarlanabilir.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Bir hedef öznitelik değeri bir hesaplamadaki giriş özniteliklerinin değerlerini kısıtlayabilir mi?
Hayır, bir hedef öznitelik değeri giriş özniteliklerinin değerlerini kısıtlayamaz, çünkü hesaplamalar tek yönlüdür. Bu nedenle, giriş öznitelik değeri, giriş öznitelik değerindeki değişikliklere dayalıdır, ancak hedef değerindeki bir değişiklik giriş özniteliklerinin değerini etkilemez. Bu davranış, kısıtlamalara özel davranıştan farklıdır. Kısıtlamalar her iki yönde gerçekleşir.

### <a name="example"></a>Örnek

Aşağıdaki ifadede, hesaplama için hedef bir güç kablosunun boyudur ve giriş değeri bir renktir:  

**Deyim:** \[If Renk == "Yeşil", 1.5, 1.0\]  

Maddeyi yapılandırdığınızda, renk özniteliği olarak **Yeşil** değeri belirtilirse, güç kablosunun uzunluğu **1.5** olarak ayarlanır. Başka bir renk belirlerseniz uzunluk **1.0** olarak ayarlanır. Ancak, hesaplamalar tek yönlü olduğundan, uzunluğu **1.5** değerine ayarlarsanız renk özniteliği rengini **Yeşil** olarak ayarlamaz.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Bir hesaplama tamsayı tipinde bir hedef özniteliğine sahipse, ancak bir ondalıklı sayı üretiyorsa ne olur?
Bir hedef özelliğin tamsayı tipinde ise, ancak bir hesaplama bir ondalıklı sayı üretiyorsa hesaplanan sonucun sadece tamsayı kısmı kullanılır. Ondalıklı kısım kaldırılır ve sonuç yuvarlanmaz. Örneğin, 12.70 sonucu 12 olarak gösterilir.

## <a name="when-do-calculations-occur"></a>Hesaplamalar ne zaman oluşur?
Hesaplamalar tüm öznitelik değerleri için bir değer sağlanmışsa oluşur.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Hedef özniteliği için hesaplanan değerin üzerine yazabilir miyim?
Hedef özniteliği, gizli veya salt okunur olarak ayarlanmadığı sürece hedef özniteliği olarak hesaplanan değerin üzerine yazabilirsiniz.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Bir hedef özniteliği nasıl gizli veya salt okunur olarak ayarlarım?
Bir özniteliği gizli veya salt okunur olarak ayarlamak için şu adımları izleyin:

1.  **Ürün bilgileri yönetimi** &gt; **Ortak** &gt; **Ürün yapılandırma modelleri** öğelerini tıklayın.
2.  Bir ürün konfigürasyon modeli seçin ve ardından İşlem Panosundaki **Düzenle** düğmesini tıklayın.
3.  **Kısıtlamaya dayalı ürün yapılandırma modeli bilgileri** sayfasında bir hedef özniteliği olarak kullanılacak özniteliği seçin.
4.  **Öznitelikler** Hızlı Sekmesinden **Gizli** veya **Salt okunur** öğelerini seçin.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Bir hesaplama ayarladığın değerlerin üzerine yazabilir mi?
Hayır. Bir ürünü yapılandırdığınızda ayarladığınız değerler kullanılan değerlerdir. Bir hesaplamadaki giriş değerleri değiştirildiğinde gerçekleştirilen hesaplama, belirli bir öznitelik için sağladığınız değerlerin üzerine yazamaz.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Bir hesaplamada bir giriş değerini kaldırırsam ne olur?
Bir hesaplamadaki bir giriş değerini kaldırırsanız hedef özniteliği değeri de kaldırılır.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Modelimin uyumsuz olduğunu gösteren hata mesajını neden alıyorum?
Bu mesaj bir hesaplamada bir hata olduğunda veya bir veya daha fazla kısıtlamada bir çakışma meydana geldiğinde görüntülenir. Kısıtlamalardaki çakışmalar hakkında daha fazla bilgi için bkz. [İfade kısıtlamaları ve tablo kısıtlamaları](expression-constraints-table-constraints-product-configuration-models.md). Hesaplamalarda hataların meydana gelebileceği bazı durumlar şunlardır:

-   Bir değerin 0 (sıfır) değerine bölünmesi.
-   Aşağıdaki iki öğe arasında bir çakışma meydana gelmesi:
    -   Bir öznitelik için mevcut olan bir kısıtlamayla sınırlandırılan değerler
    -   Bir hesaplama tarafından oluşturulan bir değer
-   Hesaplama sonucu üretilen değerlerin, öznitelik aralığı dışında kalması. 0 olarak hesaplanan \[1..10\] ifadesinden alınan bir tamsayı buna örnek gösterilebilir.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Ürün modeli başarıyla doğrulamama rağmen neden bir hata mesajı alıyorum?
Hesaplamalar doğrulamaya dahil değildir. Hesaplamalardaki hataları bulmak için ürün yapılandırma modelini test etmelisiniz. Bir ürün yapılandırma modelini test etmek için bu adımları takip edin.

1.  **Ürün bilgileri yönetimi** &gt; **Ortak** &gt; **Ürün yapılandırma modelleri** öğelerini tıklayın.
2.  Bir ürün yapılandırma modeli seçin ve ardından İşlem Panosundan **Yürüt** grubu altındaki **Test** düğmesini tıklayın.





