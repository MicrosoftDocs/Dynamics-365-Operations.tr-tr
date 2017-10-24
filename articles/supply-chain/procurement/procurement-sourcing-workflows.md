---
title: "Tedarik ve kaynak atama iş akışları"
description: "Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Tedarik ve kaynak atama iş akışları

[!include[banner](../includes/banner.md)]


Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.

İş akışı, bir iş sürecini temsil eder. Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar. İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:
-   **Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz. İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.
-   **Süreç görünürlüğü** — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.
-   **Merkezi iş listesi**— Kullanıcılar, iş akışı görevlerini ve katıldıkları tüm iş akışları boyunca kendilerine atanmış onayları görüntülemek için merkezi bir iş listesini görüntüleyebilirler. Bu iş öğelerini sayfasında mevcuttur.

## <a name="the-types-of-workflows-that-you-can-create"></a> Oluşturabileceğiniz iş akışı türleri
Aşağıdaki iş akışı türleri, Tedarik ve kaynak atama için kullanılabilir.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tip**                         | **Bu türü aşağıdakileri gerçekleştirmek için kullanın:**                                          |
| Satınalma talebi incelemesi      | Satınalma talepleri için gözden geçirme iş akışları oluşturun.            |
| Satınalma talep satırı gözden geçir | Satınalma talebi satırları için gözden geçirme iş akışları oluşturun.       |
| Satınalma siparişi iş akışı          | Satınalma siparişleri için gözden geçirme ve onay iş akışları oluşturun.     |
| Satınalma sipariş satırı iş akışı     | Satınalma siparişi satırları için gözden geçirme ve onaylama iş akışları oluşturun. |

## <a name="creating-a-workflow"></a>İş akışı oluşturma
Bir iş akışı oluşturmak için, Tedarik ve kaynak atama &gt; Kurulum &gt; Tedarik ve kaynak atama iş akışları menüsüne gidin ve oluşturmak istediğiniz iş akışı türünü seçerek yeni bir iş akışı oluşturun.  

İş akışı tuvallerinde, iş akışı öğelerini tasarımcıya sürükleyebilir ve öğeleri bir akışa bağlayabilirsiniz. İş akışı öğeleri yapılandırılmalıdır. Onay ve görev iş akışı öğeleri için hangi katılımcının eylemi gerçekleştirmesi gerektiğini yapılandırabilirsiniz.
 Katılımcı türleri
----------------------

Aşağıdaki katımcı gruplarına bir onay adımı atayabilirsiniz.

| Kullanıcı grubu    | Açıklama                                                               |
|---------------|---------------------------------------------------------------------------|
| Katılımcı   | Bir grubun veya rolün üyelerine onay adımı atayın.                   |
| Hiyerarşi     | Belirli bir organizasyonel hiyerarşideki kullanıcılara onay adımı atayın. |
| İş akışı kullanıcısı | Bu iş akışının kullanıcılarına onay adımı atayın.                       |
| Kuyruk         | Onay adımını bir çalışma öğesi kuyruğa atayın.                            |
| Kullanıcı          | Onay adımını belirli kullanıcılara atayın.                               |



<a name="see-also"></a>Ayrıca bkz.
--------

[Satınalma talepleri için iş süreci iş akışları tanımlama](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Satınalma talebi iş akışı](purchase-requisitions-workflow.md)




