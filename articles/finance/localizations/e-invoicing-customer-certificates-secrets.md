---
title: Müşteri sertifikaları ve parolaları
description: Bu makalede, Elektronik faturalamada müşteri sertifikalarının ve gizli dizilerin nasıl ayarlanacağı açıklanmaktadır.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 3943e7cb43cc6bf93995f0b3957766227cc3ec99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279855"
---
# <a name="customer-certificates-and-secrets"></a>Müşteri sertifikaları ve parolaları

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service'de (RCS) zaten bir Microsoft Azure Key Vault referansınız varsa Key Vault sertifikaları ve gizli dizilerine referanslar oluşturabilirsiniz. Key Vault referansınız yoksa, bunu oluşturma hakkında bilgi için bkz. [Hizmet ortamları](e-invoicing-service-environments.md).

## <a name="create-certificates-and-secrets"></a>Sertifikalar ve parolalar oluşturma

Sertifikalar ve parolalar oluşturmak için aşağıdaki adımları izleyin.

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Ortam kurulumu** sayfasındaki Eylem bölmesinde **Hizmet ortamları**'nı seçin.
4. **Hizmet ortamları** sayfasında, Eylem Bölmesi'nde **Key Vault parametreleri**'ni seçin.
5. **Key Vault parametreleri** sayfasında, bir Key Vault referansı seçin ve ardından **Sertifikalar** bölümünde **Ekle**'yi seçin.
6. **Ad** alanına Key Vault sertifikası veya parolasının adını girin. Daha fazla bilgi için bkz. [Azure portalında Azure depolama hesabı oluşturma](e-invoicing-create-azure-storage-account-azure-portal.md).
7. **Açıklama** alanına bir açıklama girin.
8. **Tür** alanında, Key Vault'ta saklanan bir sertifikaya referansta bulunuyorsanız **Sertifika** seçeneğini belirleyin. Key Vault'ta saklanan bir gizli diziye referansta bulunuyorsanız **Gizli Dizi** seçeneğini belirleyin.
9. **Kaydet**'i seçin.

> [!NOTE]
> Bazı senaryolarda, .cer dosya adı uzantısına sahip ortak sertifikalar kullanmalısınız. Ancak, Key Vault bu tür sertifikaları Key Vault sertifikaları olarak almayı ve depolamayı desteklemez. Bu senaryolarda, .cer dosyasını Base-64 kodlu bir X. 509 (.CER) dizesi olarak kaydetmeniz gerekir. Daha sonra, Key Vault parolasında dosyadaki **SERTİFAKALAMAYA BAŞLA** satırında ve **SERTİFAKALAMAYI SONLANDIR** satırı arasında görüntülenen diziyi saklayın. Hizmet ortamında, Key Vault kaydına referans oluşturmanız ve **Tür** alanını **Sertifika** olarak ayarlamanız gerekir.

## <a name="create-a-chain-of-certificates"></a>Sertifika zinciri oluşturma

Ülke/bölgeye özel faturalarınızda dijital imzalara sertifika zinciri uygulanması veya güvenli (Güvenli Yuva Katmanı \[SSL\]) bağlantısıyla harici web hizmetlerine bağlanılması gerekiyorsa, sertifikaların aşağıdaki sırada olacağı bir sertifika zinciri oluşturun:

1. Kök sertifikalar
2. Ara sertifikalar
3. Son kullanıcı sertifikaları

Kök sertifika yetkilileri (CA'lar), güvenilir bir sertifika kaynağıdır. Ara CA sertifikaları, son kullanıcı sertifikalarını kök CA sertifikalarına bağlayan köprülerdir.

Sertifika zinciri oluşturmak için aşağıdaki adımları izleyin.

1. **Key Vault parametreleri** sayfasında, Eylem Bölmesinde, **Sertifikalar zinciri**'ni seçin.
2. Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.
3. **Ad** alanına sertifika zinciri adını girin.
4. **Açıklama** alanına bir açıklama girin.
5. **Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.
6. Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın. CA kök sertifikasını listenin başında ve son kullanıcı sertifikasını altta tutun.
7. **Kaydet**'i seçin.

Dilediğiniz sayıda RCS'de Key Vault referansı oluşturabilirsiniz. Belirli bir hizmet ortamını Key Vault referansına bağlamak için, depolama paylaşılan erişim imzası (SAS) belirtecinin parolasının kullanılacağını unutmayın. Ayrıca, hizmet ortamını kurarken kullandığınız depolama SAS belirteci için parolayı içeren bir anahtar kasasında depolanan Key Vault sertifikalarına ve gizli dizilerine başvurabilirsiniz.
