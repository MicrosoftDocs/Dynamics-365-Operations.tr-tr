---
title: Eldeki stokun maliyet değerlerini ayarlama
description: Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963850"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Eldeki stokun maliyet değerlerini ayarlama

[!include [banner](../includes/banner.md)]

Bir stok kapanışı yürütüldükten sonra hazır stok miktarlarının maliyet değerini ayarlamak için, Eldeki stokların düzeltilmesi sayfasını kullanın.

Bir envanter kapatma işlemi yürütüldükten sonra hazır envanter miktarlarının maliyet değerini ayarlamak için **Hazır envanterin ayarlanması** sayfasını kullanabilirsiniz. **Not:** **Eldeki stokların düzeltilmesi** sayfasını açmak için **Kapanış ve düzeltme** sayfasından bir tamamlanan envanter kapatma işlemi kaydı seçin ve **Ayar** &gt; **Eldeki** seçeneğini tıklayın. **Örnek:** Şubat ayına ait şu işlemler bulunuyor olsun:

-   1 Şubat: 10.00 USD maliyetinde 2 adet için bir envanter finansal alındı
-   5 Şubat: Maliyeti 13.00 USD olan 1 adet için bir envanter finansal alındı
-   19 Şubat:Ortalama işletme maliyeti 11.00 olan 1 adet için bir envanter finansal işlemi

Bu madde ilk giren ilk çıkar (FIFO) stok modeliyle ayarlanmıştır ve stok kapanışı 28 Şubat tarihinde gerçekleştirilmiştir. 11,00 USD tutarındaki Mali çıkış hareketi 1 Şubat tarihli mali girişine karşılık eşlenerek kapatılmıştır ve 1,00 USD tutarında bir düzeltme yapılacaktır. Bu durumda aşağıdaki stok girişleri açık stok miktarları içerir:

-   1 Şubat: 10.00 USD maliyetli 1 adet
-   5 Şubat: 13.00 USD maliyetli 1 adet

Bu iki maddenin maliyetini 15,00 USD olarak ayarlamak için eldeki açık miktarları son stok kapanış dönemi itibariyle ayarlamak için eldeki stoku düzeltme seçeneğini kullanın. **Not:** Hazır ayarlama işleminin nakil tarihi, son envanter kapatma tarihi olacaktır. Bu tarih değiştirilemez.
