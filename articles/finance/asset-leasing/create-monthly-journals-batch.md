---
title: Toplu işte aylık günlük girişleri oluşturma
description: Bu makalede, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağı açıklanmaktadır.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb5c65b0a2c982171fa0ae88141d92c2f1ead6ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895007"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Toplu işte aylık günlük girişleri oluşturma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Bu makalede, aylık kira giderleri kaydedilirken verimliliği artırmaya yardımcı olmak için toplu işte günlük girişlerinin nasıl oluşturulacağı açıklanmaktadır. Birden fazla plandan günlük girişleri oluşturmak için toplu iş işleme kullanılabilir. Bu günlük girişleri arasında kira ödemeleri, yükümlülük amortismanı, kullanım hakkı (ROU) varlığı amortismanı ve icra maliyeti giderleri yer alır. Aynı anda birden fazla kiralamanın ilk kabulünü yapmak veya aynı anda birden fazla kiralama için geçiş düzeltmeleri oluşturmak amacıyla toplu iş işlemeyi kullanabilirsiniz.

Toplu iş ayarlamak veya birden fazla kiralama için ödeme faturaları, amortisman veya faiz işlemek amacıyla **Varlık kiralama \> Periyodik \> Toplu iş günlük oluşturma** bölümüne gidin. Görüntülenen iletişim kutusunda, günlük girişlerinin oluşturulacağı planlamayı seçebilirsiniz. Toplu işin belirli varlıklar, kiralama grupları veya kiralama defterleri için çalıştırılıp çalıştırılmayacağını da belirtebilirsiniz.

> [!NOTE]
> Yükümlülük amortismanı planlaması, ödemeler, amortisman ve giderler gibi sonraki hareketler, yalnızca ilgili kiralama için ilk kabul deftere nakledildikten sonra deftere nakledilir.
>
> Günlük girişleri oluşturulur ancak siz **Çalıştır** komutunu seçene kadar deftere nakledilemez.

İlk kabul günlüğünü kiralamanın başlangıç tarihinden farklı bir tarihte deftere nakletmek için **İlk kabul deftere nakletme tarihini atama**'yı seçin. Doğru deftere nakletme tarihini belirttiğiniz bir **Tarih** alanı görüntülenir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
