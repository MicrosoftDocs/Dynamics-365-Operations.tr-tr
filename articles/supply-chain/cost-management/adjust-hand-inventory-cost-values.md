---
title: "Eldeki stokun maliyet değerlerini ayarlama"
description: "Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 21942f7aa57d21f70e3014051c42328164b750a3
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a>Eldeki stokun maliyet değerlerini ayarlama

[!include[banner](../includes/banner.md)]

Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın.

Bir envanter kapatma işlemi yürütüldükten sonra hazır envanter miktarlarının maliyet değerini ayarlamak için **Hazır envanterin ayarlanması** sayfasını kullanabilirsiniz. **Not:** **Hazır envanterin ayarlanması** sayfasını açmak için **Kapatma ve ayarlama** sayfasından bir tamamlanan envanter kapatma işlemi kaydı seçin ve **Ayar** &gt; **Hazır öğelerini** tıklayın. **Örnek:** Şubat ayına ait şu işlemler bulunuyor olsun:

-   1 Şubat: 10.00 USD maliyetinde 2 adet için bir envanter finansal alındı
-   5 Şubat: Maliyeti 13.00 USD olan 1 adet için bir envanter finansal alındı
-   19 Şubat:Ortalama işletme maliyeti 11.00 olan 1 adet için bir envanter finansal işlemi

Bu madde ilk giren ilk çıkar (FIFO) stok modeliyle ayarlanmıştır ve stok kapanışı 28 Şubat tarihinde gerçekleştirilmiştir. 11,00 USD tutarındaki Mali çıkış hareketi 1 Şubat tarihli mali girişine karşılık eşlenerek kapatılmıştır ve 1,00 USD tutarında bir düzeltme yapılacaktır. Bu durumda aşağıdaki stok girişleri açık stok miktarları içerir:

-   1 Şubat: 10.00 USD maliyetli 1 adet
-   5 Şubat: 13.00 USD maliyetli 1 adet

Bu iki maddenin maliyetini 15,00 USD olarak ayarlamak için eldeki açık miktarları son stok kapanış dönemi itibariyle ayarlamak için eldeki stoku düzeltme seçeneğini kullanın. **Not:** Hazır ayarlama işleminin nakil tarihi, son envanter kapatma tarihi olacaktır. Bu tarih değiştirilemez.

