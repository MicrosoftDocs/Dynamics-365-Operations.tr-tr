---
title: Varış yeri maliyeti için satın alma ve tedarik parametreleri
description: Bu makalede, Varış yeri maliyeti modülünü kullandığınızda ilgili Satın alma ve tedarik parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905993"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Varış yeri maliyeti için satın alma ve tedarik parametreleri

[!include [banner](../../includes/banner.md)]

**Satın alma ve tedarik parametreleri** sayfasında, özellikle **Varış yeri maliyeti** modülünü kullandığınızda ilgili olan birkaç ayar vardır. Satın alma siparişi başlığında değişiklik yapıldığında satın alma siparişi satırlarının otomatik olarak güncelleştirilip güncelleştirilmeyeceğini belirtmek için **Satın alma ve tedarik parametreleri** sayfasından açılan **Sipariş satırlarını güncelleştir** iletişim kutusunu kullanın.

Bu kurulumu tamamlamak için bu adımları izleyin.

1. **Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin.
1. **Genel** sekmesinde **Sipariş satırlarını güncelleştir** bağlantısını seçin.
1. **Sipariş satırlarını güncelleştir** iletişim kutusu, sipariş başlığında, sipariş satırlarındaki ilgili alanlara otomatik güncelleştirmeler de uygulayabilen alanları listeler. Listedeki her alanı aşağıdaki değerlerden birine ayarlayın:

    - **Her zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları otomatik olarak güncelleştirilmelidir.
    - **Hiçbir zaman**: Sipariş başlığı güncelleştirildiğinde sipariş satırları hiçbir zaman güncelleştirilmemelidir.
    - **İstem**: Kullanıcıdan sipariş satırlarının güncelleştirilip güncelleştirilmeyeceğini seçmesi istenir.
