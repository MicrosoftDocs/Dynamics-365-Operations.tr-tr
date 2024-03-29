---
title: Barkod tarayıcıları için Kanban transfer panosu desteği
description: Kanban transfer panosu bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b18aad4dcdbf8c2d18960ae306556c3ea679d622
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566823"
---
# <a name="kanban-transfer-board-support-for-bar-code-scanners"></a>Barkod tarayıcıları için Kanban transfer panosu desteği

[!include [banner](../includes/banner.md)]

Kanban transfer panosu bir kanban işini Seçmek, Başlatmak, Tamamlamak ve Boşaltmak için bir pencere öğesi barkod tarayıcısından tarayıcı girişini destekler.

## <a name="registration-modes"></a>Kayıt modları

**Tarayıcı kaydı** FastTab sekmesinde, bir kanban kart numarasını seçtiğinizde veya manuel olarak numarayı Kanban kart numarası alanına yazdığınızda eylemi kontrol eden kayıt modunu seçebilirsiniz.

| Kayıt modu ayarla | Açıklama                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Başlangıç                 | Bir Kanban transfer işini devam eden olarak kaydeder.                                                 |
| Tam              | Bir Kanban transfer işini tamamlandı olarak kaydeder.                                                   |
| Boşalt                 | Bir Kanban kartının referans verdiği malzeme işleme birimini boş olarak kaydeder.              |
| Seç                | Bir Kanban kart numarası kaydeder ve referans verilen işi Kanban listesinde otomatik olarak seçer. |

 
## <a name="registration-mode-select"></a>Kayıt modu Seç

İş seçmek için barkod okuyucuyu kullandığınızda, kanban panosunun görüntüleme modu değişir. Bu modda, aşağıdaki koşullar geçerlidir:

-   Yalnızca taranan kanban işi görüntülenir.
-   Seçilen işin ayrıntıları **Ayrıntılar** FastTab'inde görüntülenir.
-   **İletiler** FastTab'i, yalnızca seçilen işin iletilerini görüntüler.
-   İşin durumunu, Eylem Bölmesi'nde bulunan işlevleri kullanarak değiştirebilirsiniz. Kanban transfer panosu, bu süre boyunca yalnızca tek bir işi görüntülemeye devam eder.
-   İşler listesindeki bilgileri Eylem Bölmesi'ndeki **Yenile** (Shift+F5) seçeneğini tıklayarak el ile güncelleyebilirsiniz. Bilgileri güncelledikten sonra, iş filtresi için tüm sonuçlar yeniden görüntülenir.

## <a name="job-status-and-possible-actions"></a>İş durumu ve olası eylemler
İşi daha fazla işleyip işleyemeyeceğinizi, seçilen işin durumu ve etkinlik kanban'ları için ilişkilendirilmiş işlerin durumu belirler. Aşağıdaki tabloda bu durum ve görevler hakkındaki bilgiler görüntülenmektedir:
-   İşler için kullanılabilir durumdaki veya işlerin referans verdiği işleme birimlerine yönelik durumlar.
-   İş için gerçekleştirebileceğiniz her bir görev.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>İş türü</th>
<th>İş durumu veya işleme birimi durumu</th>
<th>Malzeme çekme listesini güncelleştir</th>
<th>Başlangıç</th>
<th>Kaydı güncelleştir</th>
<th>Tam</th>
<th>Boşalt</th>
<th>Olay kanbanları oluştur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Transfer et</td>
<td><ul>
<li>Planlanmadı</li>
<li>İlişkilendirilmiş iş yok veya ilişkilendirilmiş işler Tamamlanmış</li>
</ul></td>
<td>Evet</td>
<td>Evet</td>
<td>Evet</td>
<td>Evet</td>
<td>Hayır</td>
<td>Evet</td>
</tr>
<tr class="even">
<td>Transfer et</td>
<td><ul>
<li>Planlanmadı</li>
<li>İlişkilendirilmiş iş Tamamlanmamış</li>
</ul></td>
<td>Evet</td>
<td>Hayır</td>
<td>Evet</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="odd">
<td>Transfer et</td>
<td>Devam ediyor</td>
<td>Evet</td>
<td>Hayır</td>
<td>Evet</td>
<td>Evet</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="even">
<td>Transfer et</td>
<td>Tamamlandı</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Evet</td>
<td>Hayır</td>
</tr>
<tr class="odd">
<td>Transfer et veya işle</td>
<td>Boşalt</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="even">
<td>Transfer et veya işle</td>
<td>Kanban kartı bulunamadı</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="odd">
<td>Transfer et veya işle</td>
<td>Kanban kartı bulundu, ancak bir kanbana atanmamış</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="even">
<td>İşle</td>
<td><ul>
<li>Planlanmadı</li>
<li>Hazırlandı</li>
<li>Devam ediyor</li>
</ul></td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
<tr class="odd">
<td>İşle</td>
<td>Tamamlandı</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
<td>Hayır</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]