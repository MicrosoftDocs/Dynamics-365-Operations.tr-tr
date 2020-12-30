---
title: Kiralama günlüğü adlarını ayarlama
description: Bu konu, kiralama günlüğü adlarının nasıl tanımlanacağını açıklamaktadır. Kiralama günlüğü adları, Varlık kiralamada girişlerin nakledildiği günlükleri belirtir.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449004"
---
# <a name="set-up-lease-journal-names"></a>Kiralama günlüğü adlarını ayarlama

[!include [banner](../includes/banner.md)]

Kiralama günlüğü adları, Varlık kiralama hareketlerinin nakledildiği günlükleri belirtir. Yalnızca **Varlık kiralama** günlük türüne atanmış günlük adları, **Varlık kiralama parametreleri** sayfasında **İlk Kabul** ve **Aylık Günlük Adı** alanlarında gösterilir. Yalnızca **satıcı faturası kaydı** günlük türü **Satıcı günlüğü adı** alanına atanabilir.

Kiralama günlüğü adlarını yapılandırmak için aşağıdaki adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**'ne gidin.
2. **Genel** sekmesindeki **İlk kabul günlük adı** alanında bir günlük seçin. Tüm ilk kabul günlüğü girişleri bu günlük adına nakledilecek.
3. **Fatura günlük adı** alanında, bir günlük seçin. Kiralama defteri için **Satıcıya öde** seçeneği **Evet** olarak ayarlanmışsa kiralama ve gider ödeme faturaları bu günlük adına nakledilir.
4. **Kiralama günlüğü adı** alanında, bir günlük seçin. Tüm amortisman, faiz ve kısa süreli yeniden sınıflama girişleri bu günlük adına nakledilecek. Kiralama defteri için **Satıcıya öde** seçeneği **Hayır** olarak ayarlanmışsa kira ödemeleri ve gider ödeme girişleri de bu günlük adına nakledilir.