---
title: Taşıma yönetimi durumları
description: Bu konuda, bir taşıma durumunun nasıl oluşturulacağı ve o durumun bir taşıyıcı durumuna nasıl eşleneceği açıklanmaktadır.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c5570d3b5b436a35bb57d051bc06cde8b78934e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569901"
---
# <a name="transportation-management-statuses"></a>Taşıma yönetimi durumları

[!include [banner](../includes/banner.md)]

Sevkiyat taşıyıcılarınız tarafından sağlanan kodları yorumlamak üzere taşıma durumları için ana kodları ayarlayın. Bu, durum sağlamak için sevkiyat taşıyıcıları ile tümleştirme yapmanıza olanak sağlar. Taşıma ana durum kodu için sağladığınız taşıma durumu; yük, sevkiyat veya konteyner durumunu izlemenize yardımcı olabilir. Bir yük, sevkiyat veya konteyner için belirli bir taşıma durumu yalnızca veri tümleştirmesi aracılığıyla güncelleştirilebilir ve kullanıcı arabirimi aracılığıyla el ile yapılamaz.

## <a name="create-a-transportation-status"></a>Taşıma durumu oluşturma

Taşıma durumu oluşturmak için şu adımları izleyin:

1. **Taşımacılık yönetimi \> Kurulum \> Taşıma ana durumları** seçeneğine gidin.
1. Taşıma ana durumu oluşturmak için **Yeni**'yi seçin.
1. **Taşıma ana durumu** alanında, taşıma durumu için benzersiz bir kod girin.
1. **Taşıma türü** alanında, taşıma türü olarak *Sevkiyat taşıyıcısı* veya *Hub*'ı seçin.
1. Bir ad ve taşıma durumu girin.
1. Sayfayı kapatın.

## <a name="map-a-transportation-status-to-a-carrier-status"></a>Taşıma durumunu bir taşıyıcı durumuna eşleme

Taşıma durumunu bir taşıyıcı durumuna eşlemek için şu adımları izleyin:

1. **Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Taşıyıcı taşıma durumu** seçeneğine gidin.
1. Sevkiyat taşıyıcısı kodunu taşıma durumu ana koduyla eşlemek için **Yeni**'yi seçin.
1. Sevkiyat taşıyıcısı ve taşıyıcı hizmeti için benzersiz kodu seçin.
1. Seçili sevkiyat taşıyıcısı koduyla eşleştirmek istediğiniz taşıma durumu kodunu seçin.
1. Sevkiyat taşıyıcısı tarafından kullanılan harici kodu girin.
1. Sayfayı kapatın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]