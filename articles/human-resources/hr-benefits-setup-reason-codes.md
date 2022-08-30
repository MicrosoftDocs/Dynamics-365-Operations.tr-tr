---
title: Neden kodlarını ayarla
description: Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 692bd5acd574492526644849fb555e5856b4463f
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323434"
---
# <a name="set-up-reason-codes"></a>Neden kodlarını ayarla

Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.

> [!NOTE]
> Ocak 2021 itibarıyla, neden kodları **Kazanç yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçirildi. Daha fazla bilgi için, bkz. [Neden kodlarını el ile Personel yönetimine geçirme](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Neden kodları oluşturma

1. **Personel yönetimi** çalışma alanında (veya neden kodlarınız geçirilmediyse **Kazanç yönetimi** çalışma alanında) **Bağlantılar**'ı seçin ve ardından **Neden kodları** seçeneğini belirleyin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Neden kodu** | Bir çalışanın bir kazanç planı kaydını değiştiren nedenini tanımlamak için benzersiz ad. |
   | **Açıklama** | Neden kodunun açıklaması. |

4. **Uygulanabilir senaryolar** altında, **Yan hak yönetimi**'ni **Evet** olarak ayarlayın. (Neden kodlarınız **Personel yönetimi** çalışma alanına geçirilmediyse geçerli değildir.)

5. **Kaydet**'i seçin.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Neden kodlarını Personel yönetimine el ile geçirme

Ocak 2021'de, neden kodları **Kazanç yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçirildi. Çoğu neden kodu verileri ortamınıza otomatik olarak geçiş yapacaktır. Bazı neden kod verileri geçirilemeyebilir. Örneğin, neden kodları artık en fazla 15 karaktere sahiptir, bu nedenle 15 karakterden uzun herhangi bir neden kodu otomatik olarak geçirilmeyecektir.

**Yan hak yönetimi** çalışma alanının **Bağlantılar** sayfasında, geçişle ilgili ve herhangi bir neden kodunun geçirilmemesi hakkında sizi bilgilendiren bir başlık görürsünüz.

1. Geçiş durumuyla ilgili ayrıntılar için **Neden kodları**'nı seçin.

   [![Neden kodları.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Geçirilemeyen bir neden kodu seçin.

   [![Neden kodu geçiş durumu.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. **Neden kodunu taşı**'yı seçin.

   [![Neden kodunu taşıma.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. **Yan hak neden kodu geçişi** bölmesinde, Personel yönetimi neden koduyla eşlemek için iki seçeneğiniz vardır:

   - Personel yönetiminde var olan bir neden kodunu kullanmak için **Var olan neden kodunu kullan** açılan menüsünün içinden birini seçin.
     > [!NOTE]
     > Personel yönetiminde var olan bir neden kodunu yalnızca başka bir Yan hak yönetimi neden kodu zaten geçiş yapmamışsa kullanabilirsiniz.
   - Personel yönetiminde yeni bir neden kodu oluşturmak için **Yeni neden kodu** bölümünde yeni bir neden kodu girin ve sonra **Yeni açıklama**'ya bir açıklama girin.

   [![Personel yönetimi neden koduyla eşleme.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Neden kodları Personel yönetimine geçtikten sonra, bunları Yan hak yönetiminde kullanma seçeneği otomatik olarak **Evet** olarak ayarlanır.

[![Yan hak yönetiminde neden kodunu kullanma.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
