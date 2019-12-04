---
title: Toplu işle izlenen maddeler için geliştirilmiş işleme
description: Bu konu, Perakende ekstresi deftere nakil işlemi sırasında toplu olarak izlenen maddeler için toplu işlerin işlenmesine yönelik yapılan geliştirmeleri açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770175"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Toplu işle izlenen maddeler için geliştirilmiş işleme


[!include [banner](includes/banner.md)]


Retail Satış Noktasında (POS), toplu iş numaraları toplu olarak izlenen maddeler için satış sırasında yakalanamaz. Ancak, belirli yapılandırmalarda satışlar merkezde müşteri siparişleri veya ekstre deftere nakil işlemi aracılığıyla deftere aktarıldığında, Microsoft Dynamics sistemi toplu izlenen maddeler için geçerli toplu iş numaraları olmasını bekler ve bu numaralar faturalama işlemi sırasında kullanılır.

Ürünler için geçerli toplu iş numaraları varsa, müşteri siparişi faturalama işlemi ve ekstre deftere nakil işleminden gerçekleştirilen satış siparişi faturalama işlemi bu numaraları kullanır. Aksi takdirde, müşteri siparişi faturalama işlemi deftere nakledilemez ve POS kullanıcısı hata mesajı alır. Ekstre deftere nakil işlemi hata durumuna geçer. Bu hata durumu, ürünler için negatif stok etkinleştirildiğinde de oluşur.

Retail sürüm 10.0.4 ve sonraki sürümlerde yapılan geliştirmeler, toplu işle izlenen maddeler için negatif stok etkinleştirildiğinde, stoğun 0 (sıfır) olması veya toplu iş numarasının kullanılabilir olmaması durumunda müşteri siparişi faturalama ve ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama işleminin engellenmemesini sağlamaya yardımcı olur. Yeni işlev, toplu iş numaraları olmadığında satış satırları için varsayılan bir toplu iş kodu kullanır.

Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlamak için **Perakende parametreleri** sayfasında bulunan **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlamak üzere **Perakende parametreleri** sayfasında bulunan **Deftere nakil** sekmesindeki **Stok güncelleştirmesi** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

> [!NOTE]
> Bu işlev yalnızca, belirli mağaza ambarı ve maddeleri için gelişmiş ambarlama etkin olduğunda kullanılabilir. Sonraki bir sürümde, işlev gelişmiş ambar yönetimi kullanılmayan senaryolar için de desteklenecektir.

> [!NOTE]
> Gelişmiş olmayan ambar yönetimi senaryoları için ekstre deftere nakledilirken, toplu işle izlenen maddelerin gelişmiş şekilde işlenmesiyle ilgili destek Retail 10.0.5 sürümünde kullanıma sunuldu.
