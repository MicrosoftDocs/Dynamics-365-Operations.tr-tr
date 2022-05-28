---
title: Satıcı sertifikasını koruma
description: Bu konu, Satıcı işbirliği çalışma alanını kullanarak satıcıların sertifikalarını korumak için kullanabileceği adımları açıklamaktadır.
author: v-kiarnd
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b1b2cdd4389afd8997b60fe8e7a9b6851cbde199
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735709"
---
# <a name="maintain-vendor-certification"></a>Satıcı sertifikasını koruma

[!include [banner](../includes/banner.md)]

Bu konu, **Satıcı işbirliği çalışma alanı**'nı kullanarak satıcılarınızın sertifikalarını korumak için kullanabileceği adımları açıklamaktadır. Sertifika örnekleri arasında Kadın İşletme Girişimi (WBE) veya Enerji ve Çevre Tasarımında Liderlik (LEED) şirketi olabilir. Satıcıların, **Satıcı bilgileri** çalışma alanına sertifika bilgilerini girmesi gerekir. Burada satıcılar, **Daha fazla ayrıntı** seçeneğini belirler ve ardından **Sertifikalar**'ı seçer.

## <a name="turn-on-the-vendor-certification-feature"></a>Satıcı sertifikasyonu özelliğini açma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül** - *Borç hesapları*
- **Özellik adı** - *Satıcı işbirliği sertifika yönetimini etkinleştirme*

## <a name="add-a-new-certification"></a>Yeni sertifika ekleme

Yeni bir sertifika eklemek için, **Satıcı bilgileri** çalışma alanında **Sertifika** ızgarasının üzerinde bulunan **Ekle** düğmesini seçin. Aşağıdaki bilgileri girin:

- Sertifika sertifikası
- Sertifika türü
- Sertifika organizasyonu
- Sertifika tarihi
- Borç tutarı (geçerliyse)
- Geçerlilik tarihi
- Bitiş tarihi
- Yorumlar, isteğe bağlı

Belirli bir sertifika ile ilgili belgeler varsa, **Belge** düğmesini seçerek bunları iliştirebilirsiniz.

Satıcılarınız tarafından bu sayfaya girilen sertifikalara "Satıcı" kaynağı atanır. Satıcı banka hesapları altından satıcınız adına sertifika bilgileri girebilirsiniz. Bilgiler burada görünür ve kaynak **Müşteri** olarak görüntülenir.

Satıcılar gerektiğinde, sertifikalarını düzenleyebilir veya silebilir.

## <a name="vendor-collaboration-generated-certification-records"></a>Satıcı işbirliğiyle oluşturulmuş sertifika kayıtları

Sertifika bilgileri bir satıcı tarafından eklendikten sonra, bilgiler, **Satıcı işbirliğiyle oluşturulmuş sertifika kayıtları** sayfasında görüntülenecektir. Sayfayı açmak için, **Borç hesapları > Sorgular > Satıcı raporları > Satıcı işbirliğiyle oluşturulmuş sertifikalar**'a gidin. Varsayılan olarak, tüm yeni veya değiştirilmiş sertifika kayıtları görüntülenir. Borç hesabı görevlisi, değişiklikleri görüntüleyebilir ve doğrulama işlemi aracılığıyla bilgileri doğrulayabilir. Bilgiler onaylandıktan sonra, sayfada listelenen sertifika kaydı incelendi olarak seçilip işaretlenebilir. Kaydın incelendi olarak işaretlenmesi, bunu varsayılan listeden kaldırır.

Tüm sertifika değişiklikleri, **Satıcı işbirliğiyle oluşturulan sertifikalar** sayfasında görüntülenir. Sayfada bir değişiklik görüntülenmiyorsa satıcı hesabı, geçerlilik tarihi aralığı veya incelenmiş sertifika değişiklikleri bilgilerinin eklenip eklenmeyeceğini belirlemeyle ilgili filtreleri ayarlayarak bunu görüntüleyebilirsiniz.

