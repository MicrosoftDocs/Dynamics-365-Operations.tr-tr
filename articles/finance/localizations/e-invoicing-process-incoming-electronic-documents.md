---
title: Gelen elektronik belgelerin işlemesi
description: Bu makalede, gelen elektronik belgelerin işlemesi hakkında bir genel bakış sağlanmaktadır.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910022"
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
