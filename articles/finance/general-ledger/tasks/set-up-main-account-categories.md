---
title: Ana hesap kategorilerini ayarlama
description: Bu konuda, Dynamics 365 Finance'da ana hesap kategorilerinin nasıl ayarlanacağı açıklanmaktadır.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fabdcd61c60e630e3f32bc4f0c13c44f50259a6
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091934"
---
# <a name="set-up-main-account-categories"></a>Ana hesap kategorilerini ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu konuda, ana hesap kategorilerinin nasıl ayarlanacağı açıklanmaktadır. Ana hesap kategorileri, finansal raporlamada ve Power BI'da varsayılan raporlar için kullanılır. Varsayılan olarak oluşturulan ana hesap kategorileri yeniden adlandırılabilir ancak silinemez. Ek hesap kategorileri raporlama ve çözümleme amacıyla oluşturulabilir ve kullanılabilir. Bu konu, USMF demo şirketini kullanır.

## <a name="create-a-main-account-category"></a>Bir ana hesap kategorisi oluştur
1. Gezinti bölmesinde **Modüller > Genel muhasebe > Hesap planı > Hesaplar > Ana hesap kategorileri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Ana hesap kategorisi** alanında benzersiz bir ad girin.
4. **Açıklama alanında**, ana hesap kategorisi için bir açıklama girin.
5. **Ana hesap türü** alanında, kategoriyle bağlantılandırılacak ana hesap türünü seçin.

## <a name="link-main-accounts-to-account-category"></a>Ana hesapları hesap kategorisine bağla
1. **Ana hesapları bağla** öğesine tıklayın.
2. Listede, **Bağlı** sütundaki kutuları işaretleyerek ana hesap kategorisine atanacak ana hesapları seçin. Bu kategori finansal raporlama ve çözümleme için kullanıldığında ana hesapları bir ana hesap kategorisine atamak hesapların bakiyelerini toplar.  
3. Ana hesapları seçmek için **Bağlantılı** seçeneğini işaretleyin veya işaretini kaldırın.
4. **Tamam**'ı seçin.
5. **Evet**'i seçin.
