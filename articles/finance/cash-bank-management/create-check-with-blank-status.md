---
title: Boş durumunda olan çek oluşturma
description: Bu konuda, Çekler sayfasında bir banka hesabı için boş çeklerin nasıl oluşturulacağı açıklanmaktadır.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: af79dd4831f2e7fc71c296922d73a9e42f7955b3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176123"
---
# <a name="create-checks-that-have-blank-status"></a>Boş durumunda olan çek oluşturma

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, boş çeklerin nasıl oluşturulacağı açıklanmaktadır. Örneğin, zarar görmüş ve ödeme için kullanılamayacak bir çek kaydetmek üzere boş bir çek oluşturabilirsiniz.

**Çekler** sayfasında, çekler için bakım görevleri gerçekleştirebilirsiniz. Örneğin, yeni çek numaraları oluşturabilir ve çekleri silebilirsiniz. Ayrıca **Boş** durumunda olan çekler de oluşturabilirsiniz. Boş çekler oluşturulduktan sonra sistemde silinemez veya yeniden kullanılamaz.

> [!NOTE]
> Bu özellik yalnızca **Özellik yönetimi** sayfasında **Çekler sayfasında boş durumunda olan çek oluştur** özelliğini açarsanız **Çekler** sayfasında kullanılabilir. Özellik açılmazsa **Boş** durumunda olan çekler yalnızca Borç hesaplarında ödeme oluşturma işlemi sırasında **Çekle ödeme** iletişim kutusundan oluşturulabilir.

**Çekler** sayfasını açmak için **Nakit ve banka yönetimi \> Banka hesapları \> Banka hesapları**'na gidin ve ardından Eylem Bölmesi'ndeki **Ödemeleri yönetme** sekmesinin **İlgili bilgiler** grubunda **Çekler**'i seçin. Alternatif olarak, **Nakit ve banka yönetimi \> Sorgular ve raporlar \> Çekler**'e gidin.

Ardından **Boş** durumunda olan çek oluşturmak için Eylem Bölmesi'nde **Boş çek oluştur**'u seçin. Sistem boş çek oluştururken ilişkili banka hesabı geçici olarak devre dışı bırakılır. Bu davranış, boş çekler oluşturulurken aynı anda ödemelerin de oluşturulması riskini azaltır. İşlem tamamlandığında ilişkili banka hesabı yeniden etkinleştirilir.
