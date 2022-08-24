---
title: Gelen elektronik belgelerin işlemesi
description: Bu makalede, gelen elektronik belgelerin işlemesi hakkında bir genel bakış sağlanmaktadır.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277316"
---
# <a name="processing-of-incoming-electronic-documents"></a>Gelen elektronik belgelerin işlemesi

[!include [banner](../includes/banner.md)]

Satıcı elektronik faturaları gibi gelen elektronik belgeler iki şekilde içe aktarılabilir ve işlenebilir:

- Dosyalar, harici kanallardan alınır ve bağlantılı uygulamanıza doğrudan geçirilir. Burada, ek dönüşüme tabi tutulurlar ve daha sonra veritabanına aktarılırlar.
- Dosyaları, Elektronik Faturalama hizmetinde ön işlemeye tabi tutulur ve ardından bağlı uygulamanıza aktarılır.

Elektronik faturalama gelen belgeler için iki kanalı destekler: e-posta ve Microsoft SharePoint klasörleri.

Belgelerin ön işlemeye mi tabi tutulacağını yoksa doğrudan bağlı uygulamanıza mı gideceğini belirten iki kurulum türü bulunur:

- **Veri kanalı** – Sistem, belgeyi doğrudan bağlı uygulamaya geçirir.
- **İşlem ardışık düzeni ile veri kanalı** – Belge bağlantılı uygulamaya geçirilmeden önce çalıştırılacak ek eylemler ayarlayabilirsiniz.

Farklı kanallar için gelen elektronik belgeleri işleme senaryolarını ayarlama hakkında bilgi için bkz. [E-posta kanalı yapılandırma](e-invoicing-configure-email.md) ve [SharePoint kanalı yapılandırma](e-invoicing-configure-sharepoint-channel.md).
