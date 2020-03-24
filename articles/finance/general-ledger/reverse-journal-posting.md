---
title: Ters günlük nakli
description: Bu konu, fiş hareket listesinden veya mali günlüklerden fişleri ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5d1c58463c24dc6a40b036f0bb803316bbb65c2
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091911"
---
# <a name="reverse-journal-posting"></a>Ters günlük nakli

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Finance'in bir günlüğün tamamını veya kaynağından bağımsız olarak, hareket listesinden bir veya daha fazla fişi ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır. 

## <a name="reversing-journals"></a>Günlükleri ters kaydetme

Günlük satırlarını tek tek ters kaydedebilirsiniz. Ters günlük nakli ile tüm mali günlüğü de tersine çevirebilirsiniz. Bir günlüğü ters kaydetmek için: 

- Mali günlüğü açın ve deftere nakledilmiş günlükleri filtreleyin.
- Sayfanın üst tarafındaki **Ters kaydet** menüsüne tıklayın.
- Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz
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

- Sayfanın üst tarafındaki **Ters kaydet** menüsünü seçin.
- Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz.
- Varolan hareket tarihlerini kullanmak için **Evet**'i, yeni bir hareket girmek için **Hayır**'ı seçin. Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmeniz gerekebilir.
- **Hayır**'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin. 
- Ters işlem hareketini açıklamak için bir açıklama girin.
- **Ters kaydet** düğmesini seçin.

Hareketler ters kaydedilir. 

100'den fazla fiş satırı varsa ters kayıt işlemi, toplu işlem kullanarak çalıştırılır. Toplu işlemdeki yorumları görüntüleyerek sonuçları inceleyebilirsiniz. Geri döndürülemeyen hareketler toplu iş geçmişine not edilir.

Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır. Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

Hareketler ancak ters işlem uygulanabilecek iş kurallarına uygun olduklarında ters kaydedilebilir. Bu konuda açıklanan özellik kullanılarak satıcı ödemeleri tersine çevrilemez. Satıcı ödemelerinin [Satıcı ödemesini tersine çevirme](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) bölümünde listelenen adımlar kullanılarak tersine çevrilmesi gerekir.

