---
title: NF-e XML dosyalarını ek olarak taşıma
description: Bu konuda, NF-e XML dosyalarının Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management veritabanınızın dışına nasıl taşınacağı ve bunun yerine ek olarak kullanılabilir hale nasıl getirileceği açıklanmaktadır.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799456"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML dosyalarını ek olarak taşıma

[!include [banner](../includes/banner.md)] 


Elektronik mali belgeler (NF-e) yayımlandığında, XML dosyaları oluşturulur ve bunlar Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management veritabanlarında depolanır. Brezilya Protekizcesi yerelleştirmesinde, Bu XML dosyalarının kullandığı veritabanı alanını boşaltmak için, **NF-e XML, ek olarak hareket etme** özelliğini kullanabilirsiniz.

Belirli bir tarih aralığı ve mali kuruluş kurulumu için özellik, NF-e XML dosyalarını Finance veya Supply Chain Management veritabanından Azure aboneliğinizdeki Blob Depolamaya taşır. Bu hareket, dosyaların yalnızca ek olarak kullanılabilmesini sağlar. XML dosyaları başarılı bir şekilde Blob Depolamasına taşındıktan sonra, özgün dosyalar Finance veya Supply Chain Management veritabanından silinir. Bu nedenle, bu dosyaların kullandığı veritabanı alanı serbest bırakılır.

**NF-e XML ek olarak hareket ettir** özelliğini etkinleştirmek için aşağıdaki adımları izleyin.

1. Finance veya Supply Chain Management'ta **Özellik yönetimi** çalışma alanını açın.
2. **Tümü** sekmesinde, **NF-e XML, bir ek olarak taşı** özelliğini arayın ve seçin.
3. **Şimdi etkinleştir**'i seçin.

NF-e XML dosyalarını ek olarak taşımak için bu adımları izleyin.

1. **Alacak hesapları** \> **Mali belgeler** \> **Elektronik mali belgeler** \> **NF-e XML öğesini ek olarak taşı** öğesine gidin.
2. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında başlangıç ve bitiş tarihlerini seçin.
3. **Mali kuruluş kodu** alanında bir değer seçin.
4. **Tamam**'ı seçin.

> [!IMPORTANT]
> İşlem geri alınamaz. NF-e XML dosyalarını taşıdıktan sonra, kullanıcılar yalnızca **Mali belge** sayfasının en üstündeki **Ekleri** seçerek görüntüleyebilirler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
