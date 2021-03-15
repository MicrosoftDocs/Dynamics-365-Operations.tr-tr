---
title: Bir konşimento oluştur
description: Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b001ef8936e7e35db89163683c023211f79b24c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996487"
---
# <a name="create-a-bill-of-lading"></a>Bir konşimento oluştur

[!include [banner](../includes/banner.md)]

Bu konu, ambar yönetimi işlemleri kullanırken bir konşimentonun nasıl oluşturulacağını açıklar.  

Bir konşimento, maddeleri sevk eden şirket ve taşıyıcı arasındaki yasal bir belgedir. Belge sevk edilen maddelere eşlik eder ve öğeler varış noktasında teslim edildiğinde sevk irsaliyesi alış irsaliyesi olarak hizmet verir. Ambar yönetimi kullanıyorsanız, konşimento oluşturmanın iki yolu vardır:

  -   **Konşimento** sayfası kullanarak raporu el ile oluşturma.
  -   Raporu **Yük planlama workbench** üzerinden oluşturmak.

Konşimentoyu **Yük planlama workbench** üzerinden oluşturursanız, yük durumu **Sevk edilmiş.** olmalıdır. Yükte birden fazla sevkiyat varsa, her bir sevkiyat için bir konşimento oluşturulur. Bir konşimento oluşturulduktan sonra **Konşimento** sayfasında onun üzerinde değişiklik yapabilirsiniz.

## <a name="master-bill-of-lading"></a>Ana konşimento
Eğer yükte birden fazla sevkiyat varsa, bir ana konşimento oluşturabilirsiniz. Bu konşimento ile aynı biçime ve bilgilere sahiptir, ancak tüm sevkiyatların özetlenmiş bir içeriğini de içerir. Eğer **Bir yükte birden fazla sevkiyat olduğunda bir ana konşimento oluştur** seçeneği **Taşıma yönetim parametreleri** sayfasında **Evet** olarak ayarlanmışsa, bir konşimentoyu **Yük planlama workbench** üzerinden oluşturduğunuzda ve birden fazla sevkiyat bulunduğunda, otomatik olarak bir ana konşimento oluşturulacaktır. Ayrıca konşimento listelerini **İlgili bilgi** &gt; **Konşimento** üzerine tıklayarak da alabilirsiniz. Konşimentoları el ile oluşturuyorsanız, bir ana konşimentoyu **Konşimento** sayfası üzerinde oluşturabilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]