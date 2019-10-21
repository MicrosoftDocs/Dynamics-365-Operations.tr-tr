---
title: Ters günlük nakli
description: Bu konu, fiş hareket listesinden veya mali günlüklerden fişleri ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248597"
---
# <a name="reverse-journal-posting"></a>Ters günlük nakli

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Finance'in bir günlüğün tamamını veya kaynağından bağımsız olarak, hareket listesinden bir veya daha fazla fişi ters kaydetmenize olanak sağlayan yetenekleri açıklamaktadır. 

## <a name="reversing-journals"></a>Günlükleri ters kaydetme

Günlük satırlarını tek tek ters kaydedebilirsiniz. Ters günlük nakli ile tüm mali günlüğü de tersine çevirebilirsiniz. Bir günlüğü ters kaydetmek için: 
- Mali günlüğü açın ve deftere nakledilmiş günlükleri filtreleyin
- Sayfanın üst tarafındaki Ters kaydet menüsüne tıklayın
- Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz
- Varolan hareket tarihlerini kullanmak için Evet'i, yeni bir hareket girmek için Hayır'ı seçin. Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmek isteyebilirsiniz.
- Hayır'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin. 
- Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin
- Ters kaydet düğmesine tıklayın

Hareketler ters kaydedilir. 

Fiş satırlarının sayısı 100'ü aşarsa, ters kayıt işlemi, toplu işlem kullanarak çalıştırılır. Çalıştırılan toplu işlemdeki yorumları görüntüleyerek, ters kayıt sonuçlarını inceleyebilirsiniz. Tüm hatalar toplu iş geçmişine kaydedilir.

Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır. Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir. İletişim kutusunu kapatmak için Tamam'a tıklayın.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Fiş hareket listesinden fişleri ters kaydetme. 

Tüm alt defterlerdeki **Fiş hareket listesinden** fişleri de ters kaydedebilirsiniz. Ayrıca, bir kerede birden fazla fişi ters kaydedebilirsiniz. 

Bir veya daha fazla fişi ters kaydetmek için: 
- Sayfanın üst tarafındaki Ters kaydet menüsüne tıklayın
- Toplam fiş ve fiş satırı sayısının yanı sıra, ters kaydedilmekte olan satırların toplam tutarını görürsünüz
- Varolan hareket tarihlerini kullanmak için Evet'i, yeni bir hareket girmek için Hayır'ı seçin. Bazı durumlarda, orijinal hareketin dönemi kapalı olabilir ve ters kayıt için yeni bir hareket tarihi girmek isteyebilirsiniz.
- Hayır'ı seçtiyseniz, ters kayıt için bir hareket tarihi girin. 
- Ters kayıt hareketine eklenmesini istediğiniz bir açıklama girin
- Ters kaydet düğmesine tıklayın

Hareketler ters kaydedilir. 

Fiş satırlarının sayısı 100'ü aşarsa, ters kayıt işlemi, toplu işlem kullanarak çalıştırılır. Çalıştırılan toplu işlemdeki yorumları görüntüleyerek, ters kayıt sonuçlarını inceleyebilirsiniz. Tüm hatalar toplu iş geçmişine kaydedilir.

Fiş satırlarının sayısı 100 veya daha az ise ters kayıt işlemi hemen çalıştırılır. Sonuçlar, ters kaydedilememiş fişleri ve ters kaydedilememe nedenlerini gösteren bir iletişim kutusunda görüntülenir. İletişim kutusunu kapatmak için Tamam'a tıklayın.

