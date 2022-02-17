---
title: Fatura günlüğüne ödeme planı uygulama
description: Bu konuda, satıcı fatura günlüğüne ödemenin nasıl ekleneceği açıklanmaktadır.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: bd288ac48ef59d8e2a4e0922aa652276dddb666d
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075590"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Fatura günlüğüne ödeme planı uygulama

[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Finance sürüm 10.0.25'te, satıcı fatura günlüğünde artık bir ödeme planı desteklenmektedir.

Bu işlevi kullanmak için Özellik yönetiminde **Fatura günlüğüne ödeme planı uygula** özelliğini etkinleştirmeniz gerekir.

Özellik etkinleştirildikten sonra, **Fatura günlüğü** sayfasına yeni bir **Ödeme planı** alanı eklenir. Bir fatura günlüğü satırı oluşturduğunuzda, ödeme koşulları satıcıda korunuyorsa ve ödeme planında ödeme koşulları seçiliyse **Ödeme planı** alanı **Fatura günlüğü** sayfasında güncelleştirilir.

İş gereksiniminize göre kullanılan ödeme planınızı değiştirebilirsiniz. Satıcı fatura günlüğünün deftere nakli sırasında, satıcı açık hareketleri ödeme planına göre oluşturulur.

Ödeme çizelgesinden oluşturulan birden çok satıcı açık hareketini gözden geçirmek için **Borç Hesapları \> Faturalar \> Açık satıcı faturaları**'na gidin ve fatura numarasını veya satıcı hesabını girin.

Ödeme zamanlamasını gözden geçirmek veya yapılandırmak için **Borç hesapları \> Ödeme kurulumu \> Ödeme planı**'na gidin.

Ödeme koşullarını yapılandırmak ve bir ödeme planı atamak için **Borç hesapları \> ödeme kurulumu \> Ödeme koşulları**'na gidin.

Bir satıcıdaki ödeme koşullarını korumak için **Borç hesapları \> Tüm satıcılar**'a gidin, satıcı hesabını seçin ve **Ödeme** sekmesinde **Ödeme koşulları** alanını ayarlayın.

Ödeme planı özelliği, **Satıcı faturası kaydı** işleminde de kullanılabilir. Fatura kayıt günlüğünde bir ödeme planı seçilirse, fatura kaydı deftere nakledildiğinde birden çok satıcı ödeme satırı **oluşturulmaz**. Fatura onaylandığında satıcı ödeme satırları oluşturulur.

## <a name="limitation"></a>Sınırlama

Bekleyen bir satıcı faturası için ödeme planı fatura başlığında varsa kullanıcıların ödeme satırlarını düzenlemesine izin veren gelişmiş bir sayfa vardır. (Örneğin, kullanıcılar her ödeme satırının son tarihini ve değerini düzenleyebilir.) Fatura günlüğünden oluşturulan ödeme satırları, ödeme planındaki değere sahip olur.

Bu işlevsellik, satıcı fatura günlüğü ve bekleyen faturalar için gelecekteki bir sürümde kullanılabilir.
