---
title: Hareketli ortalama
description: Hareketli ortalama, stok çıkışlarındaki maliyetlerin satın alma maliyeti değiştiğinde değişmediği ortalama ilkesini temel alan kalıcı bir maliyetlendirme yöntemidir. Fark aktifleştirilir ve orantısal bir hesaplamaya dayanır. Kalan tutar gider gösterilir.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0957fee111ec1fd5bb66951126869cf46d88b36e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967495"
---
# <a name="moving-average"></a>Hareketli ortalama

[!include [banner](../includes/banner.md)]

Hareketli ortalama, stok çıkışlarındaki maliyetlerin satın alma maliyeti değiştiğinde değişmediği ortalama ilkesini temel alan kalıcı bir maliyetlendirme yöntemidir. Fark aktifleştirilir ve orantısal bir hesaplamaya dayanır. Kalan tutar gider gösterilir.

Hareketli ortalama kullandığınızda, stok kapatmaları ve stok işaretleme desteklenmez. Stok kapanışı stok model grubu olarak hareketli ortalamaya sahip ürünleri etkilemez ve hareketler arasında herhangi bir kapatma oluşturmaz.

Aşağıdakiler, maliyetlendirme yöntemi olarak hareketli ortalama maliyet kullanırkenki gerekliliklerdir.

1. **Madde model grupları** sayfasında, **Stok modeli** alanında **Hareketli ortalama** seçili olan bir madde model grubu belirleyin.

    > [!NOTE]
    > Varsayılan olarak, **Hareketli ortalama** seçiliyken, **Fiziksel stoku deftere naklet** ve **Mali stoku deftere naklet** alanları da seçilidir.

1. **Deftere nakil** sayfasında, hesapları **Hareketli ortalama için fiyat farkı** öğesine atayın. Maliyetin orantılı harcanması gerektiğinde, **Hareketli ortalama için fiyat farkı** hesabını kullanırsınız. Bu aşağıdaki iki senaryoda gerçekleşir:
    - Satınalma girişi ile satınalma faturası arasındaki bir maliyet farkı vardır, çünkü orijinal stok miktarı ile elde olan miktar arasında bir fark vardır.
    - Hareketler stoku negatiften sıfıra çeker ve hareket maliyeti ile geçerli hareketli ortalama maliyeti arasında fark vardır.

1. **Deftere nakil** sayfasında, **Stok** sekmesinde hesapları **Hareketli ortalama için maliyet yeniden değerlemesi** hesabına atayın. Bir ürün için hareketli ortalamayı yeni bir birim fiyata ayarlamak istediğinizde **Hareketli ortalama için maliyet yeniden değerleme** hesaplarını kullanırsınız.

1. **Serbest bırakılan ürünler** sayfasında, ürüne hareketli ortalama madde model grubu atayın.

    > [!NOTE]
    > Stok kapatma işlemi yalnızca muhasebe dönemini kapatır. Kendilerine bir madde model grubu olarak hareketli ortalama atanmış olan ürünleri etkilemez.

## <a name="convert-to-the-moving-average-costing-method"></a>Hareketli ortalamaya dönüştürme maliyetlendirme yöntemi

Ürünler, hareketli ortalama stok değerleme yöntemini kullanacak şekilde dönüştürülebilirler. Bu tür dönüştürme genellikle yıl sonunda, geçerli yılın son ayı kapatıldıktan sonra yapılır. Ürünün geçerli maliyetlendirme modeli kullanılarak yapılır. Stok maliyetlendirme yönteminizi, ortalama maliyete veya standart maliyete dayalı maliyetlendirme yönteminden hareketli ortalamaya dayalı bir yönteme değiştirebilirsiniz.

Maliyetlendirme yönteminizi standart maliyetlendirme yönteminden hareketli ortalama yöntemine değiştiriyorsanız, şu görevleri gerçekleştirmeniz gerekir:

1. Stok miktarlarını ve değerlerini 0'a (sıfır) indirmek için ayarlamalar yapın.
1. Stok değeri ve miktarı 0 (sıfır) iken, madde model grubunu hareketli ortalamaya değiştirin.
1. Miktar ve değeri yeniden stoka göre ayarlayın.

Stok maliyetlendirme yönteminizi hareketli ortalama yönteminden İlk giren ilk çıkar (FIFO) yöntemine, Son giren ilk çıkar (LIFO) yöntemine veya ağırlıklı ortalama yöntemine değiştiremezsiniz.

> [!NOTE]
> Standart maliyetten hareketli ağırlıklı ortalamaya dönüştürmek manuel bir işlemdir.

