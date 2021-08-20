---
title: Tamamlandı bildirimi günlüğü deftere nakledildiğinde hata
description: Tamamlandı bildirimi günlüğü deftere nakledildiğinde, sipariş edilen miktarın azaltılamadığını belirten bir hata iletisi alırsınız.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750942"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Tamamlandı bildirimi günlüğü deftere nakledildiğinde hata

KB numarası: 4612891

## <a name="symptoms"></a>Belirtiler

**Tamamlandı bildirimi** günlüğünü deftere naklettiğinizde, bir hata oluşur ve aşağıdaki hata iletisini alırsınız:

> Siparişli durumda yeterli açık stok hareketi bulunmadığından, sipariş edilen miktar azaltılamaz. Maddeler; Satın Alındı, Teslim Alındı veya Kaydedildi.

Bu hata yalnızca **Hata miktarı** alanı, **Tamamlandı bildirimi** günlüğünün ilk satırında ayarlandığında ve en son satırda **Sağlam miktar** alanı ayarlandığında oluşur. **Hata miktarı** alanı son satırda ayarlanırsa bir hata oluşmaz.

## <a name="resolution"></a>Çözünürlük

Bu hatayı önlemek için, **Üretim denetim parametreleri** sayfasını açın ve **Genel** sekmesinde **Hata miktarı olan kalan miktarı artır** seçeneğini *Evet* olarak ayarlayın.
