---
title: Bakım taleplerinden iş istekleri oluşturma
description: Bu konuda Kıymet Yönetimi'nde bakım taleplerinden iş istekleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847471"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Bakım taleplerinden iş istekleri oluşturma

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Bakım talepleri oluşturduktan sonra, bunları iş emirlerine kolayca dönüştürebilirsiniz. Bu konu, bakım talepleriyle çalışmak, aynı anda birkaç bakım talebi güncelleştirmek ve aynı anda birkaç bakım talebi için bir iş emri oluşturmak için en hızlı yolu açıklar. **Etkin bakım talepleri** veya **İşlem yapılacak yerleşim bakım talepleri** sayfasında, aynı anda bir bakım talebiyle çalışabilir ve bir bakım talebini bir iş emrine dönüştürebilirsiniz.

> [!NOTE]
> Her bakım talebi yalnızca bir iş emri ile ilgili olabilir. Ancak, bakım taleplerini farklı varlıklar olsa bile birden çok bakım talebi bir iş emrine dahil edilebilir.

1. **Varlık yönetimi** \> **Ortak** \> **bakım talepleri** \> **Tüm bakım talepleri**'ni seçin.
2. Bakım taleplerinden bir iş emri oluşturmadan önce, bu bilgiler ilgili ise bakım talepleri için en az bir bakım işi türü ve aynı zamanda bir bakım işi türü varyantı ve ticaret, seçmeniz gerekir. Kılavuz görünümünde, bakım talebinin bilgilerini kolayca güncelleştirebilirsiniz.
3. Bir iş emri oluşturmaya hazır olduğunuzda, içine dahil etmek için bakım taleplerini seçin.

    - İş emrini dönüştürmek için birkaç bakım talebi seçerseniz iş emrini oluşturmadan önce her iki **Varlık** alanı ve **Bakım iş türü** alanı ayarlanmalıdır.
    - İş emrini dönüştürmek için bir bakım talebi seçerseniz iş emrini oluşturmadan önce yalnızca **Varlık** alanının ayarlanması gerekir. Ancak, iş emrini oluşturduğunuzda, **İş emri oluştur** iletişim kutusunda bir bakım işi türü (ve bu bilgiler uygun ise, ilgili bakım iş türü varyantı ve ticaret) seçebilirsiniz.

4. **İş emri**'ni seçin.
5. **İş emri oluştur** iletişim kutusunda, alanları ayarlayın ve sonra **Tamam**'ı seçin.

    Bir ileti çubuğu, yeni bir iş emri oluşturulduğunu bildirebilir.

    Ayrıca, bir bakım talebini temel alan bir iş emri oluşturduğunuzda, bakım talebiyle ilgili varlık bir garanti sözleşmesine eklendiğinde, bir ileti çubuğu garanti anlaşması hakkında sizi uyarır.

6. **Varlık yönetimi** \> **Ortak** \> **İş emirleri** \> **Tüm iş emirleri**'ni seçin ve yeni iş emrini açın.

    ![Şekil 1](media/05-manage-maintenance-requests.png)

