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
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d53181d63f7b362662d993e21671e9b685b5dfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968439"
---
# <a name="set-up-main-account-categories"></a>Ana hesap kategorilerini ayarlama

[!include [banner](../../includes/banner.md)]

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
