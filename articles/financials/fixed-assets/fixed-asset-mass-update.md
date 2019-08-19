---
title: Sabit kıymet toplu olarak güncelleştirme
description: Defterleri kullanıyorsanız, aynı defterlerin parçası olan kıymet grupları için amortisman yöntemlerini değiştirebilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b9aaaabcac09c9147c350422924a23f785c0ce
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840421"
---
# <a name="fixed-asset-mass-update"></a>Sabit kıymet toplu olarak güncelleştirme

[!include [banner](../includes/banner.md)]

Defterleri kullanıyorsanız, aynı defterlerin parçası olan kıymet grupları için amortisman yöntemlerini değiştirebilirsiniz.

Örneğin, ABD'deyseniz ve kıymetlerinizin yüzde 40'ından fazlasını yılın dördüncü çeyreği sırasında hizmete soktuysanız, çeyrek ortası amortisman yöntemini kullanmanız gerekir. Yeni amortisman yöntemi gerektiren tüm kıymetleri değiştirmek için toplu güncelleştirme süresini kullanabilirsiniz. 

Kıymetler için amortisman dönüştürmeyi güncelleştirdiğinizde, bu kıymetler için mevcut olan tüm amortisman hareketleri silersiniz. Ayrıca amortisman ayarları için tüm hareketleri, ek amortisman için hareketleri ve bu varlıklar için olağandışı amortisman hareketlerini de silersiniz. 

Zaten elden çıkarılmış kıymetlerin amortisman yöntemini güncelleştirmek için, mevcut elde çıkarma hareketlerini silmeniz gerekir. Ayrıca, elden çıkarma süreci nedeniyle oluşturulan tüm hareketlerini de silmeniz gerekir. 

Kıymetler için amortisman dönüştürmeyi güncelleştirdiğinizde her kıymet için amortismanı ve olağandışı amortismanı işleyebilirsiniz. Ayrıca, gerekirse el ile amortisman düzeltmeleri de yapabilirsiniz.





