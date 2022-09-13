---
title: Özel durum işleme için ambar işini iptal etme
description: Bu makale, ambar gözetmenlerinin durdurulan işi işlemesine izin veren işi iptal et özelliğini açıklar.
author: Mirzaab
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b1e2036e4e7a8a47d6df029f285df7aca0fa74e6
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403705"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>Özel durum işleme için ambar işini iptal etme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'taki işi iptal et işlevi, yönetici kullanıcının devam etmekte olan ancak sistem tarafından durdurulan veya olağanüstü durumlar nedeniyle tamamlanamayan belirli ambar işlerini iptal etmesine olanak tanır. Bu işlevsel, tutarsız verileri düzelten SQL düzeltme komut dosyaları için ilgi çekici ve güvenli bir alternatiftir. Ancak, bu komut dosyaları genellikle BT profesyonellerinden istense de, işi iptal et işlevi şirkette yönetici haklarına sahip kullanıcılar tarafından kullanılabilir.

İşi iptal et işlevine **Ambar yönetimi** \> **Periyodik görevler** \> **Temizle \> İşi iptal et**'ten erişebilirsiniz. **İşi iptal et** iletişim kutusunda iptal edilecek için iş kodunu belirtine ve **Tamam**'ı seçin.

## <a name="warehouse-work-that-can-be-canceled"></a>İptal edilebilecek ambar işi

Ambar çekme işlemleri sırasında, bir çalışan bir depolama konumundan kendi kullanıcı konumlarına çekilen miktarları kaydettiği ancak yerine koyma işlemini kaydedemediği durumlarla karşılaşabilir. Tutarsız ambar verileri genellikle, ancak her zaman değil, işin durdurulma nedenidir.

İş başlığındaki **İptal** düğmesi kullanılarak erişilebilen normal iptal işlevinden farklı olarak, işi iptal et işlevi son tamamlanan iş satırının **yerleştirme** türünde bir iş satırı olmasını gerektirmez. Başka bir deyişle, işi iptal et işlevi için, iş satırındaki madde miktarı bir kullanıcı konumunda olsa bile, iptal mantığı çalışabilir.

> [!NOTE]
> Operasyonel nedenlerle iptal edilmesi gereken iş için ambar kullanıcıları iş sayfasındaki olağan iptal işlevini kullanmaya devam etmelidir.

İşi iptal et işlevi kullanılarak yalnızca **Satış**, **Transfer çıkışı**, **Ham madde çekme** veya **Stok yenileme** türündeki iş iptal edilebilir. İptal mantığı dondurulan ham madde çekme işi veya normal iptal işlevi kullanılarak iptal edilebilecek iş için çalışmaz (önceki nota bakın).

İşin engelini kaldırmak için sistem kalan tüm iş satırlarını iptal eder ve kullanıcının belirttiği iş koduyla ilişkilendirilmiş ambar verilerini düzeltir. Etkilenen madde miktarıyla ilgili normal ambar işleme operasyonları daha sonra devam edebilir.

İş iptal edildikten sonra etkilenen maddeyi belirli bir konuma koymak için, kullanıcının bir mobil cihazda stok hareketi veya miktar düzeltmesi işlemi kullanması gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]