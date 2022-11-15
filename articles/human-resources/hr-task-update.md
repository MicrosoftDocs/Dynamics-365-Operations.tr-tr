---
title: Görev yönetiminde görevleri ayarlama
description: Bu makalede, Microsoft Dynamics 365 Human Resources'te Görev yönetimindeki görevlerin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745397"
---
# <a name="set-up-tasks-in-task-management"></a>Görev yönetiminde görevleri ayarlama

[!INCLUDE [PEAP](../includes/peap-1.md)]

Microsoft Dynamics 365 Human Resources'in 10.0.30 sürümünden önceki sürümlerinde, kullanıcıların bir görevi düzenlemesi için bu görevi içeren her denetim listesinde ayrı ayrı düzenlemeleri gerekiyordu. Ancak Human Resources 10.0.30 sürümünden itibaren kullanıcılar, düzenlenen görevlerin nasıl işleneceğini seçebilirler. Düzenlenen bir görev denetim listesindeyse düzenlenen görevi kullanmak üzere denetim listesini etkinleştirmek için **İnsan kaynakları paylaşılan parametreleri** sayfasının **Görev yönetimi** sekmesinde **Görev yönetimi yükseltmesini etkinleştir** seçeneği belirlenmelidir.

[![İnsan kaynakları paylaşılan parametreleri sayfasında görev yönetimi yükseltme seçeneğini etkinleştirin.](./media/task-update.png)](./media/task-update.png)

Görevlerdeki düzenlemelerin tüm denetim listesi görevlerine uygulanması gerekiyorsa görev kitaplığındaki görev ile denetim listesindeki görev arasında önceden bir ilişki bulunmalıdır. Kitaplık görevi ile denetim listesi görevi arasındaki ilişkiyi oluşturmak için bir seçenek eklenmiştir.

Görevleri tek olarak oluşturup birden çok denetim listesinde yeniden kullanabilirsiniz. Görev oluşturmak için, **Ekleme kurulumu** sayfasında, **Görevler** sekmesinde, **Yeni**'yi seçin.

## <a name="set-up-tasks"></a>Görevleri ayarlama

Oluşturulan bir görevi birden çok denetim listesine atamak için görevi seçin ve ardından menüde **Denetim listelerine uygula**'yı seçin.

Alternatif olarak, görevleri doğrudan bir denetim listesine ekleyebilirsiniz. Bir denetim listesine görev eklemek için **Ekleme kurulumu** sayfasında, **Denetim listesi** sekmesinde, görevi eklemek için yeni bir denetim listesi oluşturun veya görevi varolan bir denetim listesine ekleyin.

Bir kitaplık görevini düzenlemek için görev kitaplığı menüsünden **Düzenle**'yi seçin. Görev herhangi bir denetim listesiyle ilişkiliyse bu denetim listeleri **Görevi düzenle** sayfasında görüntülenir. Denetim listelerindeki görevlerin düzenlemelerle güncelleştirilmesini istiyorsanız **Denetim listelerine uygula** bölümünden bu denetim listelerini seçin.

Görev kitaplığından görevleri silmek için **Sil** seçeneğini belirleyin. Görev bir denetim listesiyle ilişkiliyse bu eylem görevi denetim listesinden silmez. Denetim listesindeki bir görevi kaldırmak için ayrı bir eylem gerekir.

### <a name="set-up-checklists"></a>Denetim listelerini ayarlama

Denetim listesi bir görev grubudur. Gereksinim duyduğunuz kadar çok sayıda denetim listesi oluşturabilir ve aynı görevleri birden çok denetim listesine atayabilirsiniz. Bir denetim listesi oluşturduğunuzda, bir sahip ve takvim belirtirsiniz.

Denetim listesinde yeni bir görev oluşturmak için görev menü çubuğundan **Yeni**'yi seçin. Yeni bir görev oluşturduğunuzda birden çok denetim listesi arasında paylaşılabilmesi için isteğe bağlı olarak görev kitaplığına görev eklemeyi seçebilirsiniz. Görevi görev kitaplığına eklemek için **Görevi kitaplığa uygula** seçeneğini **Evet** olarak ayarlamanız gerekir. Görevi görev kitaplığına eklemeyi seçerseniz **Denetim listelerine uygula** bölümünde bu denetim listelerini seçerek görevi aynı anda diğer denetim listelerine de ekleyebilirsiniz. Görevi görev kitaplığına eklememeyi seçerseniz görev yalnızca görevi oluşturduğunuz denetim listesinde bulunur.

Denetim listesindeki bir görevi düzenlemek için görev menüsünden **Düzenle**'yi seçin. Görev herhangi bir denetim listesiyle ilişkiliyse bu denetim listeleri **Görevi düzenle** sayfasında görüntülenir. Diğer denetim listelerindeki görevlerin düzenlemelerle güncelleştirilmesini istiyorsanız **Denetim listelerine uygula** bölümünden bu denetim listelerini seçin.

Denetim listesinden görevleri kaldırmak için **Kaldır**'ı seçin. Bu eylem görevleri denetim listesinden kaldırır. Ancak görevleri görev kitaplığından silmez. Görev kitaplığından görevleri silmek için **Görev kitaplığı** sayfasını açın ve **Sil**'i seçin.
