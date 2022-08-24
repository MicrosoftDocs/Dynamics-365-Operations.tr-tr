---
title: Günlük deftere naklini tersine çevirme
description: Bu makalede, fiş hareket listesinden veya mali günlüklerden fişleri ters kaydetmenize olanak sağlayan özellikler açıklanmaktadır.
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 7e3a22f43bcc312fe60b77db2fc3bc94d15950c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284866"
---
# <a name="reverse-journal-posting"></a>Günlük deftere naklini tersine çevirme

[!include [banner](../includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Finance'in bir günlüğün tamamını veya kaynağından bağımsız olarak, hareket listesinden bir veya daha fazla fişi ters kaydetmenize olanak sağlayan özellikleri açıklamaktadır. 

Bu makalede açıklanan özelliklerden birini kullanabilmeniz için bu özelliğin sisteminizde açılmış olması gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için **özellik yönetimi** çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:
 - Modül: Genel muhasebe
 - Özellik adı: **Birden çok belgeyi toplu tersine çevirme**

## <a name="reversing-journals"></a>Günlükleri ters kaydetme

Günlük satırlarını tek tek ters kaydedebilirsiniz. Ters günlük nakli ile tüm mali günlüğü de tersine çevirebilirsiniz. Bir günlüğü ters kaydetmek için: 

- Deftere nakledilmiş günlüklerde filtre uygulayın ve günlükte **Satırlar** görünümünü açın.
- Sayfanın üst tarafındaki **Ters kaydet** menüsüne tıklayın.
- Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz.
- Varolan hareket tarihlerini kullanmak için **Evet**'i, yeni bir hareket girmek için **Hayır**'ı seçin. Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmeniz gerekebilir.
- **Hayır**'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin. 
- Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin.
- **Ters kaydet** düğmesini seçin.

Hareketler ters kaydedilir. 

Fiş 100'den fazla satır içeriyorsa ters kayıt işlemi, toplu işlem kullanarak çalıştırılır. Toplu işlemdeki yorumları görüntüleyerek sonuçları inceleyebilirsiniz. Geri döndürülemeyen hareketler toplu iş geçmişinde listelenecektir.

Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır. Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Fiş hareket listesinden fişleri ters kaydetme. 

Tüm alt defterlerdeki **Fiş hareket listesinden** fişleri de ters kaydedebilirsiniz. Ayrıca, bir kerede birden fazla fişi ters kaydedebilirsiniz. 

Bir veya daha fazla fişi ters kaydetmek için: 

- Sayfanın üst tarafındaki **Tüm günlüğü tersine çevirme açılan** menüsünü seçin.
- Toplam fiş ve fiş satırı sayısı ve ters kaydedilmekte olan satırların toplam tutarı görüntülenir.
- Varolan hareket tarihlerini kullanmak için **Evet**'i, yeni bir hareket girmek için **Hayır**'ı seçin. Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmeniz gerekebilir.
- **Hayır**'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin. 
- Ters işlem hareketini açıklamak için bir açıklama girin.
- **Ters kaydet** düğmesini seçin.

Hareketler ters kaydedilir. 

100'den fazla fiş satırı varsa ters kayıt işlemi, toplu işlem kullanarak çalıştırılır. Toplu işlemdeki yorumları görüntüleyerek sonuçları inceleyebilirsiniz. Geri döndürülemeyen hareketler toplu iş geçmişine not edilir.

Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır. Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

Hareketler ancak ters işlem uygulanabilecek iş kurallarına uygun olduklarında ters kaydedilebilir. Bu makalede açıklanan özellik kullanılarak satıcı ödemeleri tersine çevrilemez. Satıcı ödemelerinin [Satıcı ödemesini tersine çevirme](../accounts-payable/reverse-vendor-payment.md) bölümünde listelenen adımlar kullanılarak tersine çevrilmesi gerekir.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
