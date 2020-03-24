---
title: Kaldırılan veya artık kullanılmayan Platform özellikleri
description: Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095786"
---
# <a name="removed-or-deprecated-platform-features"></a>Kaldırılan veya artık kullanılmayan Platform özellikleri

[!include [banner](../includes/banner.md)]

Bu konu, Finance and Operations uygulamalarının platofrm güncellemelerinde kaldırılmış veya kaldırılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır. 

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="platform-update-32"></a>Platform güncelleştirmesi 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>İş akışı isteği değişikliği iletişim kutusu artık kullanıcı seçimi açılan listesini içermiyor
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Değişiklik isteği istenmeyen bir kullanıcıya gönderilebileceğinden bu bir güvenlik sorunudur. Bu aynı zamanda bir kullanılabilirlik sorunudur ve kullanıcıyı iş akışının kaynağını belirlemeye ve bunları el ile seçmelerine olanak sağlar.  |
| **Başka bir özellikle mi değiştirildi?**   | Hayır |
| **Etkilenen ürün alanları**         | İş akışı |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Kullanıcı seçimi açılan listesi, platform güncelleştirmesi 32 ' deki istek değişimi iletişim kutusundan kaldırıldı. İstek değişikliği istekleri oluşturana otomatik olarak istendiği gibi gönderilecek. Bu işlevsellik hakkında daha fazla bilgi için bkz [İş akışı onay sürecindeki eylemler](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Katıştırılmış ayrıntılandırma bağlantıları bulut tarafından barındırılan hizmet tarafından işlenen sayfalandırılmış belgelerde artık desteklenmiyor 
|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Hizmet tarafından işlenen belgelere katıştırılmış olan gezinti URL'leri hassas iş verileri içerebilir. Müşteri verilerini daha iyi korumak amacıyla bir güvenlik önlemi olarak belgelerdeki katıştırılmış ayrıntılandırma bağlantıları için desteği kaldırıyoruz. Kullanıcılar ayrıca, bu değişikliğin sonucunda etkileşimli olarak belge oluştururken gelişmiş performanstan da yararlanacaktır.  |
| **Başka bir özellikle mi değiştirildi?**   | No |
| **Etkilenen ürün alanları**         | Raporlama |
| **Dağıtım seçeneği**              | Tümü |
| **Durum**                         | Bu özellik, hizmetten etkin olarak kaldırılmaktadır.<br><br>Modern istemci, uygulamada gezinme konusunda yardımcı olacak otomatik oluşturulmuş bağlantılar içeren görünümler üretmek için birçok seçenek sunar. Hizmet tarafından işlenen sayfalandırılmış belgeler e-postayla gönderilen, arşivlenen ve alıcılar için yazdırılan harici iletişimler için önerilir. Belgeleri doğrudan tarayıcıda önizleme deneyimini geliştirdik (yerel yazıcılara doğrudan erişim sunar). Daha fazla bilgi için bkz. [Katıştırılmış görüntüleyiciyle PDF belgelerini önizleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular
Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../migration-upgrade/deprecated-features.md) bakın.

