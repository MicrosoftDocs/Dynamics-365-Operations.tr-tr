---
title: Toplu işle izlenen maddeler için geliştirilmiş işleme
description: Bu konuda, ekstrenin deftere nakil işlemi sırasında toplu olarak izlenen maddeler için toplu işlerin işlenmesine yönelik yapılan geliştirmeler açıklanmaktadır.
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799721"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Toplu işle izlenen maddeler için geliştirilmiş işleme


[!include [banner](includes/banner.md)]


Satış Noktası'nda (POS), toplu iş numaraları toplu olarak izlenen maddeler için satış sırasında yakalanamaz. Ancak, belirli yapılandırmalarda satışlar merkezde müşteri siparişleri veya ekstre deftere nakil işlemi aracılığıyla deftere aktarıldığında, Microsoft Dynamics sistemi toplu izlenen maddeler için geçerli toplu iş numaraları olmasını bekler ve bu numaralar faturalama işlemi sırasında kullanılır.

Ürünler için geçerli toplu iş numaraları varsa, müşteri siparişi faturalama işlemi ve ekstre deftere nakil işleminden gerçekleştirilen satış siparişi faturalama işlemi bu numaraları kullanır. Aksi takdirde, müşteri siparişi faturalama işlemi deftere nakledilemez ve POS kullanıcısı hata mesajı alır. Ekstre deftere nakil işlemi hata durumuna geçer. Bu hata durumu, ürünler için negatif stok etkinleştirildiğinde de oluşur.

Retail sürüm 10.0.4 ve sonraki sürümlerde yapılan geliştirmeler, toplu işle izlenen maddeler için negatif stok etkinleştirildiğinde, stoğun 0 (sıfır) olması veya toplu iş numarasının kullanılabilir olmaması durumunda müşteri siparişi faturalama ve ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama işleminin engellenmemesini sağlamaya yardımcı olur. Yeni işlev, toplu iş numaraları olmadığında satış satırları için varsayılan bir toplu iş kodu kullanır.

Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlamak için **Commerce parametreleri** sayfasında bulunan **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlamak üzere **Commerce parametreleri** sayfasında bulunan **Deftere nakil** sekmesindeki **Stok güncelleştirmesi** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

> [!NOTE]
> Bu işlev yalnızca, belirli mağaza ambarı ve maddeleri için gelişmiş ambarlama etkin olduğunda kullanılabilir. Sonraki bir sürümde, işlev gelişmiş ambar yönetimi kullanılmayan senaryolar için de desteklenecektir.

> [!NOTE]
> Gelişmiş olmayan ambar yönetimi senaryoları için ekstre deftere nakledilirken, toplu işle izlenen maddelerin gelişmiş şekilde işlenmesiyle ilgili destek Retail 10.0.5 sürümünde kullanıma sunuldu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]