---
title: Neden kodlarını ayarla
description: Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056360"
---
# <a name="set-up-reason-codes"></a>Neden kodlarını ayarla

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.

> [!NOTE]
> Ocak 2021 itibarıyla, neden kodları **Yan hak yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçiriliyor. Daha fazla bilgi için, bkz. [Neden kodlarını el ile Personel yönetimine geçirme](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Neden kodları oluşturma

1. **Personel yönetimi** çalışma alanında (veya neden kodlarınız henüz geçirilmediyse **Yan hak yönetimi** çalışma alanı), **Bağlantılar**'ı ve ardından **Neden kodları**'nı seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Neden kodu** | Bir çalışanın bir kazanç planı kaydını değiştiren nedenini tanımlamak için benzersiz ad. |
   | **Açıklama** | Neden kodunun açıklaması. |

4. **Uygulanabilir senaryolar** altında, **Yan hak yönetimi**'ni **Evet** olarak ayarlayın. (Neden kodlarınız henüz **Personel yönetimi** çalışma alanına geçirilmediyse geçerli değildir.)

5. **Kaydet**'i seçin.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Neden kodlarını Personel yönetimine el ile geçirme

Ocak 2021'de, neden kodları **Yan hak yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçiriliyor. Çoğu neden kodu verileri ortamınıza otomatik olarak geçiş yapacaktır. Bazı neden kod verileri geçirilemeyebilir. Örneğin, neden kodları artık en fazla 15 karaktere sahiptir, bu nedenle 15 karakterden uzun herhangi bir neden kodu otomatik olarak geçirilmeyecektir.

**Yan hak yönetimi** çalışma alanının **Bağlantılar** sayfasında, geçişle ilgili ve herhangi bir neden kodunun geçirilmemesi hakkında sizi bilgilendiren bir başlık görürsünüz.

1. Geçiş durumuyla ilgili ayrıntılar için **Neden kodları**'nı seçin.

   [![Neden kodları](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Geçirilemeyen bir neden kodu seçin.

   [![Neden kodu geçiş durumu](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. **Neden kodunu taşı**'yı seçin.

   [![Neden kodunu taşı](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. **Yan hak neden kodu geçişi** bölmesinde, Personel yönetimi neden koduyla eşlemek için iki seçeneğiniz vardır:

   - Personel yönetiminde var olan bir neden kodunu kullanmak için **Var olan neden kodunu kullan** açılan menüsünün içinden birini seçin.
     > [!NOTE]
     > Personel yönetiminde var olan bir neden kodunu yalnızca başka bir Yan hak yönetimi neden kodu zaten geçiş yapmamışsa kullanabilirsiniz.
   - Personel yönetiminde yeni bir neden kodu oluşturmak için **Yeni neden kodu** bölümünde yeni bir neden kodu girin ve sonra **Yeni açıklama**'ya bir açıklama girin.

   [![Personel yönetimi neden koduyla eşleme](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Neden kodları Personel yönetimine geçtikten sonra, bunları Yan hak yönetiminde kullanma seçeneği otomatik olarak **Evet** olarak ayarlanır.

[![Yan hak yönetiminde neden kodunu kullanma](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]