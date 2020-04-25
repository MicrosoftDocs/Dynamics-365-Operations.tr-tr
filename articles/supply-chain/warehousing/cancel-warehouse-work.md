---
title: Özel durum işleme için ambar işini iptal etme
description: Bu konu, ambar gözetmenlerinin durdurulan işi işlemesine izin veren İşi iptal et özelliğini açıklar.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205817"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Özel durum işleme için ambar işini iptal etme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'taki İşi iptal et işlevi, yönetici kullanıcının devam etmekte olan ancak sistem tarafından durdurulan veya olağanüstü durumlar nedeniyle tamamlanamayan belirli ambar işlerini iptal etmesine olanak tanır. Bu işlevsel, tutarsız verileri düzelten SQL düzeltme komut dosyaları için ilgi çekici ve güvenli bir alternatiftir. Ancak, bu komut dosyaları genellikle BT profesyonellerinden istense de, İşi iptal et işlevi şirkette yönetici haklarına sahip kullanıcılar tarafından kullanılabilir.

İş iptal et işlevine **Ambar yönetimi** \> **Periyodik görevler** \> **Temizle \> İşi iptal et**'ten erişebilirsiniz. **İşi iptal et** iletişim kutusunda iptal edilecek için iş kodunu belirtine ve **Tamam**'ı seçin.

## <a name="warehouse-work-that-can-be-canceled"></a>İptal edilebilecek ambar işi

Ambar çekme işlemleri sırasında, bir çalışan bir depolama konumundan kendi kullanıcı konumlarına çekilen miktarları kaydettiği ancak yerine koyma işlemini kaydedemediği durumlarla karşılaşabilir. Tutarsız ambar verileri genellikle, ancak her zaman değil, işin durdurulma nedenidir.

İş başlığındaki **İptal** düğmesi kullanılarak erişilebilen normal iptal işlevinden farklı olarak, İşi iptal et işlevi son tamamlanan iş satırının **koyma** türünde bir iş satırı olmasını gerektirmez. Başka bir deyişle, İşi iptal et işlevi için, iş satırındaki madde miktarı bir kullanıcı konumunda olsa bile, iptal mantığı çalışabilir.

> [!NOTE]
> Operasyonel nedenlerle iptal edilmesi gereken iş için ambar kullanıcıları iş sayfasındaki olağan İptal işlevini kullanmaya devam etmelidir.

İşi iptal et işlevi kullanılarak yalnızca **Satış**, **Transfer çıkışı**, **Ham madde çekme** veya **Stok yenileme** türündeki iş iptal edilebilir. İptal mantığı dondurulan ham madde çekme işi veya normal İptal işlevi kullanılarak iptal edilebilecek iş için çalışmaz (önceki nota bakın).

İşin engelini kaldırmak için sistem kalan tüm iş satırlarını iptal eder ve kullanıcının belirttiği iş koduyla ilişkilendirilmiş ambar verilerini düzeltir. Etkilenen madde miktarıyla ilgili normal ambar işleme operasyonları daha sonra devam edebilir.

İş iptal edildikten sonra etkilenen maddeyi belirli bir konuma koymak için, kullanıcının bir mobil cihazda stok hareketi veya miktar düzeltmesi işlemi kullanması gerekir.
