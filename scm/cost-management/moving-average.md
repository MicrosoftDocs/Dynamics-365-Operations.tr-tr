---
title: Hareketli ortalama
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-17 15 - 16 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: e75016694e63dbc26f8d4c4ae73204966ca28dcf
ms.lasthandoff: 03/29/2017


---

# <a name="moving-average"></a>Hareketli ortalama



Aşağıdakiler, maliyetlendirme yöntemi olarak hareketli ortalama maliyet kullanırkenki gerekliliklerdir.
1.  **Madde model grupları** sayfasında, **Stok modeli** alanında Hareketli ortalama seçili olan bir madde model grubu belirleyin.
    | **Not **                                                                                                                                |
    |-----------------------------------------------------------------------------------------------------------------------------------------|
    | Varsayılan olarak, Hareketli ortalama seçiliyken, **Fiziksel stoku deftere naklet** ve **Mali stoku deftere naklet** alanları da seçilidir. |

2.  **Deftere nakil** sayfasında, hesapları **Stok** sekmesindeki **Hareketli ortalama için fiyat farkı** ve **Hareketli ortalama için maliyet yeniden değerlemesi** hesaplarına atayın. Maliyetin orantılı harcanması gerektiğinde, **Hareketli ortalama için fiyat farkı** hesabını kullanırsınız. Bunun sebebi, satınalma girişi ile satınalma faturası arasındaki bir maliyet farkıdır ve orijinal stok miktarı ile elde olan miktar arasındaki bir farktır. Bir ürün için hareketli ortalama maliyeti yeni bir birim fiyatına ayarlarken **Hareketli ortalama için maliyet yeniden değerlemesi** hesabını kullanın.
3.  **Serbest bırakılan ürünler** sayfasında, ürüne hareketli ortalama madde model grubu atayın.

| **Not **                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stok kapatma işlemi yalnızca muhasebe dönemini kapatır. Kendilerine bir madde model grubu olarak hareketli ortalama atanmış olan ürünleri etkilemez. |

## <a name="convert-to-the-moving-average-costing-method"></a>Hareketli ortalamaya dönüştürme maliyetlendirme yöntemi
Ürünler, hareketli ortalama stok değerleme yöntemini kullanacak şekilde dönüştürülebilirler. Bu tür dönüştürme genellikle yıl sonunda, geçerli yılın son ayı kapatıldıktan sonra yapılır. Ürünün geçerli maliyetlendirme modeli kullanılarak yapılır. Stok maliyetlendirme yönteminizi, ortalama maliyete veya standart maliyete dayalı maliyetlendirme yönteminden hareketli ortalamaya dayalı bir yönteme değiştirebilirsiniz. Maliyetlendirme yönteminizi standart maliyetlendirme yönteminden hareketli ortalama yöntemine değiştiriyorsanız, şu görevleri gerçekleştirmeniz gerekir:
1.  Stok miktarlarını ve değerlerini 0'a (sıfır) indirmek için ayarlamalar yapın.
2.  Stok değeri ve miktarı 0 (sıfır) iken, madde model grubunu hareketli ortalamaya değiştirin.
3.  Miktar ve değeri yeniden stoka göre ayarlayın.

Stok maliyetlendirme yönteminizi hareketli ortalama yönteminden İlk giren ilk çıkar (FIFO) yöntemine, Son giren ilk çıkar (LIFO) yöntemine veya ağırlıklı ortalama yöntemine değiştiremezsiniz.
| **Not **                                                                      |
|-------------------------------------------------------------------------------|
| Standart maliyetten hareketli ağırlıklı ortalamaya dönüştürmek manuel bir işlemdir. |

