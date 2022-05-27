---
title: Fiziksel ve mali güncellemeler
description: Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc8ffb87f6fcb9836d734dbfb4d962be4fa585a4
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670426"
---
# <a name="physical-and-financial-updates"></a>Fiziksel ve mali güncellemeler

[!include [banner](../includes/banner.md)]

Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar. 

Stok hareketleri, Dynamics 365 Supply Chain Management uygulamasında fiziksel olarak ve mali olarak güncellenebilir. Bazı fiziksel ve mali hareket türleri stok miktarlarını artırırken, bazıları bu miktarlar azaltır.

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
Miktarı artıran hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir. Hesaplanan cari ortalama maliyet fiyat, finansal olarak takip edilen her bir stok boyutu için bu hareketlerin her birinin maliyetine dayanır. Çalışan ortalama maliyet fiyatları hakkında daha fazla bilgi için [Çalışan ortalama maliyet fiyatı](running-average-cost-price.md) bölümüne bakın.

## <a name="transactions-that-decrease-quantity"></a>Miktarı azaltan hareketler
Miktarı azaltan bir hareket nakledildiğinde bu stokla ilişkili olan stok modeline bakılmaksızın, hesaplanan cari ortalama maliyet fiyatı kullanılır. Miktarı azaltan hareket kesinlikle nakledilmeden önce başka bir harekete işaretlenmemiş olmalıdır. Eldeki fiziksel stokun negatif hale gelmesi durumunda **Madde** sayfasında tanımlanan stok maliyeti kullanılır. 

> [!NOTE]
> Birden fazla saha içeren bir işlev etkinleştirilirse bunun yerine bu maliyet, bir saha için **Varsayılan sipariş ayarları** sayfasında tanımlanan stok maliyeti olur.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]