---
title: Ödeme sıklıklarını ayarlama
description: Microsoft Dynamics 365 Human Resources, yıllık kazancı hesaplamak için ödeme sıklıklarını kullanır, maaşın, her bir ödeme periyodunu ödeyen ve sağlayıcılara yapılan sıklık ödemelerini tanımlayan kazanç prim tutarını belirler.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b786485ab53dcdb3b7e5ff02562f674a7f8e6eae
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092603"
---
# <a name="set-up-payment-frequencies"></a>Ödeme sıklıklarını ayarlama

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources, yıllık kazancı hesaplamak için ödeme sıklıklarını kullanır, maaşın, her bir ödeme periyodunu ödeyen ve sağlayıcılara yapılan sıklık ödemelerini tanımlayan kazanç prim tutarını belirler.

Kazanç ödeme sıklıklarını aylık, yarı aylık, iki haftalık, haftalık ve günlük ödeme sıklıkları arasında kazanç ödeme dönemlerini dönüştürmek için dönüştürme faktörlerini kullanın. Böylece şirketler, bir kazanç planındaki ödeme sıklıklarını arasında bağımlılıkları tanımlarlar.

Dönüştürme faktörleri alanları, ödeme sıklığından standart ödeme dönemlerine dönüştürme faktörünü tanımlar ve sistemin ödeme sıklıkları arasında hesaplama yapmasına olanak tanır. Dönüştürme çarpanı tutarı, bir çalışanın her ödeme sıklığının ödemesi gereken kazanç prim tutarını belirlemek için de kullanılır.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Ödeme sıklıkları**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Ödeme sıklığı | Benzersiz bir ödeme sıklığı adı. |
   | Tanım | Ödeme sıklığının açıklaması. |
   | Dönem | Kazanç sağlayıcısının ve çalışanın ödeme sıklığının en iyi şekilde eşleştiği uygun dönem. Dönem listesi standart ödeme dönemlerinden oluşur. |
   | Ödeme dönemi sayısı | Kazanç sağlayıcısının veya çalışanların ne kadar sıklıkla ödendiğini gösteren ödeme dönemlerinin sayısı. Bu tutar, çalışanın yıllık kazançının maaş tutarını hesaplamak için kullanılır. |
   | Yıllık dönüştürme faktörü | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/1 yıl) = 12 |
   | 6 aylık dönüştürme faktörü | Ödeme sıklığında, yarı yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yarı yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler / yılda 2 kez) = 6 |
   | 3 aylık dönüştürme faktörü | Ödeme sıklığında, üç aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için üç aylık dönüştürme faktörü: </br></br>(12 aylık ödemeler/4 çeyrek) = 3 |
   | Aylık dönüştürme faktörü | Ödeme sıklığında, aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için aylık dönüştürme faktörü: </br></br>(12 aylık ödemeler/12 ay) = 1 |
   | 15 günlük dönüştürme faktörü | Ödeme sıklığında, yarı aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yarı aylık dönüştürme faktörü: </br></br>(12 aylık ödemeler/24 (2x bir ay)) = .5 | 
   | İki haftalık dönüştürme faktörü | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/26 hafta) = 0,461538 |
   | Haftalık dönüştürme faktörü | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/52 hafta) = 0,230769 |
   | Günlük dönüştürme faktörü | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/365 gün) = 0,032877 |

4. **Kaydet**'i seçin. 