Aşağıdaki örnekler, hareketli ortalama maliyetlendirme yöntemini kullanmanın etkisini gösterir. Dört yapılandırma mevcuttur:
-   Satınalma emri ve orantılı olarak harcanan maliyet farkı
-   Hareketli ortalama ürün ve stok düzeltmesi
-   Üretim ile hareketli ortalama
-   Geriye dönük tarihli işlemli hareketli ortalama

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Satınalma emri ve orantılı olarak harcanan maliyet farkı
Hareketli ortalama ile, ürünün maliyeti satınalma girişi tarafından belirlenir. Satınalma faturası deftere nakledildiğinde maliyette satınalma girişi ile satınalma faturası arasında bir fark varsa, fark oransal olarak stoktaki geçerli ürünlere ayarlanır ve kalan miktar harcanır. Bu örnekte, bir satınalma emri oluşturulur ve bir maliyete alınır ve satınalma faturası farklı bir maliyet ile nakledilir.
1.  Miktar olarak 2, birim fiyatı olarak 10,00 şeklinde bir satınalma emri oluşturun.
2.  Ürünün satınalma girişini oluşturun.
3.  Miktar olarak 1, birim fiyatı olarak 10,00 şeklinde bir satış emri oluşturun.
4.  Miktar olarak 2, birim fiyatı olarak 12,00 şeklinde bir satınalma faturası oluşturun.

Birim fiyatındaki fark olan 2,00, satınalma faturası nakledilirken Hareketli ortalama için fiyat farkı hesabına nakledilir. Bunun sebebi, iki ürünün 20,00 maliyetine satın alınmış olmasıdır. Ürünlerden biri 10,00 birim fiyatına satılmıştır. 12,00 2 miktarını içeren bir birim fiyatla satınalma faturası deftere nakledildi. Ürünün birim fiyatını 14.00 at deftere nakledilemez.

## <a name="moving-average-product-and-inventory-adjustment"></a>Hareketli ortalama ürün ve stok düzeltmesi
Bir ürünün hareketli ortalama maliyetini ayarlamanız gerekiyorsa, stok ayarlamalarına bugünün tarihi itibariyle izin verilir. Bir stok ayarlamasına bir ürünün hareketli ortalama maliyetini düzeltmek için eski bir tarih atamazsınız. Ardışık hareketler üzerinden maliyet akışınız olamaz. Bu örnekte, bir ürün için hareketli ortalama maliyet ayarlanmaktadır.
1.  Hareketli ortalama maliyetini ayarlamak istediğiniz ürünü seçin.
    | **Note**                                                                                    |
    |---------------------------------------------------------------------------------------------|
    | ** Hareketli Ortalama için yeniden değerleme ** sayfa bir ürün için kullanılabilir stoku inceler. |

    Seçilen ürünün deftere nakledilen miktarı 1, deftere nakledilen değeri 12,00, deftere nakledilen birim maliyeti 12,00 ve birim maliyeti 12,00'dir.
2.  **Birim maliyeti** alanını 16,00 olarak güncelleyin. Sistem geri kalan alanları hesaplar.
3.  Ayarlama deftere nakledilir.

| **Not **                                                        |
|-----------------------------------------------------------------|
| Hareketli ortalama maliyeti yalnızca bugünün tarihi itibariyle ayarlayabilirsiniz. |

**Fişe ait kapatmalar** sayfasında, Hareketli ortalama için maliyet yeniden değerleme hesabına 4,00'lık bir ayarlama nakledildiğini görebilirsiniz.

## <a name="moving-average-with-production"></a>Üretim ile hareketli ortalama
Hareketli ortalama, üretilen maddeleri destekler. Hareketli ortalama bir üretim ortamında kullanmayı planlıyorsanız, **tahmini maliyet fiyatını kullan** sürgüsünü ** üretim kontrol parametreleri ** sayfa seçili olmalıdır. Bu, fiili ürün reçetesi hesaplama maliyet fiyatı yerine tahmin sırasında hesaplanan maliyet fiyatının kullanılacağı anlamına gelir.

