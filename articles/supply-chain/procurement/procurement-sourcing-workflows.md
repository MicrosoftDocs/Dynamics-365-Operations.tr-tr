---
title: Tedarik ve kaynak atama iş akışları
description: Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909243"
---
# <a name="procurement-and-sourcing-workflows"></a>Tedarik ve kaynak atama iş akışları

[!include [banner](../includes/banner.md)]

Bazı kuruluşlar satınalma taleplerinin ve satınalma siparişlerinin hareketi giren kişiden başka bir kullanıcı tarafından onaylanmasını gerektirir. Bir onay sürecini ayarlamak için iş akışı oluşturabilirsiniz.

İş akışı, bir iş sürecini temsil eder. Bir belgenin sistem üzerinde nasıl aktığını tanımlar ve bir görevi kimin tamamlaması veya bir belgeyi kimin onaylaması gerektiğini tanımlar. İş akışı sistemini kuruluşunuzda kullanmanın bazı getirileri vardır:

- **Tutarlı süreçler** — Satınalma talepleri ve gider raporları gibi belirli belgelerin onay sürecini tanımlayabilirsiniz. İş akışı sistemini kullanmak, belgelerin tutarlı ve verimli şekilde işlenmesine ve onaylanmasına yardımcı olur.
- **Süreç görünürlüğü** — Belirli bir iş akışı örneğinin durumunu, geçmişini ve performans ölçülerini takip edebilirsiniz. Bu da iş akışının verimliliği yükseltmesi için değişiklikler yapılması gerekli olup olmadığını belirlemenize yardımcı olur.
- **Merkezi iş listesi**— Kullanıcılar, iş akışı görevlerini ve katıldıkları tüm iş akışları boyunca kendilerine atanmış onayları görüntülemek için merkezi bir iş listesini görüntüleyebilirler. Bu iş öğelerini sayfasında mevcuttur.

## <a name="the-types-of-workflows-that-you-can-create"></a>Oluşturabileceğiniz iş akışı türleri

Aşağıdaki iş akışı türleri, Tedarik ve kaynak atama için kullanılabilir.

| Türü | Bu türü aşağıdakileri gerçekleştirmek için kullanın: |
|---|---|
| Satınalma talebi incelemesi | Satınalma talepleri için gözden geçirme ve onay iş akışları oluşturun. |
| Satınalma talep satırı gözden geçir | Satınalma talebi satırları için gözden geçirme ve onay iş akışları oluşturun. |
| Satınalma siparişi iş akışı | Satınalma siparişleri için gözden geçirme ve onay iş akışları oluşturun. |
| Satınalma sipariş satırı iş akışı | Satınalma siparişi satırları için gözden geçirme ve onaylama iş akışları oluşturun. |
| Satıcı uygulama ekleme iş akışı | Satıcı talepleri aracılığıyla yeni satıcılar eklemek için gözden geçirme ve onay iş akışları oluşturun. |

> [!IMPORTANT]
> Yeni bir iş akışı eklerken, **İş akışı oluştur** iletişim kutusunda listelenmiş olan aşağıdaki geçersiz iş akışlarını da görebilirsiniz. Bunlar, [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows)'de bulunan fakat artık kullanımdan kaldırılan *giriş onayı* işleviyle ilgilidir. Bu iş akışları şu anda desteklenmemektedir.
> 
> - Teslimat tarihi bildirimi iş akışı
> - Fatura alındı bildirimi iş akışı
> - İş akışı bildirim ürün bilgisi başarısız oldu
> - Onaylanmayan ürün giriş ret bildirimi iş akışı

## <a name="creating-a-workflow"></a>İş akışı oluşturma

Bir iş akışı oluşturmak için, Tedarik ve kaynak atama &gt; Kurulum &gt; Tedarik ve kaynak atama iş akışları menüsüne gidin ve oluşturmak istediğiniz iş akışı türünü seçerek yeni bir iş akışı oluşturun. 

İş akışı tuvallerinde, iş akışı öğelerini tasarımcıya sürükleyebilir ve öğeleri bir akışa bağlayabilirsiniz. İş akışı öğeleri yapılandırılmalıdır. Onay ve görev iş akışı öğeleri için hangi katılımcının eylemi gerçekleştirmesi gerektiğini yapılandırabilirsiniz.

## <a name="types-of-participants"></a>Katılımcı türleri

Aşağıdaki katımcı gruplarına bir onay adımı atayabilirsiniz.

| Kullanıcı grubu | Açıklama |
|---|---|
| Katılımcı | Bir grubun veya rolün üyelerine onay adımı atayın. |
| Hiyerarşi | Belirli bir organizasyonel hiyerarşideki kullanıcılara onay adımı atayın. |
| İş akışı kullanıcısı | Bu iş akışının kullanıcılarına onay adımı atayın. |
| Kuyruk | Onay adımını bir çalışma öğesi kuyruğa atayın. |
| Kullanıcı | Onay adımını belirli kullanıcılara atayın. |

## <a name="additional-resources"></a>Ek kaynaklar

- [Satınalma talepleri için iş süreci iş akışları tanımlama](https://www.microsoft.com/download/details.aspx?id=101821)
- [Satınalma talebi iş akışı](purchase-requisitions-workflow.md)
- [Satıcıları işe alma](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]