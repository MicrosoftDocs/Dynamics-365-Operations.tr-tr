---
title: "Fiziksel ve mali güncellemeler"
description: "Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>Fiziksel ve mali güncellemeler

Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar. 

Stok hareketlerinin fiziksel olarak güncelleştirilen ve Microsoft Dynamics 365 işlemleri için de mali olarak güncelleştirilmiş. Bazı fiziksel ve mali hareket türleri stok miktarlarını artırırken, bazıları bu miktarlar azaltır.

## <a name="physical-increases"></a>Fiziksel artışlar
Bir fiziksel hareket nakledildiğinde, hareket kaydının durumu **Alındı** olur. Aşağıdaki hareketler fiziksel artış olarak kabul edilir:

-   Satınalma siparişi girişi
-   Satış siparişinin sevk irsaliyesi iadesi
-   Bir üretim emrinin tamamlandı olarak rapor edilmesi
-   Üretim emri malzeme çekme listesinde ürüne göre

## <a name="financial-increases"></a>Mali artışlar
Bir mali giriş hareketi nakledildiğinde, miktarı artıran hareket kaydının durumu **Satın alındı** olur. Aşağıdaki hareketler mali artış olarak kabul edilir:

-   Satıcı faturası
-   İade için satınalma siparişi faturası
-   Üretim emri maliyeti
-   Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi pozitif miktar stok günlükleri

## <a name="transactions-that-increase-quantity"></a>Miktarı artıran hareketler
Miktarı artıran hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir. Dynamics 365 işlemleri için her mali olarak izlenmekte olan her stok boyutu için bu işlemlerin maliyetini temel alan bir ortalama maliyet fiyatı hesaplar. Çalışan ortalama maliyet fiyatları hakkında daha fazla bilgi için [Çalışan ortalama maliyet fiyatı](running-average-cost-price.md) bölümüne bakın.

## <a name="transactions-that-decrease-quantity"></a>Miktarı azaltan hareketler
Miktarı azaltır bir hareketi deftere naklettiğinizde hesaplanan ortalama maliyet fiyatı dynamics 365 işlemler için kullanır, bu stok ile ilişkili stok modeli ne olursa olsun. Miktarı azaltan hareket kesinlikle nakledilmeden önce başka bir harekete işaretlenmemiş olmalıdır. Dynamics 365 işlemleri için fiziksel eldeki stokun negatif duruma gelirse, madde için tanımlanan Stok maliyeti kullanır **madde** sayfa. **Not:** Birden fazla saha içeren bir işlev etkinleştirilirse maliyet yerine bir saha için **Varsayılan sipariş ayarları** sayfasında tanımlanan envanter maliyeti kullanılacaktır.

## <a name="physical-issues-vs-financial-issues"></a>Fiziksel çıkışlar ile mali çıkışlar karşılaştırması
Bir fiziksel çıkış hareketi nakledildiğinde, hareket kaydının durumu **Kesinti yapıldı** olur. Aşağıdaki hareketler fiziksel çıkışlar olarak kabul edilir:

-   Üretim emri malzeme çekme listesi günlüğü
-   Satış siparişinin sevk irsaliyesi
-   Satınalma siparişinin sevk irsaliyesi iadesi

Bir finansal hareket nakledildiğinde, hareket kaydının durumu **Satılan** olur. Aşağıdaki hareketler mali çıkışlar olarak kabul edilir:

-   Bir üretim emrinin sonlandırılması
-   Satış siparişi faturası
-   Satıcı fatura iadesi
-   Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi negatif miktar stok günlükleri

Miktarı azaltan hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir. Bu nedenle, her bir maddeye atanan stok modeline dayalı olarak, çıkış hareketlerinin giriş hareketlerine kapatılması için stok kapanışı prosedürü uygulanmalıdır.


