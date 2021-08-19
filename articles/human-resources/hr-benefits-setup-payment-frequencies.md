---
title: Ödeme sıklıklarını ayarlama
description: Microsoft Dynamics 365 Human Resources yıllık kazancı hesaplamak, bir çalışanın her bir ödeme döneminde ödediği kazanç prim tutarını ve sağlayıcılara ne sıklıkla ödeme yapılacağını belirlemek için ödeme sıklıklarını kullanır.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 738df6a31ec8e9f50259461cd7bbf30bd5c2b73c6f8a23ffacba53ab261a80ed
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732765"
---
# <a name="set-up-payment-frequencies"></a>Ödeme sıklıklarını ayarlama

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources yıllık kazancı hesaplamak, bir çalışanın her bir ödeme döneminde ödediği kazanç prim tutarını ve sağlayıcılara ne sıklıkla ödeme yapılacağını belirlemek için ödeme sıklıklarını kullanır.

Kazanç ödeme sıklıklarını aylık, yarı aylık, iki haftalık, haftalık ve günlük ödeme sıklıkları arasında kazanç ödeme dönemlerini dönüştürmek için dönüştürme faktörlerini kullanın. Böylece şirketler, bir kazanç planındaki ödeme sıklıklarını arasında bağımlılıkları tanımlarlar.

Dönüştürme faktörleri alanları, ödeme sıklığından standart ödeme dönemlerine dönüştürme faktörünü tanımlar ve sistemin ödeme sıklıkları arasında hesaplama yapmasına olanak tanır. Dönüştürme çarpanı tutarı, bir çalışanın her ödeme sıklığında ödemesi gereken kazanç prim tutarını da belirler.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Ödeme sıklıkları**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Ödeme sıklığı** | Benzersiz bir ödeme sıklığı adı. |
   | **Tanım** | Ödeme sıklığının açıklaması. |
   | **Dönem** | Kazanç sağlayıcısının ve çalışanın ödeme sıklığının en iyi şekilde eşleştiği uygun dönem. Dönem listesi standart ödeme dönemlerinden oluşur. |
   | **Ödeme dönemi sayısı** | Kazanç sağlayıcısının veya çalışanların ne kadar sıklıkla ödendiğini gösteren ödeme dönemlerinin sayısı. Bu tutar, çalışanın yıllık kazançının maaş tutarını hesaplamak için kullanılır. |
   | **Yıllık dönüştürme faktörü** | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/1 yıl) = 12 |
   | **6 aylık dönüştürme faktörü** | Ödeme sıklığında, yarı yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yarı yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler / yılda 2 kez) = 6 |
   | **3 aylık dönüştürme faktörü** | Ödeme sıklığında, üç aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için üç aylık dönüştürme faktörü: </br></br>(12 aylık ödemeler/4 çeyrek) = 3 |
   | **Aylık dönüştürme faktörü** | Ödeme sıklığında, aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için aylık dönüştürme faktörü: </br></br>(12 aylık ödemeler/12 ay) = 1 |
   | **15 günlük dönüştürme faktörü** | Ödeme sıklığında, yarı aylık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yarı aylık dönüştürme faktörü: </br></br>(12 aylık ödeme / 24 (2x bir ay)) = 0,5 | 
   | **İki haftalık dönüştürme faktörü** | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/26 hafta) = 0,461538 |
   | **Haftalık dönüştürme faktörü** | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/52 hafta) = 0,230769 |
   | **Günlük dönüştürme faktörü** | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödemeler/365 gün) = 0,032877 |
   | **Saatlik dönüştürme faktörü** | Ödeme sıklığında, yıllık dönüştürme faktörü. Örneğin, aylık ödeme sıklığı için yıllık dönüştürme faktörü: </br></br>(12 aylık ödeme / 2080 saat) = 0,005769

4. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]