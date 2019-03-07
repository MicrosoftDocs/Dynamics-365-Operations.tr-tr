---
title: Tahakkuklara genel bakış
description: Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23c6a3402e4bc4a22d764017ba56554001300a67
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "339706"
---
# <a name="accruals-overview"></a>Tahakkuklara genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir.

Tahakkuklar, tahakkuk muhasebesinde ödeme alındığında değil de kazanılan dönemde elde edilen geliri takip etmek ve ödeme yapıldığında değil de meydana geldiğinde anda giderleri (maliyetleri) takip etmek için kullanılır.

## <a name="accrual-schemes"></a>Tahakkuk planları
Tahakkuk planları, ertelenmiş gelir ve maliyetleri oluşturmak için kullanılır ve aynı tahakkuk planı hem gelir hem maliyetler için kullanılabilir. Genel muhasebe tahakkukları, bir günlük satırının maliyetleri ve gelirlerini uygun dönemlerde tanınacak şekilde yeniden dağıtır. **Tahakkuk planı** sayfasında, tahakkuk planı uygulandığında kullanılacak borç ve alacak hesaplarını belirtirsiniz.

-   **Borç** – Tanımladığınız ana hesap, günlük fişinde borç ana hesabının yerini alacaktır. Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.
-   **Alacak** – tanımladığınız ana hesap, günlük fişinde alacak ana hesabının yerini alacaktır. Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.

Hangi hesapların kullanılacağını belirledikten sonra tahakkuk hareketleri oluşturulduğunda fiş numarasının nasıl oluşturulacağını belirtebilirsiniz. Hareketlerin ne sıklıkla gerçekleştirileceğini, hareketlerin gerçekleşme sayısını ve hareketlerin ne zaman nakledileceğini de belirleyebilirsiniz. Tahakkuk planı oluşturduktan sonra Genel muhasebe tahakkukları işlevini kullanarak bu planı bazı günlüklerde kullanabilirsiniz.

## <a name="ledger-accruals"></a>Genel muhasebe tahakkukları
Bir günlük girdiğinizde **İşlevler** menüsündeki **Genel muhasebe tahakkukları** öğesini tıklayabilirsiniz. Ardından, tahakkuk planını seçtiğinizde, günlükteki taban tutarını tahakkuk planında belirlendiği şekilde döneme dağılmış şekilde görürsünüz. Örneğin, bir çalışanın tüm yıla ait sigortasını Ocak ayındaki ödüyorsanız ve tutar 12.000 ise, bu gideri her ay kabul etmeniz gerekir. Başlangıç tarihini seçebilirsiniz. Tahakkuk eden tutarın hesaba mı, yoksa mahsup hesaba mı dayalı olacağını da belirleyebilirsiniz. Bu seçimleri yaptıktan sonra tahakkuk düzenine dayanarak oluşturulan tüm hareketleri görmek için **Hareketler**'i tıklatın. Örneğin, 12.000 tutarındaki sigorta masraflarını yıla yayarsanız, her ay 1.000 görürsünüz. Günlüğü deftere naklettikten sonra, **Fiş hareketleri** sorgulama sayfasını kullanarak hareketleri görebilirsiniz. Bir tahakkuk düzeni uygulanamıyorsa (örneğin, bir satış siparişi faturası veya satınalma emri faturası söz konusuysa), önceden ödenmiş tutarı alacaklandırabilir ve gider tutarını borçlandırabilirsiniz. Tahakkuk planını uygularken **Mahsup** seçimini yapabilirsiniz.


Daha fazla bilgi için bkz. [Tahakkuk planları oluşturma](tasks/create-accrual-schemes.md) ve [Genel muhasebe tahakkuk hareketleri oluşturma](tasks/create-ledger-accrual-transactions.md).