Aşağıdaki örnekler, hareketli ortalama maliyetlendirme yöntemini kullanmanın etkisini gösterir. Dört yapılandırma mevcuttur:

- Satınalma emri ve orantılı olarak harcanan maliyet farkı
- Hareketli ortalama ürün ve stok düzeltmesi
- Üretim ile hareketli ortalama
- Geriye dönük tarihli işlemli hareketli ortalama

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Satınalma emri ve orantılı olarak harcanan maliyet farkı

Hareketli ortalama ile, ürünün maliyeti satınalma girişi tarafından belirlenir. Satınalma faturası deftere nakledildiğinde maliyette satınalma girişi ile satınalma faturası arasında bir fark varsa, fark oransal olarak stoktaki geçerli ürünlere ayarlanır ve kalan miktar harcanır.

Bu örnekte, bir satınalma emri oluşturulur ve bir maliyete alınır ve satınalma faturası farklı bir maliyet ile nakledilir.

1. Miktar olarak 2, birim fiyatı olarak 10,00 şeklinde bir satınalma emri oluşturun.
1. Ürünün satınalma girişini oluşturun.
1. Miktar olarak 1, birim fiyatı olarak 10,00 şeklinde bir satış emri oluşturun.
1. Miktar olarak 2, birim fiyatı olarak 12,00 şeklinde bir satınalma faturası oluşturun.

Birim fiyatındaki fark olan 2,00, satınalma faturası nakledilirken Hareketli ortalama için fiyat farkı hesabına nakledilir. Bunun sebebi, iki ürünün 20,00 maliyetine satın alınmış olmasıdır. Ürünlerden biri 10,00 birim fiyatına satılmıştır. Satınalma faturası 12,00 birim fiyattan 2 adet miktarla deftere nakledildi. Ürünün birim fiyatı deftere 14,00'dan nakledilemez.

## <a name="moving-average-product-and-inventory-adjustment"></a>Hareketli ortalama ürün ve stok düzeltmesi

Bir ürünün hareketli ortalama maliyetini ayarlamanız gerekiyorsa, stok ayarlamalarına bugünün tarihi itibariyle izin verilir. Bir stok ayarlamasına bir ürünün hareketli ortalama maliyetini düzeltmek için eski bir tarih atamazsınız. Ardışık hareketler üzerinden maliyet akışınız olamaz.

Bu örnekte, bir ürün için hareketli ortalama maliyet ayarlanmaktadır.

1. Hareketli ortalama maliyetini ayarlamak istediğiniz ürünü seçin. 

 > [!NOTE]
 > **Hareketli ortalama için yeniden değerleme** sayfası, bir ürünün stokta olup olmadığını inceler. Seçilen ürünün deftere nakledilen miktarı 1, deftere nakledilen değeri 12,00, deftere nakledilen birim maliyeti 12,00 ve birim maliyeti 12,00'dir.
    
1. **Birim maliyeti** alanını 16,00 olarak güncelleyin. Sistem geri kalan alanları hesaplar.
1. Ayarlama deftere nakledilir.

> [!NOTE]
> Hareketli ortalama maliyetini yalnızca bugünün tarihi itibariyle ayarlayabilirsiniz.

**Fişe ait kapatmalar** sayfasında, Hareketli ortalama için maliyet yeniden değerleme hesabına 4,00'lık bir ayarlama nakledildiğini görebilirsiniz.

## <a name="moving-average-with-production"></a>Üretim ile hareketli ortalama

Hareketli ortalama, üretilen maddeleri destekler. Hareketli ortalamayı bir üretim ortamında kullanmayı planlıyorsanız, **Üretim kontrol parametreleri** sayfasındaki **Tahmini maliyet fiyatını kullan** kaydırıcısını seçin. Bu, fiili ürün reçetesi hesaplama maliyet fiyatı yerine tahmin sırasında hesaplanan maliyet fiyatının kullanılacağı anlamına gelir.

## <a name="moving-average-with-a-backdated-transaction"></a>Geriye dönük tarihli işlemli hareketli ortalama

Geçerli hareketli ortalama maliyete geriye dönük tarih atılmış hareketler atanır ve ürünün fiziksel miktarı güncellenir ama ürünün hareketli ortalama maliyeti etkilenmez. Bu hareketli ortalama örneğinde, bir hareketli ortalama ürünü için deftere geriye dönük tarihli bir hareket nakledilir.

