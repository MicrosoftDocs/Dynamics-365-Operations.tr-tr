---
title: Periyodik alacak yönetimi görevleri
description: Bu konu, müşteriler için kredi limitlerini yönetme sürecinin gerekli bir parçası olan periyodik görevleri açıklamaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: df3b0b239fe542eab80fa92057248328d3f5188f
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015433"
---
# <a name="periodic-credit-management-tasks"></a>Periyodik alacak yönetimi görevleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, müşteriler için kredi limitlerini yönetme sürecinin gerekli bir parçası olan periyodik görevleri açıklamaktadır.

## <a name="update-risk-scores"></a>Risk puanlarını güncelleştir

İşler gelişip koşullar değişince, belirli bir müşteriyle ilgili kredi riskleri de değişebilir. Müşterileriniz için uygun kredi limitlerini korumaya yardımcı olmak amacıyla, her risk puanı için ölçütleri düzenli olarak gözden geçirmeniz ve her müşteri için puanları güncelleştirmeniz gerekir. Aşağıdaki puanları **Risk puanlarını güncelleştir** sayfasını (**Alacak ve tahsilatlar \> Periyodik görevler \> Kredi yönetimi \> Riski puanlarını güncelleştir**) kullanarak güncelleştirebilirsiniz. Ayrıca tüm kullanıcı tanımlı hesaplamalar da işlenir.

- **Ortalama ödeme gün sayısı** – Bu puan, bir müşterinin ödeme için beklettiği ortalama gün sayısıdır.
- **Müşterilik başlangıç tarihi** – Bu puan, bir müşterinin kuruluşunuzun müşterisi olduğu yıl sayısıdır.
- **Sektöre giriş tarihi** Bu puan, müşterinin sektörde bulunduğu yıl sayısıdır. Bu puan, **Müşteriler** sayfasındaki **İş başlangıcı** alanının değerini kullanır.
- **Bekleyen satış gün sayısı** – Bu puan, önceki 12 aylık dönemdeki alacak hesapları bakiyesine, satış gelirine ve gün sayısına dayanır.
- **Ortalama bakiye** – Bu puan, önceki 12 aylık dönem için alacak hesapları bakiyesine dayanır.
- **Kredi yönetimi grubu**, **Hesap durumu** ve **Ülke** – Bu puanlar, müşteriden gelen bilgileri kullanır.

## <a name="update-customer-balance-statistics"></a>Müşteri bakiye istatistiklerini güncelleştirme

**Bakiye istatistikleri sorgusu** sayfasında gösterilen bakiye istatistiklerinin hesaplamasını güncelleştirmek için **Müşteri bakiyesi istatistiklerini güncelleştir** işlemini çalıştırabilirsiniz. Bu bilgiler, risk puanlarını ve **Müşteri** sayfasındaki kredi istatistikleri bilgi kutularında gösterilen değerleri hesaplamak için kullanılır.

İşlemi çalıştırdığınızda, tek bir müşteriyle ilgili müşteri bakiyesi istatistiklerini güncelleştirir. İşlemi birden fazla müşteri için yapmak üzere bir toplu iş ayarlamak için, **Bakiye istatistiklerini hesapla** sayfasını (**Kredi yönetimi \> Periyodik görevler \> Bakiye istatistiklerini hesapla**) kullanabilirsiniz.
