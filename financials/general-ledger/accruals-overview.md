---
title: "Tahakkuklara genel bakış"
description: "Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Tahakkuklara genel bakış

Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir.

Tahakkuklar, tahakkuk muhasebesinde ödeme alındığında değil de kazanılan dönemde elde edilen geliri takip etmek ve ödeme yapıldığında değil de meydana geldiğinde anda giderleri (maliyetleri) takip etmek için kullanılır.

## <a name="accrual-schemes"></a>Tahakkuk planları
Tahakkuk planları, ertelenmiş gelir ve maliyetleri oluşturmak için kullanılır ve aynı tahakkuk planı hem gelir hem maliyetler için kullanılabilir. Genel muhasebe tahakkukları, bir günlük satırının maliyetleri ve gelirlerini uygun dönemlerde tanınacak şekilde yeniden dağıtır. **Tahakkuk planı** sayfasında, tahakkuk planı uygulandığında kullanılacak borç ve alacak hesaplarını belirtirsiniz.

-   **Borç** – Tanımladığınız ana hesap, günlük fişinde borç ana hesabının yerini alacaktır. Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.
-   **Alacak** – tanımladığınız ana hesap, günlük fişinde alacak ana hesabının yerini alacaktır. Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.

Hangi hesapların kullanılacağını belirledikten sonra tahakkuk hareketleri oluşturulduğunda fiş numarasının nasıl oluşturulacağını belirtebilirsiniz. Hareketlerin ne sıklıkla gerçekleştirileceğini, hareketlerin gerçekleşme sayısını ve hareketlerin ne zaman nakledileceğini de belirleyebilirsiniz. Tahakkuk planı oluşturduktan sonra Genel muhasebe tahakkukları işlevini kullanarak bu planı bazı günlüklerde kullanabilirsiniz.

## <a name="ledger-accruals"></a>Genel muhasebe tahakkukları
Bir günlük girdiğinizde **İşlevler** menüsündeki **Genel muhasebe tahakkukları** öğesini tıklayabilirsiniz. Ardından, tahakkuk planını seçtiğinizde, günlükteki taban tutarını tahakkuk planında belirlendiği şekilde döneme dağılmış şekilde görürsünüz. Örneğin, bir çalışanın sigorta Ocak Ayındaki tüm yıl için ödeme ve 12.000 tutar ise, o gider her ay görmelidir. Başlangıç tarihi seçebilirsiniz. Tahakkuk eden tutarın hesaba mı, yoksa mahsup hesaba mı dayalı olacağını da belirleyebilirsiniz. Seçimlerinizi yaptıktan sonra'ı **hareketleri** tahakkuk düzenini temel alarak oluşturulan tüm hareketleri görüntülemek için. Örneğin, sigorta gideri 12.000 yıl boyunca yayılır, her ay için 1.000 görürsünüz. Günlüğü deftere naklettikten sonra hareketleri kullanarak görüntüleyebilirsiniz **fiş hareketleri** sorgulama sayfası. (Örneğin, satış siparişi veya satınalma siparişi faturası söz konusu olduğunda) tahakkuk düzeni uygulanamıyor peşinat tutarı Alacak ve Borç gider tutarı. Tahakkuk planını uygularken **Mahsup** seçimini yapabilirsiniz.


