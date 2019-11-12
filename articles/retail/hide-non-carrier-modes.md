---
title: Taşıyıcı dışı teslimat modlarını POS'taki sevkiyat seçeneklerinden gizleme
description: Bu konu, satış noktasında (POS) sevkiyat emirleri oluşturulurken, taşıyıcı dışı teslimat modlarının seçim için görüntülenmesini engelleyebilecek bir yapılandırma seçeneği açıklamaktadır.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659033"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Taşıyıcı dışı teslimat modlarını POS'taki sevkiyat seçeneklerinden gizleme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, satış noktası (POS) uygulaması için kullanılabilen bir yapılandırma seçeneği açıklanmaktadır. Bu yapılandırma seçeneği, POS'ta sevkiyat emirleri oluşturulduğunda, teslim modunun seçimine ilişkin davranışı değiştirir.

Kullanıcılar POS 'ta müşteri sevkiyat emirleri oluştururken, sevkiyat için bir teslimat modu seçebilir. Bu işlev, siparişin tamamının mı yoka yalnızca seçili satırların mı sevk edileceğinden bağımsız olarak kullanılabilir.

Varsayılan olarak, bir teslimat modunun seçildiği iletişim kutusu bir kanal, madde ve teslimat adresi birleşimi için geçerli teslimat modlarını gösterir. Bu teslimat şekilleri Retail Headquarters'taki **Teslimat şekli** sayfasında tanımlanır (**Satış ve pazarlama \>Kurulum \> Dağıtım \>Teslimat şekli**). **Teslim alınan** veya **Çekme** gibi "taşıyıcı dışı" teslimat şekilleri de iletişim kutusunda seçim için görüntülenebilir.

Ancak, iletişim kutusunda taşıyıcı dışı teslimat şekillerini gizlemenize olanak sağlayan bir özellik eklenmiştir. Bu özelliği açmak için, **Perakende parametreleri** sayfasında **Müşteri siparişleri** sekmesinde **Sevk emirleri için yalnızca taşıyıcı modu seçeneklerini göster** seçeneğini **Evet** olarak ayarlayın. Bu özelliği açtıktan ve bilgileri kanal veritabanıyla eşitlemek için uygun dağıtım işlerini çalıştırdıktan sonra, POS'ta sevkiyat emri oluşturma işlemi sırasında, taşıyıcı dışı teslimat şekilleri seçim için görüntülenmez.
