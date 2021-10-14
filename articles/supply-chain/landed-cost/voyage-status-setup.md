---
title: Seyahat durumu kurulumu
description: Bu konuda, kullanıcıların yolculuklara atayabilecekleri durum değerlerinin nasıl oluşturulabileceği açıklanmaktadır.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 01bfc5198b62cfe56df9ec6763d5d0ff95f13ed5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571005"
---
# <a name="voyage-status-setup"></a>Seyahat durumu kurulumu

[!include [banner](../../includes/banner.md)]

**Seyahat durumları** sayfasında, kullanıcıların seyahatlere atayabileceği durum değerleri kümesini oluşturursunuz. Kullanıcılar bir seyahatin tüm seviyelerine seyahat durumu değerleri atayabilir: seyahat, sevkiyat konteyneri, folyo, satın alma siparişi ve madde (satın alma satırları ve transfer emri satırları). İki amaç için kullanılırlar:

- Kullanıcıyı seyahatin, sevkiyat konteynerinin, folyonun, satın alma siparişinin veya maddenin (satın alma satırları ve transfer emri satırları) durumu hakkında bilgilendirmek.
- Değişikliği veya silmeyi önleyerek maliyet alanının kullanımını sınırlamak.

Seyahat durumlarınızı ayarlamak için **Varış yeri maliyeti \> Kurulum \> Seyahat durumları**'na gidin. Buradan, eylem bölmesindeki düğmeleri kullanarak durumları ekleyebilir, kaldırabilir ve düzenleyebilirsiniz.

Her maliyet alanının kendi seyahat durumları kümesi ve hiyerarşisi vardır. Bu nedenle, **Seyahat durumları** sayfasında, **Maliyet alanı** alanında, önce görüntülemek veya seyahat durumları oluşturmak istediğiniz maliyet alanını seçmeniz gerekir. Ardından, her seyahat durumu için aşağıdaki tabloda açıklanan alanları gerektiği gibi ayarlayın. Bir seyahatin durumunun, izleme denetim merkezi kullanılarak oluşturulan kurallar gibi sistem olayları tarafından da otomatik olarak değiştirilebileceğini unutmayın.

| Alan | Tanım |
|---|---|
| Seyahat durumu | Seyahat durumunun adını girin. |
| Tanım | Seyahat durumunun bir açıklamasını girin. |
| Değiştir | Kullanıcıların bu durumdaki seyahatleri değiştirmesine izin veriliyorsa bu onay kutusunu işaretleyin. |
| Delete | Kullanıcıların bu durumdaki seyahatleri silmelerine izin veriliyorsa bu onay kutusunu işaretleyin. |
| Zorunlu | Seyahat durumunun atlanmaması amacıyla seyahat durumunu zorunlu hale getirmek için bu onay kutusunu işaretleyin. |
| Üst öğe | Durum değerleri arasında bir hiyerarşi oluşturmak için bu alanı kullanın. Seyahat durumları hiyerarşide üst durumlardan alt durumlara doğru yalnızca aşağı yönde değiştirilebilir (el ile veya otomatik olarak).

> [!NOTE]
> Yalnızca kuruluşunuzun kullandığı belirli seyahat durumlarını ayarlamanız gerekir. Tipik seyahat durumları arasında *Onaylandı*, *Taşımadaki Mallar*, *Teslim Alındı*, *Maliyetlendirilme için hazır* ve *Maliyetlendirildi* değerleri bulunur. Ancak başka durumlar da olabilir.
