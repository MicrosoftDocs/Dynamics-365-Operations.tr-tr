---
title: İş emirleri oluşturma
description: Bu konuda Varlık Yönetimi'nde iş emirleri oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922126"
---
# <a name="creating-work-orders"></a>İş emirleri oluşturma

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Önleyici bakım işleri planladığınızda sonraki adım işler için iş emirleri oluşturmaktır. Bu işlem, bakım zamanlamalarının birinde gerçekleştirilir. Bakım zamanlamasında zamanlanmış işler farklı referans türlerine sahip olabilir:

| Referans türü | Tanım                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| Bakım planları     | "Süre" veya "Sayaç" bakım planı türlerini temel alan önleyici bakım işleri.                       |
| Bakım sıraları    | Benzer bir bakım türü gerektiren birkaç varlığı içeren önleyici bakım işleri.           |
| Bakım talebi   | İş emrine dönüştürülebilecek bir varlığın el ile oluşturulan bakım veya onarım talebi. |


1. **Varlık yönetimi** > **Ortak** > **Tüm bakım zamanlaması** veya **Bakım zamanlaması satırları aç** veya **Bakım zamanlaması havuzları aç** öğesine tıklayın.

2. İş emri oluşturmak istediğiniz zamanlanmış bakım işlerini seçin ve **İş emri** öğesine tıklayın. **İş emirleri oluştur** iletişim kutusunda, seçili satırlar için toplam tahmini saat sayısı **Bakım tahmini saatleri** alanında gösterilir.

3. **Parametreler** bölümünde, kaç adet iş emri oluşturulacağını seçin. Her bir bakım zamanlaması satırı için bir iş emri veya **Şuna göre bir iş emri** bölümünde yaptığınız seçimlere göre birkaç iş emri oluşturabilirsiniz.

4. Oluşturduğunuz tüm iş emirlerinde kullanılacak bir **İş emri türü** seçin. Aşağıdaki çizimde **İş emirleri oluştur** iletişim kutusunun bir örneği gösterilmektedir.

![Şekil 1](media/18-preventive-maintenance.png)

5. **Tamam**'a tıklayın. Bir veya daha fazla iş emri oluşturulur.
