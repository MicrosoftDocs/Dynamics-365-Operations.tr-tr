---
title: "Satıcı kataloglarını içe aktarma"
description: "Bu konu satıcı katalog verilerini içe aktarma işlemini açıklar."
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a56e6ea0a8470f205b1c74379c887c0cac85a6b4
ms.openlocfilehash: c290bcd4787144fb4dd4232c06d2fb9e1e67ca3e
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="import-vendor-catalogs"></a>Satıcı kataloglarını içe aktarma
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Satıcı kataloglarını içe aktarma

Microsoft Dynamics 365 for Finance and Operations'da, satınalma uzmanları, şirket personelinin dahili kullanım için maddeler ve hizmetler sipariş ederken kullanabileceği kataloglar oluşturabilir ve yönetebilir. Tedarik kataloğu oluşturmak için personele sunmak istediğiniz maddeleri ve hizmetleri ürün katalog verilerini içe aktararak veya ürün katalog verilerini ana ürüne el ile ekleyerek ilave edebilirsiniz. 

Microsoft Dynamics 365 istemcisinden bir satıcı tarafından gönderilen katalog verilerini yükleyebilirsiniz.

Bir satıcının, bir katalog bakım isteği (CMR) biçiminde size gönderdiği ürün verileri, XML dosyası biçiminde olmalıdır. CMR dosyası satıcının şirketinize sağladığı ürünlerin ayrıntılarını içermelidir.

## <a name="import-vendor-catalog-data"></a>Satıcı katalog verilerini içe aktarma

Satıcı katalog verilerini içe aktarmak için aşağıdaki görevleri tamamlamanız gerekir:

1.  Veri eşleme kurallarını tanımladığınız Veri yönetimi çalışma alanında bir proje ayarlayın. **Veri yönetimi**'ni ve arından **Veri projeleri için rolleri ayarlama**'yı seçin. 

2.  Tedarik kategori hiyerarşisi ayarlayın ve satıcılarınızı tedarik kategorilerine atayın. Emtia kodları kullanıyorsanız, emtia kodlarını tedarik kategorilerine ekleyin. Tedarik kategori hiyerarşisi ayarlama hakkında bilgi için bkz. [Tedarik kategori hiyerarşisi ayarlama](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3.  Katalog içe aktarma için satıcıyı yapılandır. Bir satıcı seçin ve ardından **Tedarik** > **Kurulum** > **Katalog içe aktarma için satıcıyı yapılandır**'ı seçin.

4.  Katalog içe aktarma için iş akışını yapılandırın. CMR dosyası şablonu oluşturun ve bunu satıcınızla paylaşın.

5.  Bir satıcı kataloğu oluşturmak için **Tedarik ve kaynak atama** \> **Ortak** \> **Kataloglar** \> **Satıcı katalogları**'nı seçin. Satıcınızdan aldığınız katalog bakımı isteği (CMR) dosyaları bu katalogda gruplandırılır. 

6.  CMR dosyasını yükleyin.

7.  Satıcı kataloğundaki ürünleri gözden geçirin, onaylayın veya reddedin. Ürünler Dynamics 365 for Finance and Operations'daki tedarik kategorileriyle otomatik olarak eşlenir. 
    
Onaylana ürünler ana ürüne eklenir ve seçilen tüzel kişiliklere serbest bırakılır. Yalnızca onaylanmış ürünler tedarik kataloğuna eklenebilir.

## <a name="generate-a-catalog-import-file-template"></a>Katalog içe aktarma dosyası şablonu oluşturma

Katalog içe aktarma dosyası şablonu, satıcı ürünleri için CMR dosyası oluşturmak üzere kullandığınız endüstri standardı XSD dosyasıdır. CMR dosyasını yeni katalog oluşturmak, mevcut bir kataloğu değiştirmek veya mevcut katalogda değişiklik yapmak için kullanabilirsiniz.

1.  **Tedarik ve kaynak atama** \> **Kataloglar** \> **Satıcı katalogları**'nı seçin ve üzerinde çalışmak istediğiniz kataloğa çift tıklayın.

2.  Geçerli katalog içe aktarma şablonunu (XSD dosyası) indirin. **Katalog güncelleştir** sayfasında **Eylem Bölmesinde** bulunan **Kataloglar** sekmesindeki **İlgili bilgiler** grubunda **Katalog şablonu oluştur**'a tıklayın ve **Tedarik kategorisi**'ni seçin.

    -   **Tedarik kategori** seçeneğiyle, satıcının ürünler sağlamak için yetkilendirildiği tedarik kataloglarını içeren bir katalog şablonu oluşturabilirsiniz.

3. **Farklı kaydet** iletişim kutusunda, katalog dosyası şablonunu kaydetmek istediğiniz konumu seçin ve dosyayı kaydedin.

Daha fazla bilgi ve örnekler için bu blog gönderisine bakın: [Dynamics AX'de satıcı katalogları](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).

