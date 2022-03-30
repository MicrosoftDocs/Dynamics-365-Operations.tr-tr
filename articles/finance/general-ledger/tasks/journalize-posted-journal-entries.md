---
title: Nakledilen günlük girişlerini günlüğe aktarma
description: Bu yordamda, günlüğe kaydetme yoluyla günlük girişleri oluşturma gösterilir.
author: aprilolson
ms.date: 03/09/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d8fca167563b14c825ebe29874c6488ddfb4d9a
ms.sourcegitcommit: 06acdfbccd7bd213a2397ea7b85d104f01914437
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2022
ms.locfileid: "8400887"
---
# <a name="journalize-posted-journal-entries"></a>Deftere nakledilen yevmiye defteri girişlerini yevmiye defterine kaydetme

[!include [banner](../../includes/banner.md)]

Genel muhasebedeki günlüğe eşitleme işlemi, genel muhasebenizdeki deftere nakledilen fiş girişlerini gruplamak ve raporlamak için bir yöntem sağlar. Sağladığınız ölçütlere göre, işlem benzersiz bir numara serisi kullanan ve genel muhasebe **Günlük numarası** değeri referans olarak bulunan fişlerin bir listesini oluşturur.

Günlüğe kaydetme yoluyla günlük girişleri oluşturmak için aşağıdaki adımları izleyin. Bu yordam, **USMF** demo verisi şirketini kullanır.

1. **Genel muhasebe** \> **Genel muhasebe ayarı** \> **Genel muhasebe parametreleri**'ne gidin.
2. **Genişletilmiş genel muhasebe günlüğü** alanında, bir değer seçin. **Evet**'i seçerseniz rapor çıktısı farklı olacaktır.
3. Günlüğe kaydetme işlemi çalıştırılmazsa dönemin kapatılıp kapatılmayacağını seçin. Bu seçenek **Evet**'i belirlerseniz, günlüğe kaydetme işlemi söz konusu dönem için tamamlanana kadar dönem kapatılamaz.
4. Sayfayı kapatın.
5. **Genel muhasebe** \> **Periyodik görevler** \> **Günlükleştirme**'ye gidin ve **Filtre**'yi seçin.
6. Tanımlamak istediğiniz filtre ölçütler için satırı seçin.
7. **Ölçütler** alanında filtre ölçütlerini girin veya seçin.
8. Sayfayı kapatmak için **Tamam** öğesini seçin.
9. Günlüğe kaydetme işlemini başlatmak için **Tamam**'ı seçin. İşlem tamamlandıktan sonra bir rapor oluşturulur.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
