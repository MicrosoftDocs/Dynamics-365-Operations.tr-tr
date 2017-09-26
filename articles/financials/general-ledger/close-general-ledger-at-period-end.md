---
title: "Genel muhasebeyi dönemi sonunda kapatma"
description: "Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: bcf58b0ca995883bc466eec66a3d75c73c0be79e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/01/2017

---

# <a name="close-the-general-ledger-at-period-end"></a>Genel muhasebeyi dönemi sonunda kapatma

[!include[banner](../includes/banner.md)]


Bu konu, genellikle bir dönem kapanışı için genel muhasebe gerçekleştirirken tamamlanmış görevleri açıklar. 

Genel muhasebede bir dönem veya bir yıl için kapatma prosedürlerini tamamlayabilirsiniz. Kapanış işlemleri, sistemi yeni bir dönem için hazırlar. Sistemi yeni yıl için hazırlamak için mutlaka yıl sonu kapanış işlemini yürütmeniz gerekir. Her kuruluşun farklı işlemleri ve bir dönemin sonu için gerçekleştirdiği adımları vardır. Dönem sonu için bazı isteğe bağlı adımlar şunlardır:

-   Borç hesapları, Alacak hesapları ve Stok gibi tüm diğer modüler için tüm görevleri tamamlayın.
-   Tüm günlüklerin nakledildiğini doğrulayın.
-   Gerçekleşmemiş kazanç veya kayıp tutarları üretmek için yabancı para biriminde yeniden değerleme çalıştırın.
-   Her bir genel muhasebe hesabı için hareketleri kapatın.
-   Gerekli tahsisatları işleyin.
-   Dönem sonu ayarlamaları el ile nakledin.
-   Hareketleri günlüğe aktarın ve **Genel muhasebe günlüğü** raporunu gözden geçirin.
-   Bir konsolidasyon şirketini veya Mali raporlamayı kullanarak bir konsolidasyon gerçekleştirin.
-   Mali raporlamayı kullanarak dönem sonu mali beyanları oluşturun.
-   Genel muhasebe dönemlerini **Beklemede** konumuna ayarlayın, böylece daha fazla nakil oluşmaz. Ayrıca, daha iyi bir kontrol için, dönem sonu faaliyetleri gerçekleşirken bir dönemi bir özel kullanıcı grubuyla sınırlayabilirsiniz. Kapatılmış bir dönemi yeniden açamayacağınızdan dönemleri **Kalıcı olarak kapalı** olarak ayarlamak iyi bir fikirdir.

Mali dönem kapanış çalışma alanı, gerekli çeşitli dönem sonu işlemlerini organize etmek ve izlemek için kullanabilir. 


Daha fazla bilgi için aşağıdaki konulara bakın:
- [Mali dönem kapatma çalışma alanı](financial-period-close-workspace.md) 
- [Yıl sonu kapanışı](Year-end-close.md)  
- [Toplu mali dönem kapatma](tasks/mass-financial-period-close.md)





