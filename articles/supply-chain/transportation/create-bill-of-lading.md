---
title: Bir konşimento oluştur
description: Bu makalede, ambar yönetimi süreçleri (WMS) kullanırken bir konşimentonun nasıl oluşturulacağı açıklanmaktadır.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68a703475191255ff6ceaee25ef8e2bdf33ba0c2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069711"
---
# <a name="create-a-bill-of-lading"></a>Bir konşimento oluştur

[!include [banner](../includes/banner.md)]

Bu makalede, ambar yönetimi süreçleri (WMS) kullanırken bir konşimentonun nasıl oluşturulacağı açıklanmaktadır.  

Bir konşimento, maddeleri sevk eden şirket ve taşıyıcı arasındaki yasal bir belgedir. Belge sevk edilen maddelere eşlik eder ve öğeler varış noktasında teslim edildiğinde sevk irsaliyesi alış irsaliyesi olarak hizmet verir. Ambar yönetimi kullanıyorsanız, konşimento oluşturmanın iki yolu vardır:

  -   **Konşimento** sayfası kullanarak raporu el ile oluşturma.
  -   Raporu **Yük planlama workbench** üzerinden oluşturmak.

Konşimentoyu **Yük planlama workbench** üzerinden oluşturursanız, yük durumu **Sevk edilmiş.** olmalıdır. Yükte birden fazla sevkiyat varsa, her bir sevkiyat için bir konşimento oluşturulur. Bir konşimento oluşturulduktan sonra **Konşimento** sayfasında onun üzerinde değişiklik yapabilirsiniz.

## <a name="master-bill-of-lading"></a>Ana konşimento
Eğer yükte birden fazla sevkiyat varsa, bir ana konşimento oluşturabilirsiniz. Bu konşimento ile aynı biçime ve bilgilere sahiptir, ancak tüm sevkiyatların özetlenmiş bir içeriğini de içerir. Eğer **Bir yükte birden fazla sevkiyat olduğunda bir ana konşimento oluştur** seçeneği **Taşıma yönetim parametreleri** sayfasında **Evet** olarak ayarlanmışsa, bir konşimentoyu **Yük planlama workbench** üzerinden oluşturduğunuzda ve birden fazla sevkiyat bulunduğunda, otomatik olarak bir ana konşimento oluşturulacaktır. Ayrıca konşimento listelerini **İlgili bilgi** &gt; **Konşimento** üzerine tıklayarak da alabilirsiniz. Konşimentoları el ile oluşturuyorsanız, bir ana konşimentoyu **Konşimento** sayfası üzerinde oluşturabilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]