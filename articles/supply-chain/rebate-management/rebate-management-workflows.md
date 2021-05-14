---
title: İndirim yönetimi anlaşması iş akışları
description: Bu konu, bir Indirim yönetimi anlaşma iş akışının anlaşmaları onaylamak ve etkinleştirmek için nasıl ayarlanacağını açıklamaktadır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 16f1c56ecd69f4dc7bfd80e74d3f35147cc173d6
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919831"
---
# <a name="rebate-management-deal-workflows"></a>İndirim yönetimi anlaşması iş akışları

[!include [banner](../includes/banner.md)]

İndirim anlaşmalarını onaylamak için, İndirim yönetimi, diğer Finance and Operations uygulamalarıyla aynı iş akışı platformunu kullanır. İki iş işlemi her iş akışı ile ilişkilendirilmiştir:

- İş akışının bir öğesi, Kullanıcı veya iş akışı işleminin hareketleri onaylaması için, anlaşmayı etkinleştirir.
- İş akışının bir öğesi anlaşmayı onaylar.

İndirim anlaşması kullanabilmeniz için, bunun **indirim Yönetimi** modülünde etkin olması gerekir. Bir anlaşmayı etkinleştirmek için önce bir *indirim yönetimi anlaşma iş akışı* oluşturmalı ve konfigüre etmelisiniz.

İndirim yönetimi için iş akışı etkinleştirildikten sonra, kullanıcılar anlaşmaları el ile onaylayamaz. İş akışının her zaman kullanılması gereklidir.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>İndirim yönetimi anlaşması iş akışlarını oluşturma ve yönetme

İndirim yönetimi anlaşması iş akışlarıyla çalışmak için, **indirim Yönetimi \>kurulum \> indirim yönetimi iş akışlarına** gidin. Burada, iş akışlarını gerektiği gibi görüntüleyebilir, oluşturabilir ve güncelleştirebilirsiniz. Aynı anda yalnızca bu türdeki bir iş akışı etkin olabilir. İş akışları hakkında daha fazla bilgi için, **indirim yönetimi iş akışları** sayfası ile nasıl çalışılacağı ve iş akışlarının nasıl oluşturulacağını öğrenmek için [iş akışı sistemine genel bakışa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ve ilgili konularına bakın.

## <a name="use-a-workflow-to-activate-a-deal"></a>Anlaşmayı etkinleştirmek için iş akışı kullanma

Bir iş akışı üzerinden bir anlaşmayı etkinleştirmek için, anlaşmayı açın (örneğin, **tüm indirim yönetimi anlaşmaları** sayfasında). Ardından Eylem bölmesinden **İş akışı \> Gönder**'i seçin. Yeni anlaşma iş akışı ile işlendikten ve onaylandıktan sonra, etkin ve kullanıma hazır olur.

Bir anlaşma etkinleştirildikten sonra, kurulumunu değiştiremezsiniz. Etkin bir anlaşmayı değiştirmeniz gerekiyorsa, bunu devre dışı bırakın ve sonra yeni bir anlaşma oluşturun. Yeni anlaşma eski anlaşmayı benziyorsa, eski anlaşmayı kopyalayarak bunu oluşturabilirsiniz.
