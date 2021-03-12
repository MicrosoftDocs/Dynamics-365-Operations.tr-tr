---
title: Toplu işte aylık günlük girişleri oluşturma
description: Bu konuda, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağını açıklamaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971340"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Toplu işte aylık günlük girişleri oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağını açıklamaktadır. Birden fazla plandan günlük girişleri oluşturmak için toplu iş işleme kullanılabilir. Bu günlük girişleri arasında kira ödemeleri, yükümlülük amortismanı, kullanım hakkı (ROU) varlığı amortismanı ve icra maliyeti giderleri yer alır. Aynı anda birden fazla kiralamanın ilk kabulünü yapmak veya aynı anda birden fazla kiralama için geçiş düzeltmeleri oluşturmak amacıyla toplu iş işlemeyi kullanabilirsiniz.

Toplu iş ayarlamak veya birden fazla kiralama için ödeme faturaları, amortisman veya faiz işlemek amacıyla **Varlık kiralama \> Periyodik \> Toplu iş günlük oluşturma** bölümüne gidin. Görüntülenen iletişim kutusunda, günlük girişlerinin oluşturulacağı planlamayı seçebilirsiniz. Toplu işin belirli varlıklar, kiralama grupları veya kiralama defterleri için çalıştırılıp çalıştırılmayacağını da belirtebilirsiniz.

> [!NOTE]
> Yükümlülük amortismanı planlaması, ödemeler, amortisman ve giderler gibi sonraki hareketler, yalnızca ilgili kiralama için ilk kabul deftere nakledildikten sonra deftere nakledilir.
>
> Günlük girişleri oluşturulur ancak siz **Çalıştır** komutunu seçene kadar deftere nakledilemez.