1. Hareketli ortalama ürüne miktar olarak 1, maliyet olarak 20,00'lik bir stok ayarlaması oluşturun.
1. Ürünün stok hareket geçmişi aşağıdakine benzeyecektir:
    - 1'lik bir stok hareketi, 16,00'lık bir maliyet, 15 Ocak şeklinde bir deftere nakil tarihi ve 15 Ocak şeklinde bir hareket tarihi.
    - 1'lik bir stok ayarlaması, 20,00'lik bir maliyet, 1 Ocak şeklinde bir deftere nakil tarihi ve 15 Ocak şeklinde bir hareket tarihi.
1. Ayarlamayı deftere nakledin.

**Stok hareketleri** sayfasında, ürün için geçerli hareketli ortalama olarak harcanan 4,00'ın 16,00 olduğunu görebilirsiniz. Geçmişe nakledebilirsiniz ancak maliyetteki fark harcanır, böylelikle hareketli ortalama maliyet etkilenmez.

## <a name="negative-inventory-balances"></a>Negatif stok bakiyeleri

Hareketler, hareket sonrası yeni eldeki miktarın eksi, sıfır veya pozitif olmasına bağlı olarak farklı şekilde ele alınır.

### <a name="new-balance-is-negative-or-zero"></a>Yeni bakiye negatif veya sıfır

Eldeki yeni miktar negatif veya sıfır ise, hareket geçerli ortalama maliyette maliyetlendirilir. Satınalma fiyatıyla geçerli ortalama maliyetler arasında fark varsa, **Hareketli ortalama için fiyat farkı** hesabına nakledilir.

### <a name="new-balance-is-positive"></a>Yeni bakiye pozitif

Hareket sonrasında eldeki yeni miktar pozitifse, hareket iki parçaya bölünür ve aşağıdaki tabloda özetlendiği gibi farklı şekilde maliyetlendirilir.

| Parça | Tanım |
|---|---|
| Negatiften sıfıra kadar olan miktar | Stok, eldeki bakiyeyi negatiften sıfıra artıran giriş miktarının bu bölümü için hareket maliyeti yerine, maddenin geçerli hareketli ortalama maliyetini kullanır. Hareket maliyeti ile geçerli hareketli ortalama maliyet arasındaki fark **Hareketli ortalama için fiyat farkı** hesabına nakledilir. |
| Sıfırdan pozitife kadar olan miktar | Stok, eldeki bakiyeyi sıfırdan pozitife artıran giriş miktarının bu bölümü için hareket maliyetini kullanır.                                                  |

## <a name="inventory-value-report"></a>Stok değeri raporu

Bu hareketli ortalama örneğinde, ürüne yönelik geçerli hareketli ortalama hesaplamasını desteklemek için stok değeri raporu yazdırılır. Stok değeri raporu, bir ürüne yönelik hareketli ortalama maliyet hesaplamasını desteklemek için maliyetle birlikte hareketleri kronolojik sıra ile yazdırabilir. Rapor, ürün için hareketli ortalama maliyeti gösterir. **Stok değeri raporları** iletişim kutusundaki tarih aralığı, raporu sıralama ölçütünü seçmek için **Hareket saati** veya **Deftere nakil tarihi** değerini seçmenize imkan verir. **Deftere nakil tarihi** seçeneği, raporun geleneksel olarak nasıl yazdırılacağıdır. **Hareket saati** seçeneği, hareketin rapor edildiği ve ürün için hareketli ortalama maliyetin güncellendiği fiili tarihtir. Hareketli ortalama maliyet hesaplamasını zaman içinde görmek isterseniz Stok değeri raporunu **Hareket saati sıralaması** seçeneğini kullanarak yazdırabilirsiniz. Aşağıdaki tabloda, **Hareket saati sıralaması** seçeneği kullanıldığında rapor yazdırılan ürün için hareketler gösterilmektedir.

| Hareket saati | Tarih         | Hareket türü           | Miktar | Tutar | Ortalama birim maliyeti |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1 Ekim    | Başlangıç bakiyesi          | 0        | 0,00   | 0,00              |
| 8 Ekim        | 28 Eylül | Geriye dönük tarihli giriş          | 1        | 16,00  | 16,00             |
| 3 Ekim        | 3 Ekim    | Satınalma girişi           | 2        | 20,00  | 12,00             |
| 5 Ekim        | 5 Ekim    | Satış siparişi                | -1       | -10,00 | 13,00             |
| 7 Ekim        | 7 Ekim    | Satınalma faturası           |          | 2,00   | 14,00             |
| 8 Ekim        | 8 Ekim    | Hareketli ortalama yeniden değerleme |          | 4.00   | 16.00             |
|                  | 31 Ekim   | Toplam                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Genel muhasebeyi stokla **Hareket saati sıralaması** seçeneğini kullanarak mutabık kılamazsınız. Raporun **Deftere nakil tarihi** seçeneği kullanılarak yazdırılması gereklidir.
