---
title: İndirim yönetimi anlaşması iş akışları
description: Bu makale, bir Indirim yönetimi anlaşma iş akışının anlaşmaları onaylamak ve etkinleştirmek için nasıl ayarlanacağını açıklamaktadır.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4f0590c4c906e746b54ac30fd6531b8c1cd67915
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067347"
---
# <a name="rebate-management-deal-workflows"></a>İndirim yönetimi anlaşması iş akışları

[!include [banner](../includes/banner.md)]

İndirim anlaşmalarını onaylamak için İndirim yönetimi, diğer finans ve operasyon uygulamalarıyla aynı iş akışı platformunu kullanır. İki iş işlemi her iş akışı ile ilişkilendirilmiştir:

- İş akışının bir öğesi anlaşmayı onaylar.
- İş akışının bir öğesi, Kullanıcı veya iş akışı işleminin hareketleri onaylaması için, anlaşmayı etkinleştirir.

İndirim anlaşması kullanabilmeniz için, bunun **indirim Yönetimi** modülünde etkin olması gerekir. Bir anlaşmayı etkinleştirmek için önce bir *indirim yönetimi anlaşma iş akışı* oluşturmalı ve konfigüre etmelisiniz.

Kullanıcılar fırsatları el ile onaylayamaz. İş akışının her zaman kullanılması gereklidir.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>İndirim yönetimi anlaşması iş akışlarını oluşturma ve yönetme

İndirim yönetimi anlaşması iş akışlarıyla çalışmak için, **indirim Yönetimi \>kurulum \> indirim yönetimi iş akışlarına** gidin. Burada, iş akışlarını gerektiği gibi görüntüleyebilir, oluşturabilir ve güncelleştirebilirsiniz. Aynı anda yalnızca bu türdeki bir iş akışı etkin olabilir. İş akışları hakkında daha fazla bilgi için, **indirim yönetimi iş akışları** sayfası ile nasıl çalışılacağı ve iş akışlarının nasıl oluşturulacağını öğrenmek için [iş akışı sistemine genel bakışa](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) ve ilgili makalelerine bakın.

## <a name="use-a-workflow-to-activate-a-deal"></a>Anlaşmayı etkinleştirmek için iş akışı kullanma

Bir iş akışı üzerinden bir anlaşmayı etkinleştirmek için, anlaşmayı açın (örneğin, **tüm indirim yönetimi anlaşmaları** sayfasında). Ardından Eylem bölmesinden **İş akışı \> Gönder**'i seçin. Yeni anlaşma iş akışı ile işlendikten ve onaylandıktan sonra, etkin ve kullanıma hazır olur.

Bir anlaşma etkinleştirildikten sonra, kurulumunun büyük bölümünü değiştiremezsiniz. Etkin bir anlaşmayı değiştirmeniz gerekiyorsa, önce bunu devre dışı bırakın ve sonra yeni bir anlaşma oluşturun. Yeni anlaşma eski anlaşmayı benziyorsa, eski anlaşmayı kopyalayarak bunu oluşturabilirsiniz.

Bir anlaşma etkinleştirildikten sonra aşağıdaki ayarları değiştirebilirsiniz:

- Mutabakat ölçütü
- Kümülatif garanti
- Deftere nakil profili
- Garanti için nakil profili
- Belge notları
- Para Birimi
- Başlangıç tarihi
- Bitiş tarihi

Ayrıca, indirim satırları kaldırılabilir.

