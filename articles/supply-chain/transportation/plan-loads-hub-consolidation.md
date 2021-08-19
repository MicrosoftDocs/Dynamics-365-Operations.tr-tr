---
title: Hub birleştirme kullanarak yükleri planlamaya genel bakış
description: Bu makalede aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etme özelliği açıklanmaktadır.
author: MarkusFogelberg
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92273"
- intro-internal
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b1ec672caaa382c819a5f1d972604e46c4e6a5cdc3ade22e35102065706102bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728495"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Hub birleştirme kullanarak yükleri planlamaya genel bakış

[!include [banner](../includes/banner.md)]

Bu makalede aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etme özelliği açıklanmaktadır.

Aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etmek yararlı olabilir.

## <a name="building-loads"></a>Yük oluşturma
Hub konsolidasyonu özelliğini kullanabilmek için **Taşıma yönetimi parametreleri** sayfasında **Transit planlamada** seçeneğini etkinleştirmeniz gerekir. Ayrıca konsolidasyonun gerçekleşeceği hub'ları da oluşturmanız gerekir. Aşağıdaki diyagramda bir hub konsolidasyonu örneği gösterilmektedir. Bu örnekte, farklı ambarlardan alınan satış siparişleri aynı müşteriye gönderilecek. Temel yükler satış siparişlerine göre her zamanki yöntemle, **Yük planlama çalışma ekranı** sayfasında oluşturulur. İki yükü müşteriye teslim edilmeden önce bir hub'da konsolide etmek için, **Yük planlama çalışma ekranı** sayfasında, **Taşıma** alanında **Hub konsolidasyonu** seçeneğini belirleyin. Her yük için doğru hub'ı seçtiğinizde, yüklerin "bırakma" hedefi olarak bu hub görünür. Ayrıca **Yük planlama çalışma ekranı** sayfasındaki **Arz ve Talep** bölümünde iki "taşıma talebi satırı" bulunur. Bundan sonra bu iki satırı yeni bir yüke ekleyebilirsiniz. Bu yeni yük iki satış siparişi satırını da içerir ve "alma" adresi olarak hub "bırakma" hedefi olarak da müşteri A görünür. Üç yük bundan sonra derecelendirilmeye ve diğer yükler gibi rotalarının belirlenmesine hazırdır. Her yük için sistemin önerdiği sevkiyat taşıyıcısını seçebilirsiniz. [![Hub konsolidasyonu.](./media/hubconsol.jpg)](./media/hubconsol.jpg) Aynı yöntemi birden çok transfer emrine ait yükleri konsolide etmek için de kullanabilirsiniz. Bu örnekte, önceki diyagramdaki müşteri A ambardır. Alternatif olarak yüklerin farklı satıcılardan aynı ambara teslim edildiği, birden fazla satınalma emrine ilişkin yükleri de konsolide edebilirsiniz. Birden fazla konsolidasyon hub'ı oluşturabilir ve farklı ambarlardan gelen daha fazla yük için birden fazla hub'ı konsolide edebilirsiniz. Temel yüklerinizi oluşturup hub konsolidasyon seçeneğini kullandıktan sonra, konsolide edilmiş taşıma istekleri satırını kullanarak yeni yükler oluşturabilirsiniz. Bundan sonra yüklerinizi derecelendirebilir ve rotalarını belirleyebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]