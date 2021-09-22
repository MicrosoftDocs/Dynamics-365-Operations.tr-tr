---
title: Stok günlükleri için "İş Akışı" açılan iletişim kutusunu bulamıyorsunuz
description: Günlük sayfasında "İş Akışı" açılır iletişim kutusunu bulamıyorsunuz veya ilgili iş akışı işlemleri kullanılamıyor
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477830"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Stok günlükleri için "İş Akışı" açılan iletişim kutusunu bulamıyorsunuz

## <a name="symptoms"></a>Belirtiler

Günlük sayfasında **İş akışı** açılır iletişim kutusunu bulamazsınız veya ilgili iş akışı işlemleri kullanılamaz.

Bu sorun, aşağıdaki bölümlerde açıklandığı gibi üç nedenden dolayı oluşabilir.

## <a name="resolution-1"></a>Çözüm 1

Sorun tüm kullanıcılar için geçerliyse sorunun nedeni onay iş akışının günlük adına atanmaması olabilir. Sorunu düzeltmek için şu adımları izleyin.

1. **Stok Yönetimi &gt; Kurulum &gt;> Günlük adları &gt;> Stok** öğesine gidin.
1. Liste bölmesinde, ayarlarını açmak için bir günlük adı seçin.
1. **Genel** hızlı sekmesinde, **Onay iş akışı** seçeneğini *Evet* olarak ayarlayın. Değişikliği onaylamanız istendiğinde, **Evet**'i seçin.
1. **İş akışı** alanında, seçili günlük adı için kullanmak istediğiniz iş akışını seçin.

## <a name="resolution-2"></a>Çözüm 2

İş akışınızda özelleştirilmiş kod kullanılıyorsa sistemi yükselttikten sonra sorunlar oluşabilir. Örneğin, günlük iş akışında **Gönder** düğmesi gri renkte olabilir. Bu nedenle, gönderimi onaylamak için düğmeyi seçemeyebilirsiniz.

**Gönder** düğmesi gri renkteyse iş akışınız özelleştirilmiş olabilir. Bu, `FormDataUtil` öğesindeki `canSubmitToWorkflow()` iş akışı yönteminin genişletildiği anlamına gelir. Bu sorunu gidermek için `canSubmitToWorkflow()` yöntemini genişletme şeklinizi aşağıdaki örnekte gösterilen yapıyı kullanarak değiştirin.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Çözüm 3

Sorun yalnızca belirli birkaç kullanıcı için geçerliyse bu kullanıcılar, stok günlüklerinde iş akışı işlemlerini çalıştırmak için gerekli güvenlik ayrıcalıklarına sahip olmayabilir. Etkilenen her kullanıcının *Stok günlüğü iş akışının bakımını yapma* güvenlik ayrıcalığına sahip olduğundan emin olun. Varsayılan olarak, bu ayrıcalık aynı adlı bir göreve atanır ve bu görev *Ambar çalışanı* ve *Ambar yöneticisi* rollerine uygulanır.
