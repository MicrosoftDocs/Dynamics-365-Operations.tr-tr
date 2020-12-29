---
title: Üretim farklılıklarının ortak kaynakları
description: Bu makale, üretim farkı türlerinin çeşitli kaynaklarını açıklamaktadır.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc310f1d5e1f99a320b803f68395d0926d39780b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439500"
---
# <a name="common-sources-of-production-variances"></a>Üretim farklılıklarının ortak kaynakları

[!include [banner](../includes/banner.md)]

Bu makale, üretim farkı türlerinin çeşitli kaynaklarını açıklamaktadır. 

Burada bazı tipik **lot boyutu** farkı kaynakları yer almaktadır:

-   Üretim emrindeki sağlam ürün miktarı, standart maliyet hesaplamasında kullanılan hesaplama miktarından farklıdır. Miktar, sabit maliyetlerin itfası için temel oluşturur.
-   Üretim emrindeki sabit maliyetlerin değeri standart maliyet hesaplamasında kullanılan sabit maliyetlerden farklıdır. Üretim emrindeki sabit maliyetler çeşitli nedenlerle farklı olabilir. Örneğin, sabit maliyetler aşağıdaki etkenleri yansıtabilir:
    -   Üretim ürün reçetesi (BOM) veya rota ile ilgili el ile yapılan değişiklikler
    -   Üretim emrini oluştururken farklı ürün reçetesi sürümü veya rota sürümü seçmeniz
    -   Maddeye atanmış ürün reçetesi sürümü veya rota sürümü ile ilgili planlanmış mühendislik değişiklikleri

Burada bazı tipik **üretim fiyatı** farkı kaynakları yer almaktadır:

-   Rota belirleme operasyonu tarafından bildirilen tüketime yönelik maliyet kategorisi (ve maliyet kategorisi fiyatı) standart maliyet hesaplamasında kullanılan maliyet kategorisinden farklıdır.
-   Maliyet kategorisi fiyatının etkin maliyeti standart maliyet hesaplamasında kullanılan maliyet kategorisi fiyatından farklıdır.

Burada bazı tipik **üretim miktarı** farkı kaynakları yer almaktadır:

-   Bir bileşen malzemesi çıkışınız fazla veya az.
-   Rota işlemi için fazla veya az zaman raporladınız.
-   Siparişin miktarına göre ana madde için mal miktarını fazla veya az aldınız. Ancak, üretim emri için sipariş miktarına göre bileşenleri ve rapor işlemlerini tam olarak çıkış yaptınız.

Burada bazı tipik **üretim yedekleme** farkı kaynakları yer almaktadır:

-   Üretim ürün reçetesinde bulunmayan bir malzeme bileşeni çıkışı yaptınız.
-   Üretim ürün reçetesine el ile bir bileşen eklediniz ve bu bileşeni tüketildi olarak raporladınız.
-   Bir maddeyi tüketildi olarak raporladınız ancak üretim ürün reçetesine el ile eklemediniz.
-   Bir işlemi üretim rotasına el il eklediniz ve işlemi tüketildi olarak raporladınız.
-   Üretim emrini oluşturduğunuzda, standart maliyet hesaplamasında kullanılan ürün reçetesi sürümünden farklı bir ürün reçetesi sürümü seçtiniz.
-   Üretim emrini oluşturduğunuzda, standart maliyet hesaplamasında kullanılan rota sürümünden farklı bir rota sürümü seçtiniz.




