---
title: Kiralama yükümlülüğünün kısa vadeli bölümünü yeniden sınıflandırma
description: Bu konu, kiralama yükümlülüğünün bir bölümünü kısa süreli olarak yeniden sınıflandırmak için aylık günlük girdisinin nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d98d66b5fe9d32a86eb75d937fedfdca6773ac4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823107"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Kiralama yükümlülüğünün kısa süreli bölümünü yeniden sınıflandırma

[!include [banner](../includes/banner.md)]

Bu konu, kiralama yükümlülüğünün bir bölümünü kısa süreli olarak yeniden sınıflandırmak için aylık günlük girdisinin nasıl oluşturulacağını açıklamaktadır. Toplu iş işleminde seçilen plan **Kısa süreli kira yükümlülüğü yeniden sınıflandırma** olduğunda bir günlük girişi oluşturulur. Bu giriş, ayın son gününe kiralama yükümlülüğünün geçerli bölümünü deftere nakletmek için kullanılır. Aynı zamanda, sonraki ayın ilk günü itibarıyla ters kayıt girişi de deftere nakledilir.

Kiralama yükümlülüğünün kısa süreli kısmı, yükümlülük amortisman planında gösterilir. Günlük girişi deftere nakledildiğinde, **Yükümlülük yeniden sınıflama günlüğü oluşturuldu** sütunu kullanılabilir duruma gelir ve günlük kimliği de plana göre doldurulur.

Kısa süreli yükümlülük yeniden sınıflama günlüğü girişi oluşturmak ve deftere nakletmek için aşağıdaki adımları izleyin.

1. **Varlık kiralama \> Periyodik \> Toplu iş günlük oluşturma** bölümüne gidin.
2. **Toplu iş günlük oluşturma** iletişim kutusundaki **Plan seçin** alanında **Kısa süreli kiralama yükümlülüğünü yeniden sınıflandırma**'yı seçin.
3. **Kiralama grubu** alanında bir kiralama grubu seçin. Bunun yerine, **Defter Kimliği** alanında defter kimliğini de seçebilirsiniz.
4. **Deftere naklet** parametresini açın. Girişin oluşturulması ancak deftere nakledilmemesi gerekiyorsa bunun yerine parametreyi kapalı bırakın.
5. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
