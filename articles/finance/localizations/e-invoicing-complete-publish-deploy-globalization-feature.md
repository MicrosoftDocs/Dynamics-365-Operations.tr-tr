---
title: Genelleştirme özelliğini tamamlama, yayımlama ve dağıtma
description: Bu konuda, Genelleştirme özelliklerinin yaşam döngüsü hakkında bilgiler verilir.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a842a3ba31c0a8e0d80ad1856d9d6d861a8514ea
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371787"
---
# <a name="complete-publish-and-deploy-a-globalization-feature"></a>Genelleştirme özelliğini tamamlama, yayımlama ve dağıtma

[!include [banner](../includes/banner.md)]

## <a name="electronic-invoicing-feature-versions"></a>Elektronik faturalama özelliği sürümleri

Elektronik faturalama özelliklerinin sürümleri oluşturulur. Yeni bir sürüm oluşturulduğunda, sürüm numarası otomatik olarak artırılır.

Elektronik faturalama özelliği sürümleri, en fazla üç durumu olan bir yaşam döngüsünü izler:

- **Taslak** – Bir özellik sürümü bu durumdaysa, yapılandırma özniteliklerini ve yapılarından herhangi birini (örneğin, dosya biçimi yapılandırmaları) düzenleyebilirsiniz.
- **Tamamlandı** – Bu durum, özellik sürümünü düzenlemeyi bitirdiğiniz ve üzerinde başka güncelleştirmeler yapmak istemediğiniz anlamına gelir. Bir özellik sürümü bu durumda olduğunda, bunu veya bileşenlerini artık düzenleyemezsiniz.
- **Yayımlandı** – Bu durum, kuruluşunuzla ilişkili Global depoda yayınlandığını belirtir. Bir özellik sürümü bu durumda olduğunda, bunu veya bileşenlerini artık düzenleyemezsiniz.

Elektronik faturalama özelliğinin yeni bir sürümü için **Geçerlilik başlangıç tarihini** belirtebilirsiniz. Bu şekilde, kullanılabilecek varsayılan bir sürüm tanımlayabilirsiniz veya özellik servis ortamına dağıtıldığında üzerine yazılabilir.

Elektronik faturalama özellik sürümünün durumunu değiştirmek için, aşağıdaki adımları izleyin.

1. Regulatory Configuration Service (RCS) hesabınızda oturum açın.
2. **Genelleştirme özelliği** çalışma alanında, **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
3. **Elektronik faturalama özellikleri** sayfasının solunda, elektronik faturalama özelliğini seçin.
4. Sayfanın sağ tarafındaki **Sürümler** sekmesinde, sürümü seçin.
5. **Değişiklik durumunu** seçin ve sonra **Tamamlandı** (geçerli durum **Taslak** ise ) veya **Yayımlandı** (geçerli durum **Tamamlandı** ise) öğesini seçin.
6. İleti kutusunda **Evet**'i seçerek isteği doğrulayın.

**Tamamlandı** durumundan **Yayımlandı** durumuna el ile geçiş isteğe bağlıdır. Elektronik faturalama özellik sürümleri, servis ortamına dağıtıldığında, otomatik olarak **Yayımlandı** durumuna güncelleştirilir.

Durumu , **Sürümler** sekmesindeki **Özellik sürümü durumu** sütununda izleyebilirsiniz.

## <a name="deploy-feature-versions"></a>Özellik sürümlerini dağıtma

RCS'de, bir elektronik faturalama özellik sürümünü hedef servis ortamı veya bağlı uygulamaya yayımlamak için **Dağıt** komutunu kullanırsınız.

