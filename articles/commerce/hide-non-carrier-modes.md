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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c06dfa697e3e0eab7a7f4183da9f178af818a6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206184"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Taşıyıcı dışı teslimat modlarını POS'taki sevkiyat seçeneklerinden gizleme


[!include [banner](includes/banner.md)]

Bu konuda, satış noktası (POS) uygulaması için kullanılabilen bir yapılandırma seçeneği açıklanmaktadır. Bu yapılandırma seçeneği, POS'ta sevkiyat emirleri oluşturulduğunda, teslim modunun seçimine ilişkin davranışı değiştirir.

Kullanıcılar POS 'ta müşteri sevkiyat emirleri oluştururken, sevkiyat için bir teslimat modu seçebilir. Bu işlev, siparişin tamamının mı yoka yalnızca seçili satırların mı sevk edileceğinden bağımsız olarak kullanılabilir.

Varsayılan olarak, bir teslimat modunun seçildiği iletişim kutusu bir kanal, madde ve teslimat adresi birleşimi için geçerli teslimat modlarını gösterir. Bu teslimat şekilleri Headquarters'taki **Teslimat şekli** sayfasında (**Satış ve pazarlama \> Kurulum \> Dağıtım \> Teslimat şekli**) tanımlanır. **Teslim alınan** veya **Çekme** gibi "taşıyıcı dışı" teslimat şekilleri de iletişim kutusunda seçim için görüntülenebilir.

Ancak, iletişim kutusunda taşıyıcı dışı teslimat şekillerini gizlemenize olanak sağlayan bir özellik eklenmiştir. Bu özelliği açmak için, **Commerce parametreleri** sayfasında **Müşteri siparişleri** sekmesinde **Sevk emirleri için yalnızca taşıyıcı modu seçeneklerini göster** seçeneğini **Evet** olarak ayarlayın. Bu özelliği açtıktan ve bilgileri kanal veritabanıyla eşitlemek için uygun dağıtım işlerini çalıştırdıktan sonra, POS'ta sevkiyat emri oluşturma işlemi sırasında, taşıyıcı dışı teslimat şekilleri seçim için görüntülenmez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]