## <a name="moving-average-with-a-backdated-transaction"></a>Geriye dönük tarihli işlemli hareketli ortalama
Geçerli hareketli ortalama maliyete geriye dönük tarih atılmış hareketler atanır ve ürünün fiziksel miktarı güncellenir ama ürünün hareketli ortalama maliyeti etkilenmez. Bu hareketli ortalama örneğinde, bir hareketli ortalama ürünü için deftere geriye dönük tarihli bir hareket nakledilir.
1.  Hareketli ortalama ürüne miktar olarak 1, maliyet olarak 20,00'lik bir stok ayarlaması oluşturun.
2.  Ürünün stok hareket geçmişi aşağıdakine benzeyecektir:
    -   1'lik bir stok hareketi, 16,00'lık bir maliyet, 15 Ocak şeklinde bir deftere nakil tarihi ve 15 Ocak şeklinde bir hareket tarihi.
    -   1'lik bir stok ayarlaması, 20,00'lik bir maliyet, 1 Ocak şeklinde bir deftere nakil tarihi ve 15 Ocak şeklinde bir hareket tarihi.

3.  Ayarlamayı deftere nakledin.

**stok hareketleri** sayfasında, ürün için geçerli hareketli ortalama olarak harcanan 4,00'ın 16,00 olduğunu görebilirsiniz. Geçmişe nakledebilirsiniz ancak maliyetteki fark harcanır, böylelikle hareketli ortalama maliyet etkilenmez.

## <a name="inventory-value-report"></a>Stok değeri raporu
Bu hareketli ortalama örneğinde, ürüne yönelik geçerli hareketli ortalama hesaplamasını desteklemek için stok değeri raporu yazdırılır. Stok değeri raporu, bir ürüne yönelik hareketli ortalama maliyet hesaplamasını desteklemek için maliyetle birlikte hareketleri kronolojik sıra ile yazdırabilir. Rapor, ürün için hareketli ortalama maliyeti gösterir. **Stok değeri raporları** iletişim kutusundaki bir Tarih aralığı, raporu bu değerlerden birine göre sıralamak için **Hareket saati** veya **Deftere nakil tarihi** seçmenize imkan verir. **Deftere nakil tarihi** seçeneği, raporun geleneksel olarak nasıl yazdırılacağıdır. **Hareket saati** seçeneği, hareketin rapor edildiği ve ürün için hareketli ortalama maliyetin güncellendiği fiili tarihtir. Hareketli ortalama maliyet hesaplamasını zaman içinde görmek isterseniz Stok değeri raporunu **Hareket saati sıralaması** seçeneğini kullanarak yazdırabilirsiniz. Aşağıdaki tabloda, **Hareket saati sıralaması** seçeneği kullanıldığında rapor yazdırılan ürün için hareketler gösterilmektedir.

| Hareket saati | Tarih         | Hareket türü           | Miktar | Tutar | Ortalama birim maliyeti |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1 Ekim    | Başlangıç bakiyesi          | 0        | 0,00   | 0,00              |
| 8 Ekim        | 28 Eylül | Geriye dönük tarihli giriş          | 1        | 16,00  | 16,00             |
| 3 Ekim        | 3 Ekim    | Satınalma girişi           | 2        | 20,00  | 12,00             |
| 5 Ekim        | 5 Ekim    | Satış siparişi                | -1       | -10,00 | 13,00             |
| 7 Ekim        | 7 Ekim    | Satınalma faturası           |          | 2,00   | 14,00             |
| 8 Ekim        | 8 Ekim    | Hareketli ortalama yeniden değerleme |          | 4,00   | 16,00             |
|                  | 31 Ekim   | Toplam                      | 2        | 32,00  | 16,00             |

 

| **Not **                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Genel muhasebeyi stokla **Hareket saati sıralaması** seçeneğini kullanarak mutabık kılamazsınız. Raporun **Deftere nakil tarihi** seçeneği kullanılarak yazdırılması gereklidir. |