1. **Elektronik faturalama özellikleri** sayfasının solunda, elektronik faturalama özelliğini seçin.
2. Sayfanın sağ tarafındaki **Sürümler** sekmesinde, servis ortamına veya bağlı uygulamaya dağıtmak istediğiniz elektronik faturalama özellik sürümünü seçin. Seçilen sürümün durumu **Tamamlandı** veya **Yayımlanmış** olmalıdır.
3. **Dağıt**'ı seçin ve sonra dağıtımın hedefini tanımlamak için aşağıdaki seçeneklerden birini veya ikisini belirleyin:

    - **Bağlantılı uygulama** – Uygulama kurulumu tarafından sağlanan konfigürasyon, daha önce kendisiyle ilişkili olan Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management örneğinde yazılır.
    - **Servis ortamı** – Elektronik faturalama özellik sürümü servis ortamına dağıtılır. Elektronik faturalama daha sonra Finance veya Supply Chain Management'ın gönderdiği elektronik belgeleri almaya ve işlemeye hazır hale gelir.

> [!NOTE]
> Genellikle, servis ortamına dağıtılması gereken Elektronik raporlama (ER) özelliğinin parametrelerini değiştirirsiniz. Bağlı uygulamada yapılan değişiklikler nadiren yapılır. Yeni sürümleri, yalnızca uygulamanızın karşılık gelen parametrelerini değiştirdiğinizde bağlı olan uygulamaya dağıtmanız gerekir.

Belirli bir ortama elektronik faturalama özelliğinin belirli bir sürümünün dağıtılıp dağıtılmadığını belirlemek için, **Ortamlar** sekmesindeki bilgileri gözden geçirin.

## <a name="remove-feature-versions"></a>Özellik sürümlerini kaldırma

RCS'de, burada dağıtılmışsa bir hizmet ortamından belirli bir elektronik faturalama özelliği sürümünü kaldırmak için **İptal**'i seçebilirsiniz.

> [!IMPORTANT]
> **İptal** düğmesi yalnızca servis ortamları için geçerlidir. Geçerli elektronik faturalam özelliği için bağlı uygulamadan hiçbir şey kaldırmaz.

## <a name="rebase-electronic-invoicing-features"></a>Elektronik faturalama özelliklerini yeniden temellendirme

Bir elektronik faturalama özelliği diğerinden türetildiğinde, **Yeniden temelle** özelliğini seçerek türetilen özelliği orijinal (üst) özellikte sunulan değişikliklerle güncelleştirebilirsiniz.

Oluşturduğunuz bir özelliğin türetilmiş sürümünü yeniden temellendirmek için aşağıdaki adımları izleyin.

1. Özelliği Genel depodan içe aktararak özelliğin en son sürümünü edinin. Daha fazla bilgi için bkz. [Global depodan içe aktarma özelliği](e-invoicing-import-feature-global-repository.md).
2. Özellik listesinde, yeniden temellendirme özelliğini seçin.
3. **Sürümler** sekmesinde, taslak sürümünü oluşturmak için **yeni**'yi seçin.
4. **Yeniden temellendirme** seçin.
5. **Yeniden temellendirme** iletişim kutusunda, tekrar temellendirmek için özelliğin sürümünü seçin.
6. **Tamam**'ı seçin.
7. Özellik bileşenlerini gözden geçirin ve gerekli değişiklikleri yapın.
8. Yeniden temellendirilen özelliği tamamlamak için **durumu değiştir**'i seçin. Yeniden temellendirme tamamlandığı zaman ek eylemler gerçekleştirebilirsiniz.

## <a name="get-a-specific-version-of-electronic-invoicing-features"></a>Elektronik faturalama özelliklerinin spesifik bir sürümünü edinme

Elektronik faturalama özelliğinin yeni sürümünü oluşturduğunuzda, sistem en son özellik sürümünün bir kopyasını oluşturur. Yeni sürümün temeli olarak özelliğin önceki bir sürümünü kullanmak için, sürümü seçin ve ardından **Bu sürüm komutunu al**'ı seçin. Seçili sürümün kopyası olan, özelliğin yeni bir taslak sürümü oluşturulur.
