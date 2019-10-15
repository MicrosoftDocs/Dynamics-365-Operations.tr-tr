---
title: Toplu işle izlenen maddelerin işlenmesi geliştirildi
description: Bu konu, Perakende ekstresi deftere nakil işlemi sırasında toplu olarak izlenen maddeler için toplu işlerin işlenmesine yönelik yapılan geliştirmeleri açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
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
ms.openlocfilehash: 35823efa2844898d3eecbf91624b3e37d308b63c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025806"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Toplu işle izlenen maddelerin işlenmesi geliştirildi

Retail Satış Noktasında (POS), toplu iş numaraları toplu olarak izlenen maddeler için satış sırasında yakalanamaz. Ancak, belirli yapılandırmalarda satışlar merkezde müşteri siparişleri veya ekstre deftere nakil işlemi aracılığıyla deftere aktarıldığında, Microsoft Dynamics sistemi toplu izlenen maddeler için geçerli toplu iş numaraları olmasını bekler ve bu numaralar faturalama işlemi sırasında kullanılır.

Ürünler için geçerli toplu iş numaraları varsa, müşteri siparişi faturalama işlemi ve ekstre deftere nakil işleminden gerçekleştirilen satış siparişi faturalama işlemi bu numaraları kullanır. Aksi takdirde, müşteri siparişi faturalama işlemi deftere nakledilemez ve POS kullanıcısı hata mesajı alır. Ekstre deftere nakil işlemi hata durumuna geçer. Bu hata durumu, ürünler için negatif stok etkinleştirildiğinde de oluşur.

Retail sürüm 10.0.4 ve sonraki sürümlerde yapılan geliştirmeler, toplu işle izlenen maddeler için negatif stok etkinleştirildiğinde, stoğun 0 (sıfır) olması veya toplu iş numarasının kullanılabilir olmaması durumunda müşteri siparişi faturalama ve ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama işleminin engellenmemesini sağlamaya yardımcı olur. Yeni işlev, toplu iş numaraları olmadığında satış satırları için varsayılan bir toplu iş kodu kullanır.

Müşteri siparişleri için kullanılan varsayılan toplu iş kodunu tanımlamak için **Perakende parametreleri** sayfasında bulunan **Müşteri siparişleri** sekmesindeki **Sipariş** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

Ekstre deftere nakil işlemi aracılığıyla satış siparişi faturalama için kullanılan varsayılan toplu iş kodunu tanımlamak üzere **Perakende parametreleri** sayfasında bulunan **Deftere nakil** sekmesindeki **Stok güncelleştirmesi** hızlı sekmesinde **Varsayılan toplu iş kodu** alanını ayarlayın.

> [!NOTE]
> Bu işlev yalnızca, belirli mağaza ambarı ve maddeleri için gelişmiş ambarlama etkin olduğunda kullanılabilir. Sonraki bir sürümde, işlem gelişmiş ambar yönetimi kullanılmayan senaryolar için de desteklenecektir.